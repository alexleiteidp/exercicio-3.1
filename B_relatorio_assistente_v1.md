# B — Relatório do assistente 1 (v1)
> **Assistente 1:** Claude (Anthropic, Claude Opus 5.5), com busca web · **Data:** 14/11/2026 · **Prompt:** o do Apêndice de `A_meta_prompt.md`.

**Convenções.** Os números entre colchetes, como [3], remetem à lista de fontes da seção (f). **[INFERÊNCIA]** marca dedução sem fonte direta. **[NÃO CONFIRMADO]** marca fonte antiga, indireta ou ambígua. Fatos já verificados no relatório v3 do exercício 2.1 vêm com a mesma URL. Quando não consegui reabrir a página nesta data, isso está dito.

---

## (a) Sumário

- **O serviço é bifurcado.** O MTE concede o benefício, com habilitação automática a partir de bases de vínculo (Res. CODEFAT 957/2022, art. 4º, § 1º) [1]. A Caixa paga: é o agente pagador (art. 64, § 1º) [1][2]. A URA 0800 726 0207 fica do lado do pagamento. A FAQ da Caixa manda dúvidas de concessão e de valor para a CTPS Digital ou o gov.br [6].
- **A jornada começa fora do telefone.** O cidadão percebe que a parcela não caiu, olha o app ou a conta e só depois liga. Os motivos mais comuns de "não caiu" são decisões do MTE: notificação, suspensão por novo emprego, indeferimento (Lei 7.998, arts. 7º e 8º; Res. 957, arts. 22 e 23) [3][2]. A URA não tem como resolver esses motivos.
- **A camada de suporte é toda invisível.** O MTE processa os documentos de pagamento em lotes semanais e os entrega à Caixa. A Caixa devolve ao sistema do MTE a informação de pagos e não pagos (Res. 957, art. 65) [2]. Uma pane no TED do Banco Central já atrasou 45.335 parcelas em maio de 2023 [15].
- **O TCU confirmou em 2026 os fail points do canal.** O Acórdão 1621/2026 aponta canais que não resolvem com rapidez, falta de base de conhecimento única e trabalhador "encaminhado de um lugar para outro". Aponta também a duplicidade Empregador Web × eSocial, que gera bloqueios e indeferimentos [12].
- **Mudou a norma de SAC.** O Decreto 11.034/2022 foi revogado pelo **Decreto 13.135, de 9/10/2026** (art. 24), que vigora 20 dias após a publicação (art. 25) [8]. A data de 2/11/2026 é cálculo meu sobre a publicação no DOU de 13/10/2026 [NÃO CONFIRMADO no DOU]. O novo decreto fixa espera de até 20 segundos para 80% das chamadas, no máximo cinco níveis de menu e opção de atendimento humano em todos os níveis (arts. 15 e 16) [8]. Se ele se aplica à URA do seguro-desemprego é **[INFERÊNCIA]** (ver seção d).
- **Continuam sem fonte primária:** o menu atual da URA; a tecnologia de voz; quem opera o call center; tempos reais de espera. A licitação CECOT 121/2026 da Caixa (atendimento multimeios, R$ 89,7 milhões estimados) continua sem resultado no PNCP, e não está provado que ela cubra o 0800 726 0207 [13].
- **A informação oficial é inconsistente entre canais.** A página de recurso do gov.br ainda cita a Res. 467/2005, revogada, e foi modificada em 25/09/2026 [10]. A FAQ do gov.br fala em revisão em "dois anos" e no app SINE-Fácil, enquanto a Res. 957 fixa 120 dias para o recurso [11][1].

---

## (b) Etapas da jornada (ótica do cidadão)

A **Linha de Visibilidade** passa entre as colunas "Frontstage" e "Backstage". A **Linha de Interação** passa entre "Ações do cidadão" e "Frontstage". Não há dado público de tempo de espera para nenhuma etapa telefônica. Os tempos citados vêm de norma ou de Carta de Serviços, e não de medição.

| # | Etapa | Evidências físicas | Ações do cidadão | Frontstage | Backstage | Processos de suporte |
|---|---|---|---|---|---|---|
| E1 | **Percebe que a parcela não caiu** | Extrato da conta ou do CAIXA Tem sem o crédito; data prevista vista antes no app | Espera o crédito na data; confere o saldo | — (ainda não há contato) | — | 1ª parcela 30 dias após o requerimento e as demais a cada 30 dias (Res. 957, art. 12) [2]. Ordem de crédito: conta indicada, depois conta digital localizada pelo agente pagador (art. 20, § 2º) [2]. Lotes semanais MTE → Caixa (art. 65) [2] |
| E2 | **Procura o motivo por conta própria** | Tela "Consultar Seguro-Desemprego" e aba "Notificações" (CTPS Digital); app Benefícios Sociais CAIXA (situação das parcelas) [11][7] | Abre os apps, pesquisa na internet, decide ligar | Apps CTPS Digital e Benefícios Sociais | Motor de habilitação (MTE/Dataprev) grava o status e a notificação | Notificação só digital, mediante anuência (Res. 957, art. 8º) [1][2]. Cruzamento com CNIS, FGTS, GFIP, eSocial e documento judicial (art. 4º, § 1º) [1] |
| E3 | **Liga para o 0800 726 0207 e ouve o menu** | Número 0800 726 0207 (FAQ Caixa) [6]; mensagens gravadas; "opção 5" para o seguro em matéria de 2018 [16] [NÃO CONFIRMADO em 2026] | Disca, ouve as opções e escolhe pelo teclado (DTMF) ou pela voz [NÃO CONFIRMADO] | URA (atendimento eletrônico 24h) [6] | Plataforma de URA e roteamento ACD/CTI [INFERÊNCIA: padrão de contact center, sem documento da Caixa] | Contrato de teleatendimento [NÃO CONFIRMADO: fornecedor desconhecido] [13] |
| E4 | **Identifica-se e ouve o status automático** | NIS e CPF digitados; "identificação positiva" por dados cadastrais [16] [NÃO CONFIRMADO em 2026] | Digita o NIS ou o CPF e confirma dados | URA informa se o requerimento foi liberado, se a parcela está agendada ou paga e a data da próxima [16] [NÃO CONFIRMADO em 2026] | Consulta ao sistema de pagamento da Caixa (documentos de seguro-desemprego recebidos do MTE) [INFERÊNCIA a partir do art. 65 da Res. 957] | Sistema do MTE recebe os "pagos/não pagos" (art. 65, § 4º) [2]. Prazo de 67 dias e devolução ao FAT (art. 21) [2] |
| E5 | **Pede atendente e espera na fila** | Música ou mensagem de espera [NÃO CONFIRMADO: conteúdo não documentado]; tempo de espera não informado publicamente | Escolhe falar com atendente; espera; pode desistir | Fila; atendimento humano de seg. a sex., das 8h às 21h, e aos sábados, das 10h às 16h [4] (dado do v3; página não reaberta nesta data) | Distribuição automática de chamadas (ACD) [INFERÊNCIA] | Níveis de serviço do contrato [NÃO CONFIRMADO]. Regra do Decreto 13.135: até 20 s para 80% das chamadas (art. 15, I) [8], aplicabilidade em [INFERÊNCIA] |
| E6 | **Fala com o atendente** | Voz do atendente; número de protocolo [INFERÊNCIA: exigido pelo art. 18 do Decreto 13.135 [8], sem prova de prática] | Explica o problema; informa dados | Atendente CAIXA Cidadão; intérprete de Libras por videochamada para pessoas surdas, por canal próprio [5] | Atendente consulta a situação de pagamento; não decide a concessão | O MTE é o gestor do benefício: em 2023, a própria Caixa disse que as informações "devem ser buscadas" no Ministério [14] |
| E7 | **É encaminhado a outro canal** | Indicação verbal de app, site ou telefone; ligação para o 158 (gratuita só de telefone fixo) [9] | Desliga e procura CTPS Digital, gov.br, 158 ou agência | Fala do atendente ou mensagem da URA | Não há evidência de transferência direta da chamada ao 158 [INFERÊNCIA] | Central 158 do MTE, das 7h às 19h, atendimento eletrônico ou humano [9]. Celeste e Plataforma Facilita [17] |
| E8 | **Resolve (ou tenta) no canal do MTE** | Notificação com o motivo; formulário de recurso; anexos; tela com datas das parcelas, se deferido [10][11] | Lê a notificação; apresenta recurso em até 120 dias; corrige dados; pede reemissão | gov.br, CTPS Digital; presencial em SRTE/Sine com agendamento pelo 158 ou pela Facilita [10] | Análise do recurso pela Secretaria de Trabalho, "em regra" cerca de 30 dias [10] | Recurso em instância única (Res. 957, arts. 27 e 28) [1]. Reemissão em até 2 anos a pedido ou por ordem judicial (art. 21, § 2º) [2]. Defesa em 30 dias quando há indício de irregularidade (art. 24) [2] |
| E9 | **Recebe, desiste ou reclama** | Crédito na conta ou saque com cartão; protocolo de reclamação | Saca; ou abandona; ou reclama | SAC e Ouvidoria Caixa; consumidor.gov.br; Fala.BR (MTE) [4][18] | Tratamento da manifestação | Prazo de 30 dias da ouvidoria pública (Lei 13.460, art. 16) [19]. Prazo de 7 dias corridos no SAC (Decreto 13.135, art. 21) [8], aplicabilidade em [INFERÊNCIA] |

**Notas sobre as etapas.**
- E3 a E6 formam o "momento URA". As etapas E1, E2, E7 e E8 ocorrem fora da ligação, mas definem se ela é útil.
- O ponto de virada é E6. Ali o cidadão descobre se o problema é de **pagamento** (Caixa resolve) ou de **concessão** (MTE resolve).
- Em E7 começa o "transbordo de canal": o cidadão sai da URA para outro canal, e não para outro setor dentro do mesmo atendimento.

---

## (c) Fail points

| # | Falha | Etapa | Evidência | Quem responde |
|---|---|---|---|---|
| FP1 | **A URA não explica o motivo do bloqueio ou indeferimento.** O motivo está na notificação do MTE, que é digital; a URA informa pagamento | E4, E6 | FAQ Caixa remete concessão ao app/gov.br [6]; notificação digital (Res. 957, art. 8º) [1]; aba "Notificações" [11] | MTE (conteúdo da decisão); Caixa (roteiro da URA) |
| FP2 | **Transbordo em cadeia:** o cidadão é encaminhado de um canal a outro | E7 | TCU 1621/2026: casos semelhantes recebem respostas diferentes e o trabalhador é encaminhado de um lugar para outro [12]. Nota da Caixa de 2023 remetendo ao MTE [14] | MTE (base de conhecimento única); Caixa (roteiro de encaminhamento) |
| FP3 | **Dado errado ou em duplicidade do empregador** gera bloqueio e indeferimento | Antes de E1; aparece em E2/E4 | TCU 1621/2026: dois sistemas paralelos (Empregador Web e eSocial), com erros, divergências, bloqueios e indeferimentos; prazo de 180 dias ao MTE [12]. Res. 957, art. 40, § 1º [1] | MTE (integração determinada); empregador (qualidade do dado) |
| FP4 | **Desistência na fila** sem registro nem responsável | E5 | Não há dado público de tempo de espera ou de abandono no 0800 726 0207 (busca sem resultado). Falha mantida como hipótese do mapa 2.1 [INFERÊNCIA] | Caixa (dona do canal e do contrato) |
| FP5 | **Recurso lento e pouco previsível** | E8 | TCU 1621/2026: análise "lenta e pouco previsível" [12]. TCU 135/2024: cerca de 4 mil recursos por ano sobre pedidos já com dois recursos negados; um requerimento analisado 15 vezes [20] | MTE; Dataprev (sistema) |
| FP6 | **Informação oficial desatualizada ou contraditória** | E2, E8 | Página de recurso cita Res. 467/2005, revogada [10]; FAQ gov.br fala em revisão em "dois anos" e no app SINE-Fácil [11], enquanto a Res. 957 fixa 120 dias (art. 27) [1] | MTE (Carta de Serviços, Lei 13.460, art. 7º, § 4º) [19] |
| FP7 | **Falha na liquidação financeira** atrasa parcelas em massa | Entre E1 e E4 | 45.335 parcelas por TED atrasadas em maio de 2023, atribuídas pela Caixa à indisponibilidade do TED do Banco Central; reemissão no lote seguinte [15] | Caixa (agente pagador); Banco Central; MTE (reemissão) |
| FP8 | **Parcela devolvida ao FAT** após 67 dias sem saque; canal de reemissão do trabalhador formal não documentado | E1, E8 | Res. 957, art. 21 e § 2º [2]; FAQ gov.br manda procurar "agências da CAIXA" quando a parcela não está disponível no cartão [11] | Caixa; MTE |
| FP9 | **Horários e custos desalinhados entre canais** | E5, E7 | Atendente Caixa até 21h [4]; 158 até 19h e gratuito só de fixo [9] | Caixa; MTE |
| FP10 | **Pagamentos indevidos e falha de governança Dataprev** (risco que gera bloqueios posteriores) | Suporte | TCU 135/2024: indícios de R$ 147 milhões e de cerca de R$ 544 mil; falhas na relação contratual Strab–Dataprev [20] | MTE; Dataprev |

---

## (d) Normativos

| Norma | Artigo | O que exige ou prevê | Etapa |
|---|---|---|---|
| Lei 7.998/1990 [3] | art. 3º | Requisitos (tempo de salário, ausência de benefício continuado, renda própria) | Suporte (E2) |
| | art. 6º | Requerimento a partir do 7º dia após a rescisão | Antes de E1 |
| | art. 7º, I a IV | Suspensão: novo emprego, benefício previdenciário continuado, auxílio-desemprego, recusa de recolocação | E1, E2 |
| | art. 8º | Cancelamento: recusa de emprego, falsidade, fraude, morte | E2 |
| | art. 15 | Pagamento pelos bancos oficiais federais | E4 |
| | art. 19, XIV | CODEFAT fixa prazos de processamento, com meta de 30 dias | Suporte |
| Res. CODEFAT 957/2022 [1][2] | art. 4º, § 1º | Habilitação automática por CNIS, FGTS, GFIP, eSocial ou documento judicial | Suporte |
| | art. 8º | Notificação exclusivamente digital, mediante anuência | E2 |
| | art. 12 | 1ª parcela 30 dias após o requerimento; as demais a cada 30 dias | E1 |
| | art. 20, §§ 2º e 4º | Crédito em conta; conta digital localizada pelo agente pagador; guarda de comprovantes por 5 anos | E1, E4 |
| | art. 21 | 67 dias de disponibilidade; devolução ao FAT; reemissão em até 2 anos | E8 |
| | arts. 22 a 24 | Suspensão, cancelamento e defesa em 30 dias | E2, E8 |
| | arts. 27 e 28 | Recurso em 120 dias, instância única, digital ou presencial | E8 |
| | art. 40, § 1º | Empregador transmite "exclusivamente" pelo Empregador Web | Antes de E1 |
| | art. 64, § 1º; art. 65 | Caixa é agente pagador; lotes semanais MTE → Caixa; retorno de pagos/não pagos ao sistema do MTE | Suporte |
| Decreto 13.135/2026 (SAC) [8] | art. 1º, par. ún. | Âmbito: serviços regulados pelo Executivo federal (I); serviços financeiros digitais supervisionados pelo BC (II) | E3 a E6 |
| | art. 3º, § 3º; art. 4º, VIII | Automação e IA permitidas, desde que o consumidor possa escolher atendimento humano | E3, E5 |
| | art. 14, § 1º | Atendimento humano das 8h às 20h, sete dias por semana | E5 |
| | art. 15, I | Espera de até 20 s para 80% das chamadas e de até 300 s para as demais | E5 |
| | art. 16 | No máximo cinco níveis; humano e retorno de ligação informados no 1º nível | E3 |
| | arts. 18, 19 e 21 | Protocolo; gravação por 90 dias; resposta em 7 dias corridos | E6, E9 |
| | art. 24 | Revoga o Decreto 11.034/2022 | — |
| Decreto 11.034/2022 (revogado) [7b] | arts. 4º, 5º, 12 e 13 | Regia o SAC até a vigência do Decreto 13.135: 24h de acesso, mínimo de 8h de atendimento humano, protocolo e 7 dias para resposta | Referência histórica |
| Lei 13.460/2017 [19] | art. 1º, § 1º | Aplica-se à administração direta e indireta | Todas |
| | art. 5º, XIV | Linguagem simples | E3, E4, E6 |
| | art. 6º, III e VI | Acesso a dados pessoais e à situação de processos | E2, E4 |
| | art. 7º, §§ 2º a 4º | Carta de Serviços com etapas, prazo e previsão de tempo de espera; atualização periódica | E2, E5 |
| | arts. 10 e 16 | Manifestação à ouvidoria; resposta em 30 dias | E9 |
| | art. 23 | Avaliação anual e publicação de resultados | Suporte |
| Lei 14.129/2021 [21] | art. 2º, II; art. 3º, VII, XIII, XIV e XVI; art. 14 | Aplica-se a empresas públicas que prestam serviço público; linguagem clara; vedação de exigir prova já comprovada; interoperabilidade; direito ao atendimento presencial | E6, E7, suporte |
| LGPD (Lei 13.709/2018) [22] | art. 7º, III; art. 23; art. 26 | Tratamento e uso compartilhado de dados para política pública | E4, suporte |
| | art. 18 | Direitos do titular, entre eles acesso e correção | E2, E8 |
| | art. 24, par. ún. | Empresa pública que operacionaliza política pública recebe o tratamento de órgão público | E4 (Caixa) |

**Aplicabilidade do SAC à URA do seguro-desemprego: [INFERÊNCIA].** Os argumentos vão nos dois sentidos:
- **A favor:** a Caixa é instituição financeira regulada, e a URA é um canal telefônico de atendimento.
- **Contra:** no pagamento do seguro, a Caixa atua como agente de política pública (LGPD, art. 24, par. ún.; Res. 957, art. 64). Nessa função a relação é de serviço público (Lei 13.460), e não necessariamente de consumo.
- **Leitura prudente:** a Lei 13.460 se aplica com certeza. O Decreto 13.135 serve de parâmetro de qualidade, mas a obrigação depende de interpretação. Não localizei norma interna pública da Caixa sobre o roteiro do 0800 726 0207.

---

## (e) Lacunas e incertezas

1. **Menu atual da URA.** A única descrição ("opção 5", NIS e identificação positiva) é de 2018 [16]. Para confirmar: ligação de teste gravada em novembro de 2026.
2. **Tecnologia de voz.** Não há comunicado da Caixa sobre URA conversacional ou com IA. A busca só trouxe material genérico de fornecedores.
3. **Operador e contrato.** A CECOT 121/2026 tem objeto de "atendimento multimeios", com tratamento de ocorrências e transferência de conhecimento de TI, situação "Divulgada" e sem resultado (atualizada em 15/05/2026) [13]. Não está provado que ela cubra o 0800 726 0207. Para confirmar: pedido via LAI à Caixa.
4. **Tempos de espera e abandono.** Não localizei dado público. Os rankings do Banco Central sobre a Caixa não separam o seguro-desemprego.
5. **Vigência e alcance do Decreto 13.135/2026.** A data de vigência é cálculo meu (20 dias após o DOU de 13/10/2026). A aplicação ao canal do benefício é [INFERÊNCIA].
6. **Horários do atendimento humano da Caixa.** O dado (seg. a sex., 8h–21h; sáb., 10h–16h) vem do v3. A página da Caixa não abriu nesta data (erro de redirecionamento). Se o Decreto 13.135 se aplicar, esse horário estaria abaixo das 8h–20h nos sete dias [INFERÊNCIA].
7. **Texto da Res. 957.** O DOU não respondeu nesta data. Os arts. 20 a 25, 64 e 65 foram lidos na LegisWeb [2], que é fonte secundária, e devem ser reconferidos no DOU [1]. Os arts. 4º, 8º, 27, 28 e 40 já tinham sido conferidos no DOU no v3.
8. **Protocolo, música de espera, SMS e carta.** Nenhuma fonte pública descreve essas evidências físicas na URA da Caixa para o seguro-desemprego.
9. **Consulta da URA a dados do MTE.** Não sei se a URA lê só a base de pagamento da Caixa ou também o status de habilitação do MTE [INFERÊNCIA: só pagamento, pela FAQ [6]].
10. **Reclame Aqui e consumidor.gov.br.** As páginas do Reclame Aqui bloquearam a leitura automatizada (HTTP 403). Não há estatística específica do seguro-desemprego. Uso só a nota de 2023 [14] e o caso do TED [15].

---

## (f) Fontes

1. Res. CODEFAT 957/2022, DOU (arts. 4º, 8º, 27, 28, 40 conferidos no v3): https://www.in.gov.br/web/dou/-/resolucao-codefat-n-957-de-21-de-setembro-de-2022-431328890
2. Res. CODEFAT 957/2022, LegisWeb (arts. 8º, 12, 20 a 25, 64 e 65, lidos em 14/11/2026; secundária): https://www.legisweb.com.br/legislacao/?id=436595
3. Lei 7.998/1990: https://www.planalto.gov.br/ccivil_03/leis/l7998.htm
4. Caixa, Atendimento (horários; via v3): https://www.caixa.gov.br/atendimento/Paginas/default.aspx
5. Caixa, Libras por videochamada (resultado de busca; página com redirecionamento): https://www.caixa.gov.br/atendimento/libras/
6. Caixa, FAQ do Seguro-Desemprego (via v3 e resultado de busca): https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx
7. Caixa, app Benefícios Sociais: https://www.caixa.gov.br/atendimento/aplicativos/beneficios-sociais-caixa/Paginas/default.aspx
7b. Decreto 11.034/2022 (revogado): https://www.planalto.gov.br/ccivil_03/_Ato2019-2022/2022/Decreto/D11034.htm
8. Decreto 13.135/2026: https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2026/decreto/d13135.htm
9. MTE, Central Alô Trabalho 158: https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/inspecao-do-trabalho/acesso-a-informacao/central-alo-trabalho-158
10. gov.br, Cadastrar recurso relativo ao seguro-desemprego (modificada em 25/09/2026): https://www.gov.br/pt-br/servicos/cadastrar-recurso-relativo-ao-seguro-desemprego
11. gov.br, Perguntas frequentes do Seguro-Desemprego: https://www.gov.br/pt-br/temas/perguntas-frequentes-seguro-desemprego
12. TCU, Acórdão 1621/2026 (notícia): https://portal.tcu.gov.br/imprensa/noticias/tribunal-avalia-servico-digital-de-seguro-desemprego-para-trabalhadores-formais
13. PNCP, CECOT 121/2026 (API): https://pncp.gov.br/api/consulta/v1/orgaos/00360305000104/compras/2026/315
14. O Povo, "Usuários reclamam de atraso no seguro-desemprego" (19/05/2023): https://mais.opovo.com.br/jornal/economia/2023/05/19/usuarios-reclamam-de-atraso-no-seguro-desemprego.html
15. Seu Dinheiro/Estadão, falha no TED atrasa 45 mil parcelas (19/05/2023): https://www.seudinheiro.com/2023/economia/falha-do-banco-central-atrasa-mais-de-45-mil-parcelas-do-seguro-desemprego-veja-quando-os-beneficios-serao-liberados-lvit
16. Jornal Contábil (2018; secundária): https://jornalcontabil.com.br/noticia/seguro-desemprego-fgts-e-pis-tem-novas-datas-de-pagamento/
17. Agência Gov, canais do MTE (06/07/2026): https://agenciagov.ebc.com.br/noticias/202607/saiba-como-acessar-os-canais-de-atendimento-do-ministerio-do-trabalho-e-emprego
18. consumidor.gov.br, sobre o serviço: https://www.consumidor.gov.br/pages/conteudo/sobre-servico
19. Lei 13.460/2017: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2017/lei/l13460.htm
20. TCU, Acórdão 135/2024 (notícia): https://portal.tcu.gov.br/imprensa/noticias/inconsistencias-no-seguro-desemprego-causaram-prejuizo-a-administracao-publica
21. Lei 14.129/2021: https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2021/lei/l14129.htm
22. LGPD, Lei 13.709/2018: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm
