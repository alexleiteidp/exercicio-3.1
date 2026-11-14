# A — Meta-prompt

> **Assistente 1:** Claude (Anthropic, modelo Claude Opus 5.5), com busca na web.
> **Data de uso:** 14/11/2026.
> **Função deste arquivo:** é o pedido que fiz ao assistente 1 para que **ele escrevesse o prompt** de deep research. Não pedi a pesquisa em si. O prompt gerado está no Apêndice.

---

## Meta-prompt enviado ao assistente 1

Sou advogado e aluno da disciplina "Governo Digital e Transformação de Serviços Públicos no Brasil" (IDP, 2026). Preciso que você **elabore um prompt para um assistente de deep research**. Não faça a pesquisa agora: escreva o prompt.

**O serviço.** O serviço é o **"Atendimento ao Seguro-Desemprego pela URA da Caixa"**:
- **Canal:** a central telefônica Atendimento CAIXA ao Cidadão, **0800 726 0207**, com menu de voz (URA/IVR), autoatendimento, fila e transbordo para atendente.
- **Órgãos:** a **Caixa Econômica Federal**, que é o agente pagador e dona do canal, e o **Ministério do Trabalho e Emprego (MTE)**, que concede o benefício. Na retaguarda estão a **Dataprev**, que opera o sistema de habilitação, e o **CODEFAT**, que edita as normas.
- **Público:** o trabalhador formal dispensado sem justa causa.

**O problema.** Vou desenhar um **Service Blueprint AS-IS**, na metodologia de G. Lynn Shostack (1984), que retrate **como o serviço opera hoje**, e não como deveria operar. Depois da pesquisa, farei uma entrevista adversarial (`/grill-me`) com um agente de IA. Nela vou decidir as etapas, as camadas, onde passa a Linha de Visibilidade e quais são os fail points. A pesquisa precisa sustentar essas decisões.

**O que já tenho.** Fiz um mapa de atores desse serviço (exercício 2.1), que vai anexo como contexto. Ele tem 22 atores, entre eles:
- URA, atendente terceirizado, Caixa e MTE;
- o motor de habilitação, a Dataprev, as bases de vínculo (CNIS, eSocial, FGTS) e o empregador;
- WhatsApp Caixa, Celeste, Central 158, app Carteira de Trabalho Digital, SRTE/Sine e órgãos de controle.

O mapa também identificou fail points: desistência na fila, URA que não explica indeferimento, transbordo em cadeia e dado errado do empregador.

**O que o prompt deve exigir do pesquisador:**
1. **Jornada na ótica do cidadão.** As etapas começam antes da ligação, no momento em que o cidadão percebe que a parcela não caiu, e não no balcão. Para cada etapa: o que o cidadão faz, o que vê e ouve, e quanto tempo leva, quando houver dado.
2. **Frontstage.** O que é visível ao cidadão: menus da URA, mensagens gravadas, identificação, autoatendimento, atendente humano e scripts.
3. **Backstage e processos de suporte.** Quem faz o quê fora da vista do cidadão:
   - roteamento (ACD/CTI) e o contrato de teleatendimento;
   - a consulta ao sistema de pagamento da Caixa;
   - o motor de habilitação do MTE/Dataprev e as bases CNIS, eSocial e FGTS;
   - a ordem de pagamento do FAT, a notificação e o recurso.
4. **Evidências físicas** de cada etapa: o número do telefone, a música de espera, o protocolo, o SMS, a carta, o extrato e a tela do app.
5. **Normativos aplicáveis**, com artigo:
   - Lei 7.998/1990 e Res. CODEFAT 957/2022;
   - Decreto 11.034/2022 (regras de SAC);
   - Lei 13.460/2017 (direitos do usuário de serviço público);
   - LGPD;
   - normas internas da Caixa, quando forem públicas.
6. **Fail points e gargalos conhecidos**, com fonte. Exemplos: acórdãos do TCU, reclamações no consumidor.gov.br e no Reclame Aqui, Ouvidoria, notícias e auditorias da CGU. Para cada um: em que etapa ocorre e quem responde.
7. **Formato de saída:**
   - (a) sumário;
   - (b) tabela de etapas com colunas por camada do blueprint;
   - (c) fail points;
   - (d) normativos;
   - (e) lacunas e incertezas;
   - (f) fontes com URL.
8. **Regras de evidência.** Use fontes primárias quando houver: planalto.gov.br, gov.br/trabalho-e-emprego, caixa.gov.br, TCU e DOU. Marque o que for **[INFERÊNCIA]** e o que estiver **[NÃO CONFIRMADO]**. Não invente tempos de espera, números de contrato nem estatísticas. Data de referência: novembro de 2026.

Escreva o prompt em português, pronto para colar, com persona, objetivo, escopo, perguntas de pesquisa, formato de saída e regras de evidência.

---

## Apêndice — Prompt de deep research gerado pelo assistente 1

> Colado aqui só para rastreabilidade. O entregável da Parte A é o meta-prompt acima.

```
# PERSONA
Você é um pesquisador sênior em design de serviços públicos e direito administrativo brasileiro. Domina a metodologia de Service Blueprint de G. Lynn Shostack (1984) e suas camadas (evidências físicas, ações do cliente, frontstage, linha de visibilidade, backstage, processos de suporte). Conhece a legislação do seguro-desemprego, as regras de SAC e o controle externo (TCU/CGU). Escreve em português do Brasil, com rigor de fonte.

# OBJETIVO
Levantar, com evidência verificável, como o serviço "Atendimento ao Seguro-Desemprego pela URA da Caixa" funciona HOJE (AS-IS, referência: novembro de 2026), para sustentar um Service Blueprint que será depois discutido numa entrevista adversarial. Não proponha melhorias (TO-BE). Descreva o que existe, com o que está provado separado do que é inferido.

# ESCOPO
- Serviço: atendimento telefônico ao seguro-desemprego do trabalhador formal dispensado sem justa causa (Lei 7.998/1990; Res. CODEFAT 957/2022).
- Canal central: Atendimento CAIXA ao Cidadão, 0800 726 0207 (URA/IVR, autoatendimento, fila, transbordo para atendente humano).
- Órgãos: Caixa (agente pagador e dona do canal); MTE (concedente); Dataprev (opera o sistema de habilitação); CODEFAT (normatiza).
- Jornada: começa ANTES da ligação, quando o cidadão percebe que a parcela não caiu, e termina na resolução, no encaminhamento, na desistência ou na reclamação posterior.
- Fora do escopo: empregado doméstico, pescador artesanal (seguro-defeso), trabalhador resgatado e bolsa qualificação. Cite-os só se afetarem o fluxo do formal.
- Contexto anexo: mapa de atores do exercício 2.1 (22 atores; fail points já levantados: desistência na fila, URA que não explica indeferimento, transbordo em cadeia, dado errado do empregador). Use-o como ponto de partida, não como prova.

# PERGUNTAS DE PESQUISA
1. Jornada (ótica do cidadão): quais são as etapas, da percepção de que a parcela não caiu até o desfecho? Em cada uma: o que o cidadão faz, vê e ouve; quanto tempo leva, SE houver dado publicado.
2. Frontstage: qual é o menu atual da URA (opções, mensagens gravadas)? Como o cidadão se identifica (CPF, NIS, senha)? Quais consultas são autoatendidas? Quando e como há transbordo para atendente? Há script público?
3. Backstage: quem atende (equipe própria ou terceirizada; contrato vigente)? Como funciona o roteamento (ACD/CTI)? Que sistema da Caixa o atendente consulta? A URA consulta dados do MTE ou só de pagamento?
4. Processos de suporte: como o motor de habilitação do MTE/Dataprev cruza CNIS, eSocial, FGTS e Empregador Web? Como a ordem de pagamento chega à Caixa? Como funcionam notificação, recurso e reemissão de parcela?
5. Evidências físicas: número de telefone, música/mensagem de espera, protocolo de atendimento, SMS, carta/notificação, extrato, telas da CTPS Digital, do CAIXA Tem e do app Benefícios Sociais.
6. Normativos (com artigo): Lei 7.998/1990; Res. CODEFAT 957/2022 e alterações; Decreto 11.034/2022 (SAC); Lei 13.460/2017; LGPD (Lei 13.709/2018); Lei 14.129/2021; normas internas públicas da Caixa. O Decreto 11.034 se aplica à Caixa nesse atendimento? Diga se é fato ou inferência.
7. Fail points: o que dizem acórdãos do TCU, relatórios da CGU, ouvidorias, consumidor.gov.br, Reclame Aqui e imprensa? Para cada falha: etapa, evidência (com URL) e quem responde (Caixa, MTE, Dataprev, empregador).
8. Lacunas: o que não foi possível confirmar em fonte pública, e como confirmar (ex.: ligação de teste, pedido via Lei de Acesso à Informação).

# FORMATO DE SAÍDA (Markdown, 2.000 a 3.500 palavras)
(a) Sumário (5 a 8 tópicos).
(b) Tabela de etapas (mínimo 7), com colunas: Etapa | Evidências físicas | Ações do cidadão | Frontstage | Backstage | Processos de suporte. Indique onde passa a Linha de Visibilidade.
(c) Fail points: tabela com # | Falha | Etapa | Evidência (URL) | Quem responde.
(d) Normativos: tabela com Norma | Artigo | O que exige | Etapa afetada.
(e) Lacunas e incertezas.
(f) Fontes com URL completa, numeradas.

# REGRAS DE EVIDÊNCIA
- Priorize fontes primárias: planalto.gov.br, in.gov.br (DOU), gov.br/trabalho-e-emprego, portalfat, caixa.gov.br, portal.tcu.gov.br, gov.br/cgu, pncp.gov.br.
- Fontes secundárias (imprensa, Reclame Aqui, consumidor.gov.br, blogs) servem para fail points e indícios, nunca para afirmar norma.
- Toda afirmação factual deve ter URL. Cite o artigo exato das normas.
- Marque [INFERÊNCIA] quando deduzir algo sem fonte direta e [NÃO CONFIRMADO] quando a fonte for antiga, indireta ou ambígua.
- NÃO invente tempos de espera, números de contrato, nomes de fornecedores, estatísticas, acórdãos ou jurisprudência. Se não achar, escreva "não localizado".
- Indique a data da fonte quando ela puder estar desatualizada (ex.: menu de URA de anos anteriores).
- Data de referência: novembro de 2026.
```
