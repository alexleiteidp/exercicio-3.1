# Relatório do Assistente 1 — versão 3 (final)

**Service Blueprint AS-IS — Atendimento ao Seguro-Desemprego pela URA da Caixa (0800 726 0207)**

- **Assistente 1:** Claude Opus 5.5 (com busca na web)
- **Data:** 14/11/2026
- **Responde a:** `B_relatorio_auditoria_v2.md`
- **Base:** `B_relatorio_assistente_v2.md`, revisado só onde a auditoria v2 apontou problema.

**Convenções.** [INFERÊNCIA] marca dedução minha a partir de fonte citada. [NÃO CONFIRMADO] marca dado sem fonte primária localizada. "Não localizado" quer dizer que procurei e não achei. "Não verificado" vale para jurisprudência que não conferi em fonte primária. Os números entre colchetes remetem à seção (f).

**O que há de novo na verificação desta rodada (14/11/2026):**
- li o **Sumário Executivo oficial do TCU sobre o Acórdão 1.621/2026-Plenário** (PDF de 16 páginas) [42];
- reli no PDF oficial do Contrato 07/2026 os itens **TR 5.3.6.4, 5.3.7.1, 5.3.8.4, 5.3.17.1 e 5.3.23** [5];
- reli no PDF oficial da Res. 957 os **arts. 20, 21 e 65** [1];
- reabri a **página oficial da Central 158** [31];
- conferi na Lei 13.146/2015, no Planalto, os **arts. 3º, 9º e 63 a 73** [18];
- reabri a **notícia oficial do Acórdão 135/2024** [23];
- localizei a **origem provável do prazo de "dois anos" da FAQ**: Res. CODEFAT 392/2004, art. 15, § 4º [39].

**O que continua sem verificação:** os itens numerados do dispositivo do Acórdão 1.621/2026 (9.1, 9.2…). A pesquisa de jurisprudência do TCU (pesquisa.apps.tcu.gov.br) devolveu página sem conteúdo ao acesso automatizado.

---

## Registro de mudanças (v2 → v3)

Cada delta tem um gatilho na auditoria v2. Os gatilhos seguem a numeração dela: N1 a N10 (seção 2); "F__ (seção 1.2)" para falhas marcadas Parcial ou Não resolvida; FP__ (seção 3); 4.x (seção 4); 5.x (seção 5).

Status possíveis:
- **Resolvido**;
- **Resolvido em parte**: a correção foi feita, mas sobra um ponto, com o caminho para resolvê-lo;
- **Pendente**: depende de evidência que não é pública ou de ligação de teste; o caminho está indicado.

| Delta | Gatilho na auditoria v2 | O que mudou | Status |
|---|---|---|---|
| D01 | **N1** (premissa "não paga, logo não é consumo") | Retirei a premissa da v2. A seção d.2 foi refeita com **três relações**: União–Caixa (contrato administrativo); trabalhador–Administração (benefício de direito público); trabalhador–Caixa (execução do pagamento + relação bancária). A **remuneração indireta** (CDC, art. 3º, § 2º) entrou como argumento a favor do consumo na relação bancária. Ela tem amparo doutrinário em fontes secundárias; precedente do STJ **não verificado** em fonte primária e nenhum REsp citado. O inciso II do art. 1º, par. ún., do Decreto 13.135 (plataformas digitais) **não se estende automaticamente** à URA telefônica | Resolvido |
| D02 | **N2** (funções presumidas na matriz de canais) | A matriz Sim/Não foi trocada por **três categorias**: C = comprovado documentalmente; P = parcialmente demonstrado; N = não confirmado. Separei pagamento de consulta em agência e lotérica. Sine/SRTE e CAIXA Tem foram reclassificados pela fonte (b.2) | Resolvido |
| D03 | **N3** (Dataprev superatribuída) | b.1 foi refeita no formato sugerido. Habilitação: "Sistema Seguro-Desemprego". Emissão: MTE. Transmissão: MTE→Caixa. Retorno: Caixa→"DATAPREV/SEPRT" (TR 5.3.8.17). **Motor de regras: não determinado.** O resíduo (quem opera o motor) foi para a lacuna e.3 | Resolvido em parte (resíduo pendente: LAI ao MTE sobre o contrato MTE–Dataprev) |
| D04 | **N4** (FP28 exagerado) | FP28 reescrito com a redação sugerida pela auditoria, sem "atrasa o lote inteiro". A contingência por atraso de transmissão (TR 5.3.18.2) virou mecanismo separado: **FP28-B** | Resolvido |
| D05 | **N5** (recomendação do TCU tratada como prova de ausência) | FP19 e FP25 foram divididos em **"a" = insuficiência comprovada** (achados 2.2 e 2.4 do Sumário Executivo oficial [42]) e **"b" = ausência total = hipótese** | Resolvido |
| D06 | **N6** (conta localizada × conta aberta) | FP26 foi dividido. **FP26-A**: crédito em conta já existente localizada pelo agente pagador (Res. 957, art. 20, § 2º; TR 5.3.6.4). **FP26-B**: crédito em **Conta Poupança Social Digital aberta automaticamente** (TR 5.3.7.1; ordem de prioridade do TR 5.3.8.4) | Resolvido |
| D07 | **N7** (pagamento × recebimento) | Nova tabela de **cinco estados** em b.3: registrado como pago; creditado; disponibilizado em canal de saque; sacado; recebimento reconhecido. Acrescentei o achado oficial do TCU de que a integração com a Caixa "pode marcar parcelas como 'pagas' antes da efetivação do crédito" [42] | Resolvido |
| D08 | **N8** (60 × 67 dias) | Confronto literal. Res. 957: 67 dias **"a contar de sua disponibilização para saque"** (art. 21) e fechamento do lote em até 67 dias após a disponibilização (art. 65, § 1º) [1]. TR 5.3.17.1: lote fechado "até 60 (sessenta) dias **após o vencimento** das parcelas" [5]. Os marcos de início são diferentes e "vencimento" não é definido no trecho lido. A conciliação ficou registrada como hipótese, não como fato | **Pendente**: consulta formal (LAI/Fala.BR) ao MTE e à Caixa sobre o marco "vencimento" e o prazo que prevalece |
| D09 | **N9** (procedimento de reemissão) | FP8 e FP22 passaram a separar quatro perguntas abertas: formulário; serviço digital; órgão (MTE ou Caixa); controle de duplicidade e prazo. Só o prazo de 2 anos da emissão (art. 21, § 2º) e a legitimidade ("solicitação do beneficiário" ou decisão judicial) estão comprovados [1] | **Pendente**: LAI ao MTE pedindo o procedimento, o sistema e o prazo de reemissão; ligação de teste perguntando "como peço reemissão" |
| D10 | **N10** (TR 5.3.23.5 não explorado) | O TR 5.3.23 entrou em b.1, b.2, E6 e no novo **FP30**. A Caixa faz bloqueios preventivos (5.3.23.1), comunica ao MTE (5.3.23.2) e "se responsabilizará pelo atendimento a beneficiários que tenham seus benefícios eventualmente bloqueados" (5.3.23.5) [5]. A obrigação de atendimento existe; o canal não é especificado | **Pendente** (operacionalização): LAI à Caixa sobre os canais e o roteiro de atendimento a bloqueados; ligação de teste |
| D11 | **F1 (seção 1.2)** (TCU 1621 subutilizado) | A dependência da notícia especializada [22] foi substituída pelo **Sumário Executivo oficial do TCU** [42]. Seus achados 2.1 a 2.7 e a Tabela 2 (recomendações) foram incorporados a (a), (b) e (c), com dados como 479.226 recursos em 2025, 24% acima de 30 dias | Resolvido (numeração 9.x: ver D25) |
| D12 | **F2 (seção 1.2)** (Dataprev insuficientemente demonstrado) | Tratado junto com N3 (D03) | Resolvido em parte (mesmo resíduo de D03) |
| D13 | **F4 (seção 1.2)** (competências presumidas) | Tratado junto com N2 (D02) | Resolvido |
| D14 | **F7/F30 (seção 1.2)** (aplicabilidade do Decreto) | Tratados junto com N1 (D01). A conclusão mudou. **Na relação bancária** o Decreto tende a incidir, a depender do enquadramento do inciso I. **Na informação sobre o benefício** a incidência é incerta. A Lei 13.460 é o piso em ambas | Resolvido em parte (resíduo pendente: LAI ao Banco Central e à Caixa sobre o enquadramento no art. 1º, par. ún., I) |
| D15 | **F12 (seção 1.2)** (rastreabilidade dos 4 mil recursos) | Tratado junto com 4.5 (D28). Os dois números estão na notícia oficial do TCU [23], com trecho transcrito | Resolvido |
| D16 | **F14 (seção 1.2)** (reemissão) | Tratado junto com N9 (D09) | **Pendente** (LAI ao MTE) |
| D17 | **F20 (seção 1.2)** (atendimento humano) | Acrescentei a obrigação contratual do TR 5.3.23.5 (D10) e o achado oficial sobre a baixa resolutividade dos canais, incluindo o 158 [42]. Sistemas, permissões e roteiro do atendente do 0800 continuam sem fonte | **Pendente**: LAI à Caixa (perfis de acesso, roteiros, base de conhecimento); ligação de teste |
| D18 | **F21 (seção 1.2)** (acessibilidade telefônica) | A base legal foi especificada (ver D33). O TCU constatou fragilidades de acessibilidade **digital** (CTPS Digital e Emprega Brasil) [42], não telefônica. A acessibilidade da URA continua sem evidência direta | **Pendente**: ligação de teste com roteiro de acessibilidade; LAI à Caixa sobre alternativas para pessoas surdas ou com deficiência de fala no 0800 |
| D19 | **F22 (seção 1.2)** (consumidor × usuário de serviço público) | A matriz de escalonamento (d.3) foi refeita sobre as três relações de D01 | Resolvido |
| D20 | **F31 (seção 1.2)** (origem da divergência FAQ × Res. 957) | Origem provável documentada. A Res. CODEFAT 392/2004, art. 15, § 4º, previa recurso "no prazo de 2 (dois) anos, contados a partir da data de dispensa", e foi revogada pela Res. 467/2005 [39]. A FAQ gov.br [26] reproduz essa regra antiga. O texto da Res. 467/2005 não foi conferido | Resolvido em parte (resíduo pendente: manifestação ao MTE via Fala.BR pedindo correção da FAQ e indicação da base normativa) |
| D21 | **FP19 (seção 3)** (classificação incorreta) | Dividido. **FP19-A** (comprovado): mensagens genéricas, sem indicar a inconsistência, a base e a providência (achado 2.2) [42]. **FP19-B** (hipótese): ausência de qualquer retorno após regularização | Resolvido |
| D22 | **FP21 (seção 3)** (Parcial) | Reformulado com os cinco estados de D07 e o novo título de 5.1 (D29) | Resolvido |
| D23 | **FP25 (seção 3)** (Parcial) | Dividido. **FP25-A** (comprovado): modelo "entre e consulte", sem escolha de SMS ou e-mail (achado 2.4) [42]. **FP25-B** (hipótese): nenhuma comunicação proativa em nenhum canal, inclusive da Caixa | Resolvido |
| D24 | **FP23 (seção 3)** (quatro situações) | FP4/FP23 reformulado com as quatro situações da auditoria: sem indicador público; sem monitoramento; monitoramento interno não divulgado; monitoramento sem uso. Só a primeira está comprovada; o FP não afirma mais "abandono não monitorado" | Resolvido (qual das outras três vale: LAI à Caixa, já no plano) |
| D25 | **4.1** (inteiro teor e itens 9.1/9.2) | Usei a fonte oficial disponível, o Sumário Executivo do TCU [42], que identifica o "Acórdão 1.621/2026-TCU-Plenário", a determinação de integrar ao eSocial em 180 dias e seis blocos de recomendações. A **numeração dos itens 9.1 e 9.2 não foi conferida**: a pesquisa de jurisprudência do TCU não devolveu conteúdo ao acesso automatizado | **Pendente**: abrir o inteiro teor manualmente em pesquisa.apps.tcu.gov.br (TC 015.553/2025-6) ou pedir à Ouvidoria do TCU (0800 644 1500) |
| D26 | **4.3** (IMR) | O pedido do plano de coleta foi ampliado: arquivos mensais do IMR, resultados, descumprimentos, glosas, justificativas e relatórios do fiscal | **Pendente**: LAI ao MTE (gestão e fiscalização do Contrato 07/2026) |
| D27 | **4.4** (art. 27, § 4º como problema de UX) | A presunção de ciência em cinco dias passou a ser tratada também como falha de **efetividade da comunicação** (FP25-A, E2): notificação presumida não é notificação lida nem compreendida | Resolvido |
| D28 | **4.5** (localizar 4 mil recursos e 15 vezes) | Os dois trechos estão na notícia oficial do TCU sobre o Acórdão 135/2024 [23]: "média anual de aproximadamente quatro mil recursos referentes a situações em que já teria havido dois recursos" e "um único requerimento foi analisado 15 vezes". Reconferido em 14/11/2026 | Resolvido |
| D29 | **5.1** (título do FP21) | Novo título: "Registro de pagamento efetivado sem confirmação de recebimento pelo trabalhador" | Resolvido |
| D30 | **5.2** (condicionalidade do FP27) | FP27 agora diz que a Caixa "poderá executar" batimentos (TR 5.3.5), sem presumir validação idêntica de toda parcela | Resolvido |
| D31 | **5.3** (FP8: devolução ≠ reemissão negada) | FP8 separa a devolução financeira ao FAT (art. 21, caput) do direito de pedir reemissão (art. 21, § 2º) | Resolvido |
| D32 | **5.4** (158 gratuito só de fixo) | Reconfirmado na página oficial do MTE: "O telefonema é gratuito de qualquer telefone fixo; chamadas por celular serão cobradas"; horário de 7h às 19h; atendimento "automatizado ou por meio de um atendente" [31]. A página traz só a data de publicação, 14/10/2020; vigência atual [NÃO CONFIRMADO] | Resolvido |
| D33 | **5.5** (artigos da Lei 13.146) | Citados os dispositivos conferidos: art. 3º, I, III e V; art. 9º, II, III e V; art. 63; arts. 65 e 66; art. 69; art. 73. Informei que os arts. 67 e 68 tratam de radiodifusão e livros e **não se aplicam** à URA | Resolvido |

**Totais:** 33 deltas.
- **Resolvidos:** 21.
- **Resolvidos em parte:** 4 (D03, D12, D14, D20), cada um com resíduo e caminho indicados.
- **Pendentes:** 8 (D08, D09, D10, D16, D17, D18, D25, D26).

---

## (a) Sumário

- **Quatro papéis, duas relações jurídicas com o trabalhador.**
  - O CODEFAT normatiza.
  - O MTE gere o benefício, habilita, notifica, julga recurso e emite o DSD em lotes semanais (Res. 957, arts. 4º, 8º, 27, 28 e 65) [1].
  - A Caixa é o agente pagador (art. 64, § 1º) [1], contratada pelo MTE no **Contrato 07/2026**: inexigibilidade, R$ 2,25 por parcela paga, vigência de 16/04/2026 a 16/04/2031 [5].
  - Os arquivos diários de pagamento vão à "DATAPREV/SEPRT" (TR 5.3.8.17) [5]. Quem opera o motor de regras da habilitação **não foi determinado**.
- **O próprio TCU registrou a Caixa como fonte de status enganoso.** O Sumário Executivo oficial do Acórdão 1.621/2026 diz que a integração com a Caixa "pode marcar parcelas como 'pagas' antes da efetivação do crédito" [42]. É o achado oficial mais próximo do problema "não caiu" que a URA atende. Ainda assim, a auditoria avaliou o **serviço digital** (Portal Emprega Brasil e CTPS Digital), não o 0800 da Caixa.
- **O contrato não regula o telefone, mas obriga a Caixa a atender bloqueados.** O TR 5.3.23.5 diz que a Caixa "se responsabilizará pelo atendimento a beneficiários que tenham seus benefícios eventualmente bloqueados" [5]. A Caixa também faz bloqueios preventivos por indício de irregularidade (5.3.23.1). O canal desse atendimento não é especificado. É um elo provável com o 0800 [INFERÊNCIA], a confirmar.
- **"Não caiu" tem cinco estados de pagamento**, além dos eventos de concessão:
  - registrado como pago;
  - creditado;
  - disponibilizado em canal de saque;
  - sacado;
  - recebimento reconhecido pelo trabalhador.

  O contrato considera pago o benefício creditado em conta (TR 5.13; 5.3.23.9) [5]. O crédito pode cair em Conta Poupança Social Digital aberta automaticamente (TR 5.3.7.1) [5], que o trabalhador pode não conhecer.
- **O Decreto 13.135/2026 está vigente desde 02/11/2026** [9][11]. Ele não se aplica nem se afasta em bloco: depende da relação.
  - Na relação bancária entre o trabalhador e a Caixa, a remuneração indireta favorece a incidência do CDC.
  - No pagamento como execução de política pública, prevalecem a Lei 13.460 e a Res. 957.
  - O inciso II do decreto (plataformas digitais) não alcança automaticamente a URA.
- **Informação oficial contraditória, com origem identificada.** A FAQ gov.br fala em revisão em "dois anos contados da data de demissão" [26]. Essa era a regra da Res. 392/2004, revogada em 2005 [39]. A Res. 957 fixa 120 dias contados da notificação (art. 27, § 2º) [1].
- **Ainda falta evidência direta do canal:**
  - gravação da URA;
  - roteiros;
  - indicadores de espera e abandono;
  - contrato do operador;
  - IMR e fiscalização do Contrato 07/2026;
  - procedimento de reemissão;
  - dispositivo numerado do Acórdão 1.621/2026.

  A seção (e) indica o caminho de cada item (LAI ou ligação de teste).

---

## (b) Etapas da jornada

### b.1 Arquitetura institucional (N3, N10)

| Função | Quem | Base | Grau |
|---|---|---|---|
| Normatizar | CODEFAT | Lei 7.998, art. 19 [4]; Res. 957 [1] | Comprovado |
| Habilitar (processamento automático) | "Sistema Seguro-Desemprego" sob gestão do MTE | Res. 957, art. 4º, § 1º [1] | Comprovado quanto ao órgão gestor |
| Motor de regras e infraestrutura do sistema | **Não determinado** | O TCU 135/2024 trata da relação Strab–Dataprev [23], o que não prova a operação do motor | [NÃO CONFIRMADO] |
| Notificar e julgar recurso | MTE | Res. 957, arts. 8º, 27 e 28 [1] | Comprovado |
| Emitir os DSD em lotes semanais | MTE | Res. 957, art. 65 [1]; TR 5.3.6.2 [5] | Comprovado |
| Transmitir os lotes | MTE → Caixa | TR 5.3.6.2 e 5.3.18 a 5.3.20 [5] | Comprovado |
| Pagar: batimento, crédito, conta automática, canais de saque, contestação, devolução | Caixa | Res. 957, arts. 20 e 64, § 1º [1]; TR 5.3.5 a 5.3.17 [5] | Comprovado |
| Bloqueio preventivo e atendimento a bloqueados | Caixa (o MTE pode pedir desbloqueio) | TR 5.3.23.1 a 5.3.23.5 e 5.3.23.8 [5] | Comprovado o dever; canal não especificado |
| Retornar pagos e não pagos | Caixa → "DATAPREV/SEPRT" e sistema do MTE | TR 5.3.8.17 a 5.3.8.19 [5]; Res. 957, art. 65, § 4º [1] | Comprovado |
| Operar o 0800 726 0207 | Caixa; operador terceirizado desconhecido | FAQ Caixa via busca [27] | [NÃO CONFIRMADO] |
| Agente operador do programa | Caixa | Portaria Interministerial 70/2002 [8] | [NÃO CONFIRMADO no texto integral] |
| Fornecer dados de vínculo | Empregador (eSocial, Empregador Web) | Res. 957, arts. 4º e 40, § 1º [1]; TCU, achado 2.1 [42] | Comprovado |

**Repartição de risco.**
- A Caixa não responde por pagamentos "indevidos, recusados, estornados, suspensos, atrasados" que decorram de dado inconsistente do MTE (TR 5.3.6.8) [5].
- O MTE assume "total responsabilidade" pelos bloqueios e devoluções pedidos por ele (TR 5.3.23.8) [5].

Isso dá à Caixa base contratual para remeter ao MTE quem tem problema de dado. Mas o TR 5.3.23.5 a obriga a atender quem foi bloqueado. O transbordo (FP2) tem, portanto, um limite contratual que precisa ser testado.

### b.2 Matriz de competência por canal (N2)

**Legenda.**
- **C** = comprovado documentalmente: norma, contrato ou página oficial diz que o canal faz isso.
- **P** = parcialmente demonstrado: fonte secundária, trecho de busca, ou documento oficial que atribui a função à instituição sem nomear o canal.
- **N** = não confirmado: sem fonte. Inclui presunções de que o canal faz ou não faz.
- "—" = a função não é atribuída ao canal por nenhuma fonte, e nada indica que ele a exerça. Não é prova de que não exerça.

| Canal (operador) | Consultar situação da parcela | Ver motivo da decisão | Recorrer | Sacar / receber | Contestar saque | Pedir reemissão | Atender bloqueio (TR 5.3.23.5) | Fontes |
|---|---|---|---|---|---|---|---|---|
| URA 0800 726 0207 (Caixa) | P | N | — | — | N | N | N | FAQ Caixa via busca [27] |
| Atendente do 0800 (Caixa; operador desconhecido) | N | N | — | — | N | N | P (dever da Caixa; canal não nomeado) | TR 5.3.23.5 [5] |
| CAIXA Tem (Caixa) | P (saldo da conta digital) | — | — | P (movimentação da conta digital) | N | — | N | FAQ via busca [27]; TR 5.3.7.1 (a conta, não o app) [5] |
| App Benefícios Sociais (Caixa) | P | — | — | — | N | N | N | Página da Caixa [30]; FAQ via busca [27] |
| Agência Caixa | P | — | — | **C** (pagamento em canais) | P (ambiente da Caixa, sem nomear a agência) | P (a FAQ gov.br manda procurar a agência) | P | TR 5.3.8.4, 5.3.8.11, 5.3.8.14, 5.3.14.1 [5]; FAQ gov.br [26] |
| Lotérica / Caixa Aqui | N | — | — | **C** (pagamento em canais) | — | — | — | TR 5.3.8.4 [5] |
| CTPS Digital / gov.br (MTE) | **C** | **C** (existe a notificação; conteúdo insuficiente, achado 2.2) | **C** | — | — | N | — | Res. 957, arts. 8º, 27, § 1º, e 31 [1]; FAQ gov.br [26]; TCU [42] |
| Facilita (MTE) | N | N | **C** (complemento de parcelas, reembolso, parcela adicional) | — | — | N | — | TCU, achado 2.3 [42] |
| Central 158 (MTE) | P (orientação) | P (orientação) | P (agenda atendimento presencial) | — | — | — | — | Página oficial [31]; página de recurso [25]; TCU, achado 2.5 (baixa resolutividade) [42] |
| Sine / SRTE (MTE e rede Sine) | P | P | **C** (recurso presencial) | — | P (unidade do MTE, nas modalidades sem crédito em conta) | N | — | Res. 957, art. 27, § 1º [1]; TR 5.3.14.2 [5] |
| Banco destinatário (TED/PIX) | P (extrato) | — | — | **C** (crédito) | **C** (se o crédito não foi devolvido) | — | — | TR 5.3.14.1 [5] |

**Leitura.**
- Só os canais do MTE têm função **comprovada** de mostrar a decisão e receber recurso.
- Dos canais da Caixa, só os de **saque** (agência, lotérica, autoatendimento) têm função comprovada por contrato. A **consulta** pela URA e pelos apps está apenas parcialmente demonstrada.
- Reemissão não tem nenhum canal comprovado (FP8, FP22).
- Atendimento a bloqueados é dever da Caixa sem canal nomeado (FP30).

### b.3 Eventos do pagamento e estados de recebimento (N7, N8)

**Eventos.**

| # | Evento | Quem | Base | O que o cidadão vê | Falha possível |
|---|---|---|---|---|---|
| 1 | Requerimento | Trabalhador / MTE | Res. 957, arts. 5º e 12 [1] | Comprovante no gov.br | Fora do prazo |
| 2 | Habilitação automática e decisão | Sistema Seguro-Desemprego (MTE) | Art. 4º, § 1º; art. 8º [1] | Notificação no app | Dado do empregador (FP3); mensagem genérica (FP19-A) |
| 3 | Ciência presumida | MTE | Art. 27, § 4º: cinco dias após a disponibilização [1] | Nada, se não abrir o app | Prazo corre sem leitura (FP25-A) |
| 4 | Emissão do DSD em lote semanal | MTE | Art. 65 [1]; TR 5.3.6.2 [5] | Nada | Registro fora do lote |
| 5 | Transmissão e confirmação | MTE → Caixa | TR 5.3.18 a 5.3.20 [5] | Nada | Contingência (FP28-B); rejeição sem reprocessamento (FP28) |
| 6 | Batimento facultativo com CPF | Caixa ("poderá executar") | TR 5.3.5 e 5.3.5.2 [5] | Nada | Devolução por incompatibilidade (FP27) |
| 7 | Bloqueio preventivo (eventual) | Caixa; desbloqueio a pedido do MTE | TR 5.3.23.1 a 5.3.23.3 [5] | Parcela não sacável [INFERÊNCIA] | FP30 |
| 8 | Disponibilização | Caixa | TR 5.3.6.1: a partir da 1ª terça-feira após o lote [5] | Data no app | Atraso do lote |
| 9 | Crédito em conta (= pagamento para o contrato) | Caixa | Art. 20 e §§ 2º e 3º [1]; TR 5.13, 5.3.6.4, 5.3.7.1, 5.3.8.4 [5] | Saldo em conta informada, localizada ou aberta automaticamente | FP26-A, FP26-B |
| 10 | Devolução de TED/PIX e nova tentativa | Banco destinatário → Caixa | TR 5.3.6.5 [5] | Atraso | Ciclo de devoluções |
| 11 | Saque | Trabalhador | TR 5.3.8.12 e 5.3.8.14 [5] | Dinheiro | Saque por terceiro (FP21) |
| 12 | Retorno de pagos e não pagos | Caixa → DATAPREV/SEPRT e MTE | Art. 65, §§ 2º e 4º [1]; TR 5.3.8.17 a 5.3.8.19 [5] | Status no app | Status "pago" antes do crédito (FP13/14; achado 2.4 [42]) |
| 13 | Fim da disponibilidade; devolução ao FAT | Caixa | Art. 21, caput (67 dias da disponibilização); art. 65, §§ 1º e 3º [1]; TR 5.3.17.1 (60 dias após o "vencimento") [5] | Parcela some | FP8; divergência de prazos (N8) |
| 14 | Reemissão a pedido | Beneficiário pede; órgão e canal não localizados | Art. 21, § 2º: até 2 anos da emissão de cada parcela [1] | — | FP8, FP22 |

**Os cinco estados do recebimento.** O trabalhador que liga dizendo "não caiu" pode estar em qualquer um deles.

| Estado | Definição | Quem o registra | Fonte | Lacuna |
|---|---|---|---|---|
| 1. Registrado como pago | O sistema exibe "pago" | Sistema do MTE, a partir do retorno da Caixa | Art. 65, § 4º [1]; achado 2.4: pode ocorrer "antes da efetivação do crédito" [42] | Frequência não medida |
| 2. Creditado | O valor entrou em conta do titular | Caixa ou banco destinatário | TR 5.13 e 5.3.23.9 ("após o crédito os benefícios são considerados pagos") [5] | Conta pode ser desconhecida (FP26-B) |
| 3. Disponibilizado em canal de saque | Sem conta: parcela sacável em agência, lotérica ou autoatendimento | Caixa | TR 5.3.8.4 (5ª prioridade) [5]; art. 20, § 3º [1] | Prazo de 67 dias (art. 21) |
| 4. Sacado | O dinheiro saiu da conta ou do canal | Caixa ou banco | TR 5.3.8.12 a 5.3.8.14 [5] | Saque por terceiro |
| 5. Recebimento reconhecido | O trabalhador confirma que recebeu | Ninguém registra; só a contestação registra o não reconhecimento | Art. 20, § 5º (portaria não localizada) [1]; TR 5.3.14 [5] | Não há evento formal de "reconhecimento" [INFERÊNCIA] |

**Prazo de 60 × 67 dias (N8), pendente.**
- A Res. 957 conta 67 dias "a contar de sua disponibilização para saque" (arts. 21 e 65, § 1º) [1].
- O TR conta 60 dias "após o vencimento das parcelas" (5.3.17.1) [5]. "Vencimento" não está definido no trecho lido.

As duas regras podem ser compatíveis se o vencimento for posterior à disponibilização [INFERÊNCIA não verificada]. Não trato isso como fato. Resolver exige consulta formal ao MTE e à Caixa (e.4).

### b.4 Tabela de etapas (E1–E9)

A **Linha de Interação** passa entre "Ações do cidadão" e "Frontstage". A **Linha de Visibilidade** passa entre "Frontstage" e "Backstage": o que fica à direita dela o cidadão não vê. Nenhum tempo de espera telefônico tem fonte pública. Os prazos vêm de norma, contrato ou página oficial.

| # | Etapa | Evidências físicas | Ações do cidadão | Frontstage | ‖ Linha de Visibilidade ‖ Backstage | Processos de suporte |
|---|---|---|---|---|---|---|
| E1 | **Percebe que a parcela não caiu** | Extrato sem crédito; data prevista vista no app; possível Conta Poupança Social Digital desconhecida | Espera, confere o saldo, às vezes na conta errada | — (sem contato) | Batimento facultativo (TR 5.3.5); eventual bloqueio preventivo (TR 5.3.23.1); escolha da conta pela ordem do TR 5.3.8.4 [5] | Lote semanal do MTE (art. 65) [1]; disponibilização na 1ª terça-feira (TR 5.3.6.1); abertura automática de conta (TR 5.3.7.1) [5] |
| E2 | **Procura o motivo por conta própria** | CTPS Digital/gov.br ("Notificações") [26]; apps CAIXA Tem e Benefícios Sociais [27][30] | Abre os apps, compara, decide ligar | Apps do MTE (decisão) e da Caixa (situação financeira) | Sistema do MTE grava decisão e notificação; status "pago" pode vir antes do crédito (achado 2.4) [42] | Notificação só digital (art. 8º); ciência presumida em 5 dias (art. 27, § 4º) [1]: presunção processual, não prova de leitura (FP25-A). Mensagens genéricas (achado 2.2) [42] |
| E3 | **Liga para o 0800 726 0207 e ouve o menu** | Número 0800 726 0207 [27]; menu e mensagens [NÃO CONFIRMADO em 2026; registro de 2018 [36]] | Disca, ouve, escolhe | URA [NÃO CONFIRMADO em 2026] | Plataforma de URA e roteamento [INFERÊNCIA: padrão de contact center] | Operador e contrato do canal não localizados; Contrato 07/2026 sem cláusula de telefone [5] |
| E4 | **Identifica-se e ouve o status automático** | Dado digitado (CPF ou NIS) [NÃO CONFIRMADO] | Digita e confirma | **Leitura de status pela URA [não confirmado em 2026]** | Consulta à base de pagamento da Caixa [INFERÊNCIA] | Retorno de pagos e não pagos (art. 65, § 4º; TR 5.3.8.17) [1][5]; cinco estados de b.3 |
| E5 | **Pede atendente e espera** | Música ou mensagem de espera [NÃO CONFIRMADO] | Espera; pode desistir | Fila; horário humano informado pela Caixa [28] [NÃO CONFIRMADO em 2026] | Distribuição de chamadas [INFERÊNCIA] | Indicadores de espera e abandono: não localizados (FP4/FP23). Decreto 13.135, art. 15 (20 s para 80%), só como referência ou se incidir (d.2) [9] |
| E6 | **Fala com o atendente** | Voz do atendente; protocolo [NÃO CONFIRMADO] | Explica, informa dados | Atendente Caixa; Libras por videochamada, canal à parte [29] | Sistemas e permissões do atendente [NÃO CONFIRMADO] | Dever de atender bloqueados (TR 5.3.23.5); isenção por dado do MTE (TR 5.3.6.8) [5] |
| E7 | **É encaminhado a outro canal** | Indicação de app, site, agência ou 158. O 158 é gratuito de fixo, cobrado de celular, das 7h às 19h [31] | Desliga e procura outro canal | Fala do atendente ou da URA | Transferência direta ao 158: não documentada | Achado 2.5: cidadão "reencaminhado entre múltiplos pontos de contato", inclusive agências da Caixa [42] |
| E8 | **Resolve (ou tenta) no canal certo** | Notificação com motivo; recurso com 500 caracteres, anexos de 1 MB, protocolo antes dos documentos (achado 2.3) [42] | Recorre em até 120 dias da notificação; corrige dados; contesta saque; pede reemissão | gov.br, CTPS Digital, Facilita, Sine/SRTE [25][42]; unidade do MTE (TR 5.3.14.2) [5] | Análise do recurso pelo MTE em instância única (art. 28) [1]; em 2025, 24% dos 479.226 recursos passaram de 30 dias [42]; contestação analisada pela Caixa (TR 5.3.14.4) [5] | Arts. 27 a 31 [1]; Lei 9.784, art. 59, §§ 1º e 2º [14]; reemissão em até 2 anos (art. 21, § 2º), procedimento não localizado |
| E9 | **Recebe, desiste ou reclama** | Crédito ou saque; protocolo de reclamação | Saca, abandona ou reclama | SAC e Ouvidoria Caixa; consumidor.gov.br; Fala.BR | Tratamento da manifestação | Ouvidoria pública: 30 dias (Lei 13.460, art. 16) [15]; satisfação de 30,2% com a ouvidoria do MTE em seguro-desemprego, segundo o Painel Resolveu? citado pelo TCU [42]; Res. CMN 4.860 [38]; Decreto 13.135, art. 21, na relação bancária (d.2) [9] |

**Notas.**
- E3 a E6 formam o "momento URA".
- O ponto de virada é E6: ali se descobre se o caso é de **pagamento ou bloqueio** (Caixa, inclusive pelo TR 5.3.23.5) ou de **concessão e dado** (MTE).
- A leitura de status pela URA em E4 continua [não confirmado em 2026].

---

## (c) Fail points revisados

**Domínios:**
- **SD:** serviço digital e canais do MTE;
- **TEL:** URA e atendente do 0800 da Caixa;
- **PAG:** retaguarda de pagamento;
- **INF:** informação oficial.

### c.1 Comprovado (fonte oficial descreve a falha)

| # | Falha | Etapa | Domínio | Evidência | Quem responde |
|---|---|---|---|---|---|
| FP2 | **Transbordo em cadeia** entre canais | E7 | SD (comprovado); TEL (hipótese) | Achado 2.5: baixa resolutividade do 158 e dos meios digitais; cidadão reencaminhado entre aplicativo, portal, telefone, ouvidoria, Sine e "agências da Caixa" [42] | MTE; Caixa |
| FP3 | **Dado do empregador em dois sistemas** gera bloqueio e indeferimento | Antes de E1; E2 | SD / PAG | Achado 2.1; determinação de integrar ao eSocial em 180 dias [42][20] | MTE; empregador |
| FP5 | **Recurso lento e pouco previsível** | E8 | SD | Achado 2.6: 479.226 recursos analisados em 2025, 24% (113.809) acima de 30 dias; sem prioridades legais automatizadas [42]. TCU 135/2024: sem 2ª instância; recursos ilimitados; "aproximadamente quatro mil" por ano; requerimento "analisado 15 vezes" [23] | MTE |
| FP6 | **Informação oficial contraditória sobre prazo** | E2, E8 | INF | FAQ gov.br: "dois anos contados da data de demissão" [26]; origem provável: Res. 392/2004, art. 15, § 4º, revogada [39]; Res. 957, art. 27, § 2º: 120 dias da notificação [1] | MTE (Lei 13.460, art. 7º) [15] |
| FP7 | **Falha de liquidação financeira** (evento único) | E1–E4 | PAG | Maio/2023: 45.335 parcelas por TED atrasadas (fonte jornalística) [35]. Recorrência não medida | Caixa; BC; MTE |
| FP10 | **Pagamentos indevidos e governança** | Suporte | PAG | TCU 135/2024: mais de 300 mil solicitações inconsistentes; indícios de R$ 147 milhões e R$ 544 mil [23] | MTE |
| FP13/14 | **Status exibido diverge do pagamento real** | E2, E4 | SD (comprovado); TEL (hipótese) | Achado 2.4: a integração com a Caixa "pode marcar parcelas como 'pagas' antes da efetivação do crédito" [42] | MTE; Caixa |
| FP19-A | **Mensagem de decisão insuficiente**: não indica a inconsistência, a base nem a providência | E2, E8 | SD | Achado 2.2: mensagens "genéricas e pouco orientadoras"; 28% dos trabalhadores e 31% dos atendentes discordam que expliquem o problema [42] | MTE |
| FP20 | **Recurso com barreiras técnicas** | E8 | SD | Achado 2.3: 500 caracteres; 1 MB por arquivo; protocolo antes dos documentos; Facilita mal sinalizado [42] | MTE |
| FP25-A | **Comunicação reativa ("entre e consulte") e ciência presumida** | E2, E9 | SD | Achado 2.4: sem aviso sistemático de mudança de status, sem escolha de SMS ou e-mail [42]; art. 27, § 4º presume ciência em cinco dias [1]. O cidadão pode perder prazo sem ter lido a notificação (efetividade, não só prazo) | MTE |

### c.2 Mecanismo comprovado em norma ou contrato; efeito a medir

| # | Falha | Etapa | Domínio | Mecanismo (fonte) | O que falta medir | Quem responde |
|---|---|---|---|---|---|---|
| FP8 | **Parcela não sacada é devolvida ao FAT; a reemissão é um evento separado, sem procedimento localizado** | E1, E8 | PAG / INF | Devolução: art. 21, caput, e art. 65, § 3º [1]; TR 5.3.17.1 [5]. Reemissão: art. 21, § 2º, a pedido do beneficiário ou por decisão judicial, em até 2 anos da emissão [1]. Devolução não é reemissão negada | Volume de devoluções e de reemissões; canal; prazo | MTE; Caixa |
| FP21 | **Registro de pagamento efetivado sem confirmação de recebimento pelo trabalhador** | E4, E9 | PAG | O contrato considera pago o creditado (TR 5.13; 5.3.23.9) [5]; não há evento de "recebimento reconhecido" (b.3). Contestação em três destinos: Caixa, banco destinatário, unidade do MTE (TR 5.3.14.1 e 5.3.14.2) [5]; art. 20, § 5º, com portaria não localizada [1] | Volume e prazo das contestações; quantos "pagos" estão nos estados 2 a 4 sem saque | Caixa; MTE; banco destinatário |
| FP26-A | **Crédito em conta já existente localizada pela Caixa**, diferente da informada | E1, E4 | PAG | Art. 20, § 2º [1]; TR 5.3.6.4 (conta "localizada mediante batimento de dados cadastrais") e 5.3.8.4, 2ª e 3ª prioridades [5] | Quantos créditos vão para conta não indicada | Caixa |
| FP26-B | **Crédito em Conta Poupança Social Digital aberta automaticamente**, que o trabalhador pode não saber que existe | E1, E4 | PAG | TR 5.3.7.1 (Lei 14.075/2020) e 5.3.8.4, 4ª prioridade [5] | Quantas contas abertas; quantas sem acesso; ligações geradas | Caixa |
| FP27 | **Parcela devolvida por incompatibilidade no batimento de CPF**, quando o batimento é feito | E1 | PAG | A Caixa "poderá executar batimentos" com primeiro nome e data de nascimento (TR 5.3.5); devolução se incompatível ou CPF cancelado ou nulo (5.3.5.2) [5]. Não há prova de que toda parcela passe pelo mesmo batimento | Frequência e critérios de aplicação | MTE (dado); Caixa |
| FP28 | **Rejeição de arquivo de pagamento, sem possibilidade de reprocessamento, exigindo regularização e novo procedimento de transmissão, com potencial atraso na disponibilização das parcelas** | E1 | PAG | TR 5.3.20 [5] | Frequência; atraso em dias | MTE; Caixa |
| FP28-B | **Atraso na transmissão aciona procedimento de contingência** | E1 | PAG | TR 5.3.18.2 [5] | Frequência; efeito na data de disponibilização | MTE; Caixa |
| FP30 | **Bloqueio preventivo pela Caixa, com dever de atendimento sem canal definido** | E1, E6 | PAG / TEL | Bloqueio por indício de irregularidade (TR 5.3.23.1); comunicação ao MTE (5.3.23.2); desbloqueio a pedido do MTE (5.3.23.3); dever de atender bloqueados (5.3.23.5) [5] | Volume de bloqueios; canal e roteiro do atendimento; se a URA informa o bloqueio | Caixa; MTE |

### c.3 Hipóteses a testar (sem evidência direta)

| # | Falha | Etapa | Domínio | Por que é plausível | Como testar |
|---|---|---|---|---|---|
| FP1 | **URA não explica o motivo** do bloqueio ou indeferimento | E4, E6 | TEL | Motivo e resultado do recurso ficam em canais do MTE (arts. 8º e 31) [1] | Ligação de teste com CPF próprio ou de titular que consinta |
| FP4/FP23 | **Abandono na fila**, em uma de quatro situações: (i) sem indicador público, **comprovado**; (ii) sem monitoramento; (iii) monitoramento interno não divulgado; (iv) monitoramento sem uso para melhoria | E5 | TEL | Nenhum dado público; o achado 2.5 do TCU fala em ligações que "caem após longos períodos de espera", mas no **158** [42] | LAI à Caixa: série mensal de espera e abandono, uso gerencial, cláusulas do contrato do operador |
| FP9 | **Horários e custos desalinhados** entre canais | E5, E7 | TEL / SD | 158: gratuito só de fixo, das 7h às 19h [31] (confirmado). Horário humano da Caixa: [NÃO CONFIRMADO em 2026] [28] | Reconferir a página da Caixa; ligação fora de horário |
| FP11 | **URA indisponível ou sem acesso à base de pagamento** | E3, E4 | TEL | Depende de integração não documentada | Ligações em dias e horários variados; LAI sobre incidentes |
| FP12 | **Falha de identificação por CPF ou NIS** | E4 | TEL | Migração para CPF como identificador (TR 5.3.5.3) [5] | Ligação de teste |
| FP15 | **Atendente sem acesso à decisão do MTE** | E6 | TEL | Decisão em sistema do MTE; a Caixa recebe só lotes [INFERÊNCIA] | LAI (perfis de acesso) |
| FP16 | **Atendimento sem protocolo rastreável** | E6 | TEL | Sem documento público | Pedir protocolo na ligação |
| FP17 | **Transferência sem histórico** | E6, E7 | TEL | Sem integração documentada 0800–158 | Ligação de teste; LAI a ambos |
| FP18 | **Encaminhamento a canal sem competência** | E7 | TEL / SD | Matriz b.2: competências que não se sobrepõem | Ligação com cenários (reemissão, contestação, bloqueio) |
| FP19-B | **Ausência total de retorno** após regularização de dado | E8 | SD | Recomendação do TCU de informar órgão, reanálise e prazo [42]; não prova ausência absoluta | Teste com caso real; LAI |
| FP22 | **Reemissão sem controle de duplicidade** | E8 | PAG | Procedimento não localizado (N9) | LAI ao MTE |
| FP24 | **Protocolo da Caixa não se liga à demanda no MTE** | E6, E7 | TEL / SD | O Portal de Demandas é entre instituições (TR 5.3.22) [5] | LAI a ambos |
| FP25-B | **Nenhuma comunicação proativa em nenhum canal**, inclusive da Caixa | E2, E9 | SD / TEL | O TCU descreve o modelo como "predominantemente" reativo [42], o que admite exceções | Teste com caso real; LAI à Caixa sobre SMS e push no CAIXA Tem |
| FP31 | **URA sem alternativa acessível** para pessoas surdas ou com deficiência de fala | E3–E6 | TEL | A Caixa tem Libras por videochamada [29], mas em canal à parte; a ligação com a URA não foi testada. O TCU achou barreiras de acessibilidade só no digital [42] | Ligação de teste; LAI à Caixa |

---

## (d) Normativos

### d.1 Tabela

| Norma | Artigo | O que exige ou prevê | Etapa |
|---|---|---|---|
| Constituição [40] | art. 7º, II; art. 201, III | Seguro-desemprego como direito; proteção ao desemprego involuntário | Todas |
| Lei 7.998/1990 [4] | arts. 3º, 6º a 8º; 15; 19 | Requisitos; requerimento; suspensão e cancelamento; pagamento por banco oficial federal; CODEFAT | E2, suporte |
| Res. CODEFAT 957/2022 [1] | art. 4º, §§ 1º e 2º | Habilitação automática; recurso quando a inconsistência impede a habilitação | E2 |
| | art. 8º | Notificação exclusivamente digital, com anuência | E2 |
| | art. 12 | 1ª parcela 30 dias após o requerimento; as demais a cada 30 dias | E1 |
| | art. 20, §§ 1º a 5º | Crédito em conta "sem ônus para o trabalhador"; conta localizada; outras formas; guarda por 5 anos; contestação do recebimento por portaria (não localizada) | E1, E4, E8 |
| | art. 21, §§ 1º e 2º | 67 dias "a contar de sua disponibilização para saque"; devolução ao FAT; retenção excepcional; reemissão a pedido em até 2 anos da emissão | E1, E8 |
| | art. 27, §§ 1º a 7º; arts. 28 a 31 | Recurso digital ou presencial; 120 dias da notificação; ciência presumida em 5 dias; instância única; resultado no gov.br e na CTPS Digital | E2, E8 |
| | arts. 64, § 1º; 65, §§ 1º a 4º; 66 | Caixa como agente pagador; lotes semanais; fechamento em até 67 dias da disponibilização; restituição; retorno ao sistema; tarifa por DSD pago | Suporte |
| Res. CODEFAT 392/2004 (revogada) [39] | art. 15, § 4º | Recurso em 2 anos da dispensa: origem provável do texto da FAQ | INF |
| Contrato MTE–Caixa 07/2026 e TR [5] | 5.3.5; 5.3.6; 5.3.7.1; 5.3.8; 5.3.14 a 5.3.22; **5.3.23**; 5.13; 7.1 e Anexo V (IMR); 10.5 | Batimento facultativo; disponibilização; conta automática; ordem de prioridade; contestação; devolução; fechamento em 60 dias do vencimento; arquivos; **bloqueio preventivo e dever de atender bloqueados**; pagamento = crédito; medição de resultado; transparência das suboperações | E1, E4, E6, E8, suporte |
| Lei 14.133/2021 | art. 74, I | Inexigibilidade, base da contratação da Caixa (conforme o próprio contrato) [5] | Suporte |
| Decreto 13.135/2026 [9] | art. 1º, caput, e par. ún., I e II | Regulamenta o CDC; SAC "nas relações de consumo". (I) fornecedores regulados pelo Executivo federal que se enquadrem nos critérios do regulador; (II) serviços financeiros, de pagamento ou de crédito **por plataformas digitais** supervisionados pelo BC | d.2 |
| | arts. 13 a 16; 18; 21 | Níveis do menu; telefone obrigatório; humano das 8h às 20h; 20 s para 80%; exceção do art. 15, § 1º; protocolo; resposta em 7 dias | E3–E6, E9 (se incidir) |
| CDC [13] | art. 3º, § 2º; art. 22 | Serviço "mediante remuneração", inclusive bancário; serviço público adequado | d.2 |
| Lei 9.784/1999 [14] | art. 49; art. 59, §§ 1º e 2º | Decisão em 30 dias; recurso em 30 dias, prorrogáveis | E8 |
| Lei 13.460/2017 [15] | arts. 1º; 5º, XIV; 6º; 7º; 16; 23 | Administração direta e indireta; linguagem simples; acesso à situação; Carta de Serviços; ouvidoria em 30 dias; avaliação | Todas |
| Lei 14.129/2021 [16] | art. 3º | Princípios do governo digital | E6, E7 |
| LGPD [17] | arts. 7º, III; 18; 23; 24, par. ún. | Tratamento para política pública; direitos do titular; empresa pública que operacionaliza política pública tratada como órgão público | E4, suporte |
| **Lei 13.146/2015** [18] | **art. 3º, I, III e V** | Definições de acessibilidade, tecnologia assistiva e comunicação (inclui Libras, legendas, meios alternativos) | E3–E6 |
| | **art. 9º, II, III e V** | Atendimento prioritário em "todas as instituições e serviços de atendimento ao público"; recursos humanos e tecnológicos que garantam igualdade de condições; recursos de comunicação acessíveis | E5, E6 |
| | **art. 63** | Acessibilidade obrigatória nos sítios da internet de empresas e órgãos de governo | E2 |
| | **arts. 65 e 66** | Prestadoras de telecomunicações devem garantir acesso pleno; poder público incentiva aparelhos acessíveis. Atingem a operadora, não diretamente a Caixa [INFERÊNCIA] | E3 |
| | **art. 69** | Informação correta e clara sobre produtos e serviços ao consumidor com deficiência: relação bancária | E4, E6 |
| | **art. 73** | Capacitação de intérpretes de Libras e profissionais afins (dever do poder público) | Suporte |
| | arts. 67 e 68 | Radiodifusão e livros: **não aplicáveis** à URA. Arts. 70 a 72 não conferidos nesta rodada | — |
| Res. CMN 4.860/2020 [38]; 4.949/2021 [41] | — | Ouvidoria e relacionamento com clientes | E9 |

### d.2 Decreto 13.135/2026 e a URA: as três relações (N1, F7/F30)

**Correção da v2.** A v2 concluiu que, como o trabalhador não paga, não há consumo. Essa premissa não se sustenta sozinha. O art. 3º, § 2º, do CDC exige remuneração, mas a doutrina admite a **remuneração indireta**: o fornecedor ganha por outra via, como publicidade, captação ou venda cruzada. Fontes secundárias atribuem essa leitura ao STJ e a Cláudia Lima Marques [43]. **Não verifiquei precedente do STJ em fonte primária e não cito número de REsp nem ementa.** A conclusão agora é por relação.

**Relação 1: União (MTE)–Caixa.**
- **Natureza:** contrato administrativo de prestação de serviços de pagamento, por inexigibilidade (art. 74, I, Lei 14.133), a R$ 2,25 por parcela paga [5].
- **Regime:** Lei 14.133, Contrato 07/2026, TR, IMR e Res. 957, arts. 64 a 66 [1][5].
- **CDC:** não se aplica. A União é contratante, não consumidora.
- **Efeito no blueprint:** a qualidade do atendimento ao beneficiário só é exigível da Caixa pelo MTE se estiver no contrato. Nele há o dever de atender bloqueados (TR 5.3.23.5), mas nenhum nível de serviço telefônico.

**Relação 2: trabalhador–Administração (MTE/CODEFAT).**
- **Natureza:** direito social (CF, art. 7º, II) concedido por ato administrativo. O benefício não é serviço remunerado pelo trabalhador nem atividade de mercado.
- **Regime:**
  - Lei 7.998 e Res. 957;
  - Lei 9.784 (processo e recurso);
  - Lei 13.460 (direitos do usuário);
  - Lei 14.129 (governo digital);
  - LGPD.
- **CDC e Decreto 13.135:** não incidem nessa relação [INFERÊNCIA]. O art. 22 do CDC fala de serviço público prestado por órgão ou concessionária e não converte a concessão de benefício em relação de consumo.
- **Efeito no blueprint:** recurso, motivo, notificação e prazo seguem a Res. 957 e a Lei 9.784. O 158, o Sine e o gov.br seguem a Lei 13.460.

**Relação 3: trabalhador–Caixa.** Tem duas camadas:
- **(3a) Execução do pagamento como contratada da União.** Inclui informar se a parcela foi liberada, por que não caiu, bloqueio e reemissão.
  - A Caixa age em nome da política pública. É empresa pública, sujeita à Lei 13.460 (art. 1º) [15], e tratada como órgão público para a LGPD quando operacionaliza política pública (art. 24, par. ún.) [17].
  - A incidência do CDC aqui é **discutível** [INFERÊNCIA]. Não há prestação bancária ao trabalhador nessa camada, e a remuneração da Caixa vem da União. Mesmo pela tese da remuneração indireta, faltaria demonstrar a vantagem econômica da Caixa junto ao trabalhador nessa camada. Não localizei fonte que o faça.
- **(3b) Relação bancária.** Inclui a conta onde o crédito cai (inclusive a Poupança Social Digital aberta automaticamente, TR 5.3.7.1), cartão, senha, saque, CAIXA Tem e contestação de saque em conta Caixa.
  - Aqui há **relação de consumo**. Há serviço bancário (art. 3º, § 2º, CDC). A gratuidade da conta para o trabalhador não afasta o consumo, pela tese da remuneração indireta: a Caixa capta saldo e relacionamento [INFERÊNCIA com amparo doutrinário secundário [43]].
  - A aplicação do CDC às instituições financeiras é tida como pacífica. O enunciado da súmula do STJ **não foi verificado** nesta rodada.

**Incidência do Decreto 13.135.**
- **Inciso II** (plataformas digitais de serviços financeiros supervisionados pelo BC): pode alcançar o **CAIXA Tem e os apps** na camada 3b. **Não se estende automaticamente à URA**, que é canal telefônico, não plataforma digital. O inciso trata de serviços prestados por meio de plataformas digitais (paráfrase; ver texto em [9]).
- **Inciso I** (fornecedores regulados pelo Executivo federal que se enquadrem nos critérios do regulador): é a via provável para a Caixa como banco. **Não localizei** ato do CMN ou do BC que fixe esses critérios. Fica pendente (e.4).
- **A URA 0800 726 0207 atende às camadas 3a e 3b no mesmo número.** Leitura proposta:
  - (i) nas demandas bancárias (3b), as regras de SAC do decreto tendem a ser exigíveis se a Caixa se enquadrar no inciso I;
  - (ii) nas demandas de benefício (3a), o decreto serve como **referência de qualidade**, e o piso exigível é a Lei 13.460;
  - (iii) mesmo onde incidir, o art. 15, § 1º, admite regra específica do regulador.

**Consequência para o blueprint.** Em E3 a E6, os parâmetros do decreto aparecem com a nota "exigível na relação bancária, se enquadrada (inciso I); referência nas demandas de benefício". Isso substitui a nota da v2, "incidência incerta para todo o canal".

### d.3 Matriz de escalonamento por relação (F22)

| Demanda | Relação | Primeiro canal | Escalonamento | Prazo | Regime |
|---|---|---|---|---|---|
| Concessão, motivo, valor, número de parcelas | 2 | gov.br/CTPS Digital; 158; Sine | Recurso (art. 27); Ouvidoria MTE (Fala.BR) | Recurso: 30 dias (Lei 9.784, art. 59, § 1º) [14]; ouvidoria: 30 dias (Lei 13.460, art. 16) [15] | Direito público |
| Recurso de complemento, reembolso, parcela adicional | 2 | Facilita [42] | Ouvidoria MTE | Idem | Direito público |
| Parcela liberada e não creditada; bloqueio preventivo; devolução; reemissão | 3a (Caixa) e 2 (MTE, reemissão e desbloqueio) | Caixa (0800, agência); MTE | Ouvidoria Caixa; Fala.BR | Não localizado | Execução de política pública; Lei 13.460 |
| Saque não reconhecido | 3a/3b | Caixa (conta Caixa); banco destinatário; unidade do MTE | Análise da Caixa (TR 5.3.14.4) | Lei 9.784 (TR 5.3.14.11) [5] | Misto |
| Conta, cartão, senha, CAIXA Tem | 3b | SAC Caixa | Ouvidoria Caixa (Res. CMN 4.860) [38]; consumidor.gov.br [37]; BC | Decreto 13.135, art. 21 (7 dias), se enquadrada [9] | Consumo |
| Qualidade do atendimento do 0800 | 3a/3b | Ouvidoria Caixa | Fala.BR | 30 dias (Lei 13.460, art. 16) [15] | Serviço público e consumo |

---

## (e) Lacunas e plano de coleta de evidências

**e.1 Lacunas que permanecem**
1. Menu, mensagens, identificação e leitura de status atuais da URA (E3, E4).
2. Operador, contrato e níveis de serviço do 0800.
3. Quem opera o motor de regras da habilitação (N3).
4. Marco "vencimento" do TR 5.3.17.1 frente aos 67 dias da Res. 957 (N8).
5. Procedimento de reemissão: formulário, canal, órgão, controle de duplicidade, prazo (N9, F14).
6. Canal e roteiro do atendimento a bloqueados, previsto no TR 5.3.23.5 (N10).
7. Sistemas, permissões e roteiro do atendente (F20).
8. Acessibilidade da URA (F21).
9. Itens numerados do dispositivo do Acórdão 1.621/2026 (4.1).
10. Dados do IMR e da fiscalização do Contrato 07/2026 (4.3).
11. Enquadramento da Caixa no Decreto 13.135, art. 1º, par. ún., I.
12. Portaria do art. 20, § 5º, da Res. 957 (contestação), não localizada.
13. Texto da Res. 467/2005 e da Portaria Interministerial 70/2002.

**e.2 Plano de coleta**

| Evidência | Situação | Caminho |
|---|---|---|
| Inteiro teor e dispositivo do Acórdão 1.621/2026 (TC 015.553/2025-6) | Público, não obtido por acesso automatizado | Abrir manualmente em pesquisa.apps.tcu.gov.br; ou Ouvidoria do TCU (0800 644 1500) |
| IMR: arquivos mensais, resultados, descumprimentos, glosas, justificativas, relatórios do fiscal | Exige LAI | Fala.BR ao MTE, citando Contrato 07/2026, item 7.1 e Anexo V |
| Procedimento de reemissão e portaria do art. 20, § 5º | Exige LAI | Fala.BR ao MTE |
| Definição de "vencimento" (TR 5.3.17.1) e prazo que prevalece | Exige consulta formal | Fala.BR ao MTE e LAI à Caixa |
| Canal e roteiro de atendimento a bloqueados; volume de bloqueios preventivos | Exige LAI | LAI à Caixa; ao MTE, as comunicações do TR 5.3.23.2 |
| Contrato do operador do 0800; níveis de serviço; espera e abandono; uso gerencial (FP4/FP23) | Público em parte (licitacoes.caixa.gov.br, cláusula 10.5) [5]; resto via LAI | Pesquisa no portal; LAI à Caixa |
| Perfis de acesso, roteiros e base de conhecimento do atendente | Exige LAI (pode haver negativa) | LAI à Caixa |
| Contrato MTE–Dataprev e papel no motor de regras | Exige LAI | Fala.BR ao MTE |
| Enquadramento no Decreto 13.135, inciso I | Exige consulta | LAI ao BC e à Caixa |
| Correção da FAQ (dois anos) | Manifestação | Fala.BR ao MTE (Lei 13.460, art. 7º) |
| Menu, status lido pela URA, tempo até o humano, protocolo, acessibilidade, roteiros de reemissão, contestação e bloqueio | **Exige ligação de teste** | Roteiro abaixo |

**e.3 Roteiro da ligação de teste.**
- Fazer no mínimo seis ligações em dias e horários diferentes, inclusive sábado e depois das 20h. Gravar com aviso e usar só o CPF do pesquisador ou de titular que consinta por escrito.
- Registrar:
  - opções e número de níveis até o seguro-desemprego;
  - se o humano é oferecido em todos os níveis;
  - dados pedidos para identificação;
  - o que a URA lê sobre a parcela (E4);
  - tempo até o atendente;
  - protocolo;
  - respostas a quatro perguntas fixas: "minha parcela está bloqueada?", "como peço reemissão?", "como contesto um saque que não fiz?", "onde está o dinheiro se aparece pago?";
  - para onde o atendente encaminha;
  - existência de alternativa para pessoa surda ou com deficiência de fala;
  - informação sobre custo da ligação e horário.

---

## (f) Fontes

1. Res. CODEFAT 957/2022, texto revisado, Portal do FAT (PDF lido; arts. 20, 21 e 65 relidos em 14/11/2026): https://portalfat.trabalho.gov.br/wp-content/uploads/2026/09/Resolucao-no-957-de-21-de-setembro-de-2022-Revisao-do-SD.pdf
2. Res. CODEFAT 957/2022, DOU (não respondeu): https://www.in.gov.br/web/dou/-/resolucao-codefat-n-957-de-21-de-setembro-de-2022-431328890
3. Portal do FAT, normas do seguro-desemprego: https://portalfat.mte.gov.br/resolucoes-2/resolucoes-por-assunto/seguro-desemprego/
4. Lei 7.998/1990: https://www.planalto.gov.br/ccivil_03/leis/l7998.htm
5. MTE, Contrato 07/2026 MTE–Caixa, com Termo de Referência (PDF; TR 5.3.6.4, 5.3.7.1, 5.3.8.4, 5.3.17.1 e 5.3.23 relidos em 14/11/2026): https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/licitacoes-e-contratos/pca/072026completo.pdf
6. PNCP, registro do Contrato 07/2026: https://pncp.gov.br/app/contratos/23612685000122/2026/000012
7. MTE, 8º Termo de Apostilamento ao Contrato 11/2021: https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/licitacoes-e-contratos/contratos/8Termo_de_Apostilamento.pdf
8. Portaria Interministerial MTE/MF 70/2002, reprodução indicada por busca (HTTP 403) [NÃO CONFIRMADO]: https://simrppn.sisicmbio.icmbio.gov.br/uploads/ato-criacao/2010_06_08/RJ_RPPN_Fattoria_Grigia.pdf
9. Decreto 13.135/2026, Planalto: https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2026/decreto/d13135.htm
10. Decreto 13.135/2026, Senado: https://legis.senado.leg.br/norma/44154496/publicacao/44157502
11. Atlas Público, publicação e vigência (secundária): https://atlaspublico.com.br/regulacao/dou/decreto-n-13-135-de-9-de-outubro-de-2026-843116
12. Decreto 11.034/2022 (revogado): https://www.planalto.gov.br/ccivil_03/_Ato2019-2022/2022/Decreto/D11034.htm
13. CDC, Lei 8.078/1990: https://www.planalto.gov.br/ccivil_03/leis/l8078compilado.htm
14. Lei 9.784/1999: https://www.planalto.gov.br/ccivil_03/leis/l9784.htm
15. Lei 13.460/2017: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2017/lei/l13460.htm
16. Lei 14.129/2021: https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2021/lei/l14129.htm
17. LGPD, Lei 13.709/2018: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm
18. Lei 13.146/2015, Planalto (arts. 3º, 9º e 63 a 69 e 73 conferidos em 14/11/2026): https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2015/lei/l13146.htm
19. Decreto 8.373/2014 (eSocial): https://www.planalto.gov.br/ccivil_03/_ato2011-2014/2014/decreto/d8373.htm
20. TCU, notícia do Acórdão 1621/2026: https://portal.tcu.gov.br/imprensa/noticias/tribunal-avalia-servico-digital-de-seguro-desemprego-para-trabalhadores-formais
21. TCU, página do sumário executivo: https://portal.tcu.gov.br/publicacoes-institucionais/sumario-executivo/auditoria-seguro-desemprego-emprega-brasil
22. Capital Digital (secundária, substituída por [42] onde possível): https://capitaldigital.com.br/tcu-determina-integracao-do-seguro-desemprego-ao-esocial-e-cobra-reforma-digital/
23. TCU, notícia do Acórdão 135/2024 (TC 006.464/2022-0; reconferida em 14/11/2026): https://portal.tcu.gov.br/imprensa/noticias/inconsistencias-no-seguro-desemprego-causaram-prejuizo-a-administracao-publica
24. Agora RN (secundária): https://agorarn.com.br/?p=831572
25. gov.br, Cadastrar recurso relativo ao seguro-desemprego: https://www.gov.br/pt-br/servicos/cadastrar-recurso-relativo-ao-seguro-desemprego
26. gov.br, Perguntas frequentes do Seguro-Desemprego: https://www.gov.br/pt-br/temas/perguntas-frequentes-seguro-desemprego
27. Caixa, FAQ do Seguro-Desemprego (via resultado de busca): https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx
28. Caixa, Atendimento (não reaberta): https://www.caixa.gov.br/atendimento/Paginas/default.aspx
29. Caixa, Libras por videochamada: https://www.caixa.gov.br/atendimento/libras/
30. Caixa, app Benefícios Sociais: https://www.caixa.gov.br/atendimento/aplicativos/beneficios-sociais-caixa/Paginas/default.aspx
31. MTE, Central Alô Trabalho 158 (reaberta em 14/11/2026; publicada em 14/10/2020): https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/inspecao-do-trabalho/acesso-a-informacao/central-alo-trabalho-158
32. Agência Gov, canais do MTE: https://agenciagov.ebc.com.br/noticias/202607/saiba-como-acessar-os-canais-de-atendimento-do-ministerio-do-trabalho-e-emprego
33. PNCP, CECOT 121/2026: https://pncp.gov.br/api/consulta/v1/orgaos/00360305000104/compras/2026/315
34. O Povo (2023): https://mais.opovo.com.br/jornal/economia/2023/05/19/usuarios-reclamam-de-atraso-no-seguro-desemprego.html
35. Seu Dinheiro (2023): https://www.seudinheiro.com/2023/economia/falha-do-banco-central-atrasa-mais-de-45-mil-parcelas-do-seguro-desemprego-veja-quando-os-beneficios-serao-liberados-lvit
36. Jornal Contábil (2018): https://jornalcontabil.com.br/noticia/seguro-desemprego-fgts-e-pis-tem-novas-datas-de-pagamento/
37. consumidor.gov.br: https://www.consumidor.gov.br/pages/conteudo/sobre-servico
38. Res. CMN 4.860/2020 (cópia secundária): https://www.ancord.org.br/wp-content/uploads/2021/01/ResolucaoBCB-4.860.pdf
39. Res. CODEFAT 392/2004, LegisWeb (art. 15, § 4º; nota de revogação pela Res. 467/2005; aberta em 14/11/2026; secundária): https://www.legisweb.com.br/legislacao/?id=100711
40. Constituição Federal: https://www.planalto.gov.br/ccivil_03/constituicao/constituicao.htm
41. Res. CMN 4.949/2021 (secundária): https://www.legisweb.com.br/legislacao/?id=421170
42. **TCU, Sumário Executivo "Auditoria sobre o Serviço de Seguro-Desemprego oferecido pelo Portal Emprega Brasil", Acórdão 1.621/2026-TCU-Plenário** (PDF oficial, 16 p., lido em 14/11/2026; achados 2.1 a 2.7 e Tabela 2): https://portal.tcu.gov.br/uploads/Sumario_Executivo_Portal_Emprega_Brasil_ec9ed29b5c.pdf
43. Remuneração indireta no CDC, doutrina e referências ao STJ, **fontes secundárias via resultado de busca, não abertas; nenhum precedente verificado**: Migalhas, coluna ABC do CDC (Rizzatto Nunes), https://www.migalhas.com.br/coluna/abc-do-cdc/415038/a-relacao-juridica-de-consumo--o-conceito-de-servico--parte-ii ; Jus.com.br, https://jus.com.br/artigos/84171/existe-relacao-juridica-de-consumo-mesmo-sem-remuneracao

---

## Uso no blueprint

O blueprint final não exibe os 30 fail points individualmente. Usa **seis fail points sintetizados**, cada um remetendo aos FPs de (c):

| FP do blueprint | Síntese | Etapas | FPs de origem | Grau dominante |
|---|---|---|---|---|
| **FP-A** | O status e o motivo não chegam ao telefone, ou chegam errados ("pago" antes do crédito) | E2, E4 | FP1, FP11, FP12, FP13/14 | Comprovado no digital; hipótese no telefone |
| **FP-B** | Espera e abandono sem medição pública; horários e custos desalinhados | E5 | FP4/FP23, FP9 | Hipótese (só a falta de indicador público é comprovada) |
| **FP-C** | Atendente sem visão da decisão, sem protocolo integrado e sem canal definido para bloqueados | E6 | FP15, FP16, FP24, FP30, FP31 | Mecanismo comprovado (FP30); demais hipóteses |
| **FP-D** | Transbordo entre Caixa e MTE | E7 | FP2, FP17, FP18 | Comprovado no MTE; hipótese no 0800 |
| **FP-E** | Retaguarda de pagamento opaca: batimento, conta automática, rejeição de arquivo, devolução, reemissão | E1, E8 | FP7, FP8, FP21, FP22, FP26-A/B, FP27, FP28, FP28-B | Mecanismo comprovado; efeito a medir |
| **FP-F** | Comunicação reativa, mensagens genéricas, recurso lento e com barreiras, prazo divulgado errado | E2, E8 | FP3, FP5, FP6, FP19-A/B, FP20, FP25-A/B | Comprovado (TCU) |

**Regra de leitura em E4.** A leitura de status pela URA fica marcada **[não confirmado em 2026]** até a ligação de teste. O blueprint deve desenhá-la como hipótese (borda tracejada ou nota), não como fato.
