# B — Relatório do assistente 1 (v2)
> **Assistente 1:** Claude Opus 5.5 (Anthropic), com busca na web · **Data:** 14/11/2026 · **Responde a `B_relatorio_auditoria_v1.md`** (auditoria adversarial do assistente 2, ChatGPT) · Versão anterior: `B_relatorio_assistente_v1.md` · Prompt: Apêndice de `A_meta_prompt.md`.

**Convenções.** Os números entre colchetes, como [5], remetem às fontes da seção (f). **[INFERÊNCIA]** marca dedução sem fonte direta. **[NÃO CONFIRMADO]** marca fonte antiga, indireta, secundária ou que não consegui reabrir nesta data. "Não localizado" significa que procurei e não achei. Itens do contrato MTE–Caixa são citados pelo número do Termo de Referência (ex.: TR 5.3.14).

---

## Tratamento das falhas da auditoria v1

| Falha | Resumo | Tratamento | O que mudou / justificativa |
|---|---|---|---|
| F1 | Acórdão TCU 1621/2026 subutilizado | **(a) corrigida** | Incorporei as recomendações detalhadas: motivo específico de cada decisão, memória de cálculo, alinhamento entre o status exibido e a situação real do pagamento, notificações automáticas, fim do limite de 500 caracteres, do limite de 1 MB e da exigência de protocolar antes de juntar documentos, metas de prazo de recurso, base única de conhecimento, treinamento, indicadores de espera e abandono, acessibilidade [20][22]. Ressalva: o detalhamento vem de notícia especializada (Capital Digital, 06/07/2026) e de resultado de busca; o inteiro teor não abriu no sistema de pesquisa do TCU, por isso os itens levam **[NÃO CONFIRMADO no inteiro teor]**. |
| F2 | Agente pagador × agente operador | **(a) corrigida** | Arquitetura institucional refeita (seção b.1) com fonte primária nova: **Contrato MTE–Caixa nº 07/2026** (inexigibilidade nº 05/2026; assinado em 16/04/2026; vigência até 16/04/2031; R$ 383.325.207,75 estimados; R$ 2,25 por parcela) [5][6], que sucede o Contrato nº 11/2021, vigente até 05/04/2026 [7]. A **Portaria Interministerial MTE/MF nº 70/2002** (DOU de 14/10/2002), que institui a Caixa como agente operador, foi localizada só em resultado de busca; o PDF do DOU devolveu HTTP 403 e o Portal do FAT não a lista → **[NÃO CONFIRMADO no texto integral]** [8]. |
| F3 | Funções da URA tiradas de matéria de 2018 | **(a) corrigida** | Todas as funções da URA em E3–E4 (opção do menu, identificação por NIS/CPF, leitura de status e data) passaram a **[NÃO CONFIRMADO]**. A matéria de 2018 virou registro histórico. A confirmação depende de ligação de teste gravada (seção e). |
| F4 | Canais de consulta não distinguidos | **(a) corrigida** | Nova matriz de competência por canal (b.2): CAIXA Tem, Portal Cidadão, app Benefícios Sociais, CTPS Digital/gov.br, Emprega Brasil, 0800 726 0207, agências e lotéricas, 158, Sine/SRTE. A lista de canais da FAQ Caixa veio de resultado de busca, porque o site da Caixa entrou em loop de redirecionamento nesta data [27]. |
| F5 | Emissão × disponibilização × crédito × saque | **(a) corrigida** | Nova tabela b.3 com 12 eventos técnicos e a base de cada um: Res. 957, arts. 12, 20, 21 e 65 [1]; TR 5.3.6.1 (disponibilização "a partir da primeira terça-feira, após recebimento dos lotes") e TR 5.13 (pagamento "considerado efetivado no momento do crédito em conta") [5]. |
| F6 | Art. 21 e art. 65 misturados | **(a) corrigida** | Separados: art. 21 (janela de 67 dias por parcela e devolução ao FAT; reemissão em até 2 anos); art. 65, §§ 1º a 4º (fechamento de lote em até 67 dias, restituição dos não pagos até o fim do 1º decêndio, informação de pagos e não pagos ao sistema) [1]; TR 5.3.17.1 (lote fechado "até 60 dias após o vencimento das parcelas"; devolução até o dia 10) [5]. Registro a diferença de redação 67 × 60 dias [INFERÊNCIA: marcos de contagem distintos]. |
| F7 | Aplicabilidade do Decreto 13.135/2026; art. 16 | **(a) corrigida** | Vigência confirmada: assinado em 09/10/2026, publicado no DOU em 13/10/2026, vigente desde 02/11/2026 (art. 25) [9][10][11]. Análise de incidência feita na seção d.2, com conclusão cautelosa [INFERÊNCIA]. No ponto do art. 16 mantenho a v1: o art. 16 trata do canal **telefônico** (até cinco níveis; opção de humano e de retorno informadas no 1º nível), e o art. 13 trata dos canais **eletrônicos** [9]. A v1 estava certa nesse detalhe. |
| F8 | 20 segundos sem a exceção | **(a) corrigida** | Incluí o art. 15, § 1º (o tempo máximo não se aplica quando há disciplina específica do regulador) e o dever de transferir a chamada ao setor competente (art. 15) [9]. Como calcular o indicador (universo, abandono no denominador) não está no texto lido e entrou no plano de coleta. |
| F9 | Motor de habilitação atribuído sem prova | **(a) corrigida** | Separei norma de implementação: o art. 4º, § 1º, só fala em "sistema seguro-desemprego" [1]. O contrato documenta parte do fluxo: a Caixa envia diariamente à "DATAPREV/SEPRT" os arquivos de movimento liquidado (TR 5.3.8.17) [5]. Quem executa o motor de regras e grava notificações continua **[NÃO CONFIRMADO]**. |
| F10 | Notificação digital: consequências | **(a) corrigida** | Incluí o art. 27, § 4º: a notificação se presume válida cinco dias após disponibilizada no ambiente do sistema; e o § 3º: quem recorre fica ciente de que as notificações podem ser só digitais [1]. Consequência: o prazo de 120 dias pode correr sem leitura efetiva. Os logs de anuência e de ciência seguem no plano (LAI). |
| F11 | Duplicidade Empregador Web × eSocial imprecisa | **(a) corrigida** | Reescrita conforme a determinação: integrar o seguro-desemprego (trabalhador formal) ao eSocial em 180 dias, com captura automática de admissões, demissões e readmissões e processamento tempestivo das readmissões [20][22]; direito de revisão por recurso quando a inconsistência impede a habilitação automática (art. 4º, § 2º) [1]. Quais eventos são duplicados e qual o prazo de sincronização não é público. O TCU recomendou informar isso ao cidadão, o que indica que hoje não se informa [INFERÊNCIA]. |
| F12 | TCU 135/2024 não sustenta FP5 | **(b) defendida** | O dado da v1 é fiel à fonte: o TCU registra "média anual de aproximadamente quatro mil recursos" sobre requerimentos já com dois recursos indeferidos, a falta de segunda instância, recursos ilimitados e um requerimento analisado 15 vezes [23]. Esses fatos sustentam o fail point de **governança do recurso**, que era o objeto do FP5. Os números que a auditoria acrescenta não estão na notícia do TCU: "R$ 1 bilhão" não consta; "29.535 pagamentos" aparece só em imprensa regional [24]. Mesmo assim, separei volume, instância, reincidência e pagamentos indevidos (FP5 e FP10). |
| F13 | Contrato MTE–Caixa não examinado | **(a) corrigida** | Li o Contrato 07/2026 com o Termo de Referência (32 páginas) [5]. Achados: remuneração por parcela paga (art. 66 da Res. 957); Instrumento de Medição de Resultado (IMR) no Anexo V; Portal de Demandas entre as partes; prazos para entrega de documentos (15 dias corridos para demanda judicial ou policial; 30 dias úteis para demanda administrativa, TR 5.3.16); cláusula que isenta a Caixa por falhas decorrentes de dados inconsistentes enviados pelo MTE (TR 5.3.6.8). **O texto não traz cláusula de atendimento telefônico ao cidadão** (nenhuma ocorrência de "telef" no texto extraído). Ficam pendentes o conteúdo do Anexo V e os relatórios de fiscalização (LAI). |
| F14 | Reemissão sem procedimento | **(c) pendente** | Corrigi o prazo: até dois anos **contados da emissão de cada parcela** (art. 21, § 2º) [1]. Canal, unidade responsável, prazo de análise e controle de duplicidade: **não localizados** na Res. 957, no contrato 07/2026 nem nas páginas gov.br lidas. Não há fonte pública que resolva. Como resolver: pedido LAI ao MTE (procedimento, unidade, prazo e quantidade de reemissões por ano) e ligação de teste perguntando à URA e ao atendente como pedir reemissão. |
| F15 | Contestação de pagamento ignorada | **(a) corrigida** | Novo fluxo (b.3 e FP21) com base no art. 20, § 5º [1] e no TR 5.3.14 [5]: crédito em conta Caixa é contestado "no ambiente da CONTRATADA"; crédito em outro banco, pelo banco destinatário; nas demais modalidades, o trabalhador formaliza a contestação numa unidade do MTE, que envia o processo à Caixa; a Caixa analisa e ressarce se procedente, provando a regularidade por log do canal, cartão e senha; os prazos seguem a Lei 9.784. A portaria ministerial prevista no § 5º: **não localizada**. |
| F16 | Transmissão MTE–Caixa não auditável | **(a) corrigida** | Fluxo técnico descrito com base no TR [5]: arquivos semanais com leiaute e horário (5.3.18.1); atraso leva o arquivo à rotina de contingência, sem garantia de prazo (5.3.18.2); confirmação automática de recebimento (5.3.19); arquivo inconsistente é devolvido e "não há possibilidade de reprocessamento" (5.3.20.2); retorno diário de pagos e relatório analítico de rejeitados com motivo (5.3.8.17 a 5.3.8.19; 5.3.21). Novos FP27 e FP28. |
| F17 | Divergência de status de pagamento fora da matriz | **(a) corrigida** | Novo fail point (FP13/14, fundidos): o TCU recomendou alinhar as informações exibidas no sistema à situação real dos pagamentos [22]. Mecanismo plausível documentado: para o contrato, "pagamento = crédito em conta" (TR 5.13), e o crédito pode cair em conta digital localizada ou aberta automaticamente (art. 20, § 2º; TR 5.3.6.4) [1][5] [INFERÊNCIA quanto ao efeito na percepção do cidadão]. |
| F18 | "30 dias" do recurso sem base | **(a) corrigida** | Os "cerca de 30 dias" são o prazo **informado** pela página gov.br ("em torno de 30 dias", variando por tipo de notificação) [25], e não tempo medido. Base legal mais precisa que o art. 49: Lei 9.784, art. 59, § 1º (recurso decidido em até 30 dias do recebimento dos autos) e § 2º (prorrogação por igual período, com justificativa); o art. 49 rege a decisão após concluída a instrução [14]. A Res. 957 não fixa prazo de julgamento (arts. 27 a 31 lidos) [1]. Tempo médio observado: não público. |
| F19 | Canais tratados como equivalentes | **(a) corrigida** | Matriz de competência por canal (b.2), com o que cada canal consulta, decide, recebe e encaminha. |
| F20 | Procedimentos do atendente não examinados | **(c) pendente** | Não há documento público sobre sistemas, permissões ou roteiro do atendente do 0800 726 0207. O contrato 07/2026 não trata de atendimento telefônico, e a recomendação do TCU sobre base de conhecimento mira a rede Sine e os canais do MTE [22]. Como resolver: pedido LAI à Caixa (roteiros, base de conhecimento, perfis de acesso, tipos de ocorrência que o atendente abre) e ligação de teste com roteiro de perguntas. |
| F21 | Acessibilidade da URA | **(c) pendente** | Incluí a Lei 13.146/2015 e a recomendação do TCU de avaliar a acessibilidade digital (dirigida ao serviço do MTE) [18][22]. A acessibilidade da URA em si (alternativa ao menu sonoro, tempo para digitar, clareza das mensagens) não tem fonte pública. Como resolver: ligação de teste com checklist de acessibilidade e pedido LAI sobre o canal Libras e as alternativas para pessoas surdas ou com deficiência de fala. |
| F22 | Consumidor × usuário de serviço público | **(a) corrigida** | Matriz de escalonamento por natureza da manifestação (d.3): SAC e Ouvidoria Caixa (ouvidoria bancária regida pela Res. CMN 4.860/2020) [38], consumidor.gov.br [37], Fala.BR e Ouvidoria do MTE (Lei 13.460, arts. 10 e 16) [15], com prazo e responsável próprios. |
| F23 | Fonte de 2018 para a URA de 2026 | **(a) corrigida** | Rebaixada a registro histórico. Não sustenta mais nenhuma afirmação sobre a URA atual. |
| F24 | Incidente de 2023 tratado como recorrente | **(a) corrigida** | FP7 reescrito como **evento comprovado único** (maio/2023). Frequência e tempo de recuperação: não medidos; entram no plano (LAI). |
| F25 | CECOT 121/2026 sem vínculo com o 0800 | **(b) defendida** | A v1 já dizia que "não está provado que ela cubra o 0800 726 0207" e não tirou conclusão disso [33]. Mantenho. Fato novo: o contrato 07/2026 diz que os contratos de suboperações da Caixa podem ser consultados em licitacoes.caixa.gov.br, aba Transparência (cláusula 10.5) [5]; é o próximo caminho para achar o operador do 0800. |
| F26 | Página geral de atendimento da Caixa | **(b) defendida** | A v1 usou essa página só para os horários do atendimento humano, nunca para descrever funções da URA. Ressalva: a página não reabriu nesta data (loop de redirecionamento), então os horários seguem **[NÃO CONFIRMADO em 2026]**. |
| F27 | LegisWeb como fonte da Res. 957 | **(a) corrigida** | Li o texto revisado da Res. 957 publicado no Portal do FAT (PDF de set./2026) [1][3] e conferi os arts. 4º, 8º, 12, 20, 21, 24, 27, 28, 30, 31, 64, 65 e 66. O DOU não respondeu ("socket hang up"). A LegisWeb saiu da lista de fontes da Res. 957. |
| F28 | Escopo digital do TCU estendido ao telefone | **(a) corrigida** | Aceito. A recomendação do TCU sobre prazos e indicadores de atendimento cita Central 158, e-mail, Facilita e serviços digitais; a notícia oficial não menciona a Caixa [20][22]. Os fail points agora têm coluna **Domínio** (serviço digital do MTE / canal telefônico da Caixa / retaguarda de pagamento) e estão separados entre **comprovado em fonte** e **hipótese a testar**. |
| F29 | 4 mil recursos sem contexto | **(a) corrigida** | Contextualizado até onde a fonte permite: média anual citada pelo TCU para requerimentos já com dois recursos indeferidos; inconsistências apuradas entre 2018 e junho de 2022 em mais de 300 mil solicitações; TC 006.464/2022-0, relator Min.-Subst. Marcos Bemquerer Costa, sessão de 31/01/2024 [23]. O universo total de recursos não aparece na notícia; inteiro teor no plano. |
| F30 | Decreto presumido aplicável | **(a) corrigida** | Seção d.2: análise de incidência pelo art. 1º do Decreto (relação de consumo; incisos I e II do parágrafo único), pelo CDC (art. 3º, § 2º: serviço "mediante remuneração") e pela forma de remuneração do pagamento (União paga R$ 2,25 por parcela; o pagamento é "sem ônus para o trabalhador", art. 20 da Res. 957). Conclusão: regime dúplice [INFERÊNCIA]. |
| F31 | Divergência FAQ × Res. 957 não investigada | **(a) corrigida** | Investigada: a FAQ gov.br diz que a revisão vale por "dois anos contados da data de demissão" e indica o app SINE-Fácil [26]; os "120 dias" da FAQ referem-se ao prazo para **requerer** o benefício, e não ao recurso. O prazo de dois anos coincide com o regime da Res. CODEFAT 392/2004, revogada pela 467/2005 [39] (resultado de busca; origem marcada como [INFERÊNCIA]). A página de serviço diz 120 dias da notificação, mas cita a Res. 467/2005, revogada (página modificada em 25/09/2026) [25]. Risco de perda de prazo: FP6. |
| Seção 3 | Evidências físicas e documentais ausentes | **(a) corrigida** | Plano de coleta (seção e) com as evidências das camadas telefônica, tecnológica, financeira e de governança, cada uma classificada como: pública e obtida; pública não obtida; exige LAI; exige ligação de teste; só obtível em auditoria formal. Duas evidências de governança foram obtidas nesta rodada: o Contrato 07/2026 com o TR e o 8º apostilamento do Contrato 11/2021 [5][7]. |
| FP11–FP25 | Novos fail points propostos | **(a) corrigida** | Todos incorporados na seção (c); nenhum rejeitado. Fundi FP13 com FP14 (e com F17) e FP23 com FP4. FP20 está comprovado no serviço digital (TCU); FP21 tem base contratual (TR 5.13 e 5.3.14); FP19 e FP25 têm indício no serviço digital (recomendações do TCU). FP11, FP12, FP15 a FP18, FP22 e FP24 ficam como hipótese a testar no canal telefônico. Acrescentei FP26 a FP28 a partir do contrato. |

**Contagem:** F1–F31: 25 corrigidas (a), 3 defendidas (b: F12, F25, F26), 3 pendentes (c: F14, F20, F21). A seção 3 e o grupo FP11–FP25 foram tratados como (a).

### Detalhe do tratamento: FP11–FP25 (auditoria v1, seção 4)

Cada fail point proposto pela auditoria foi incorporado na seção (c) com classe de prova, domínio (SD = serviço digital do MTE; TEL = 0800 da Caixa; PAG = retaguarda de pagamento) e forma de teste.

| FP da auditoria | Onde ficou na v2 | Classe de prova | Como testar ou fonte |
|---|---|---|---|
| FP11 URA indisponível | c.3, E3–E4, TEL | Hipótese | Ligações em dias e horários variados; LAI sobre disponibilidade |
| FP12 Falha CPF/NIS | c.3, E4, TEL | Hipótese | Ligação de teste; TR 5.3.5.3 prevê CPF como identificador único |
| FP13 Informação desatualizada | Fundido no FP13/14 (c.1), E2/E4 | Comprovado no SD; hipótese no TEL | TCU 1621/2026 recomendou alinhar o status exibido ao pagamento real |
| FP14 Status divergente | Fundido no FP13/14 (c.1), com F17 | Comprovado no SD; hipótese no TEL | Idem |
| FP15 Histórico incompleto | c.3, E6, TEL | Hipótese | LAI (perfis de acesso); ligação de teste |
| FP16 Sem ocorrência rastreável | c.3, E6, TEL | Hipótese | Pedir protocolo na ligação; LAI |
| FP17 Transferência sem histórico | c.3, E6–E7, TEL | Hipótese | Ligação de teste; LAI à Caixa e ao MTE |
| FP18 Canal sem competência | c.3, E7, TEL/SD | Hipótese apoiada na matriz b.2 | Ligações com cenários de reemissão, contestação e recurso |
| FP19 Sem retorno após regularização | c.1, E8, SD | Indício (recomendação do TCU) | TCU 1621/2026 |
| FP20 Recurso com barreiras | c.1, E8, SD | Comprovado no SD | TCU 1621/2026: 500 caracteres, 1 MB, protocolo antes da juntada |
| FP21 Pago sem reconhecimento | c.2, E4/E9, PAG | Mecanismo comprovado | Art. 20, § 5º; TR 5.13 e 5.3.14 |
| FP22 Reemissão duplicada | c.3, E8, PAG | Hipótese | LAI ao MTE (procedimento não localizado) |
| FP23 Abandono não monitorado | Fundido no FP4 (c.3), E5, TEL | Hipótese | LAI à Caixa: espera média e taxa de abandono |
| FP24 Protocolo sem vínculo com o MTE | c.3, E6–E7, TEL/SD | Hipótese | Ligação de teste; LAI |
| FP25 Sem comunicação proativa | c.1, E2/E9, SD | Indício (recomendação do TCU) | TCU 1621/2026 |

### Detalhe do tratamento: seção 3 da auditoria v1 (evidências)

A seção (e) traz um plano de coleta com uma linha por evidência, dizendo se ela é **pública e obtida**, **pública e não obtida**, **exige LAI** ou **exige ligação de teste**:

- **Camada telefônica:** gravação da URA, mensagens, tempo até o humano, protocolo e acessibilidade exigem ligação de teste (roteiro de seis ligações em dias e horários diferentes). Espera, abandono e volume de chamadas exigem LAI à Caixa. Roteiros, base de conhecimento e perfis do atendente exigem LAI.
- **Camada tecnológica:** arquitetura da URA, integrações, logs e plano de contingência só se obtêm em auditoria formal. Isso foi registrado como fora do alcance da pesquisa pública.
- **Camada financeira:** lotes, comprovantes de transmissão, rejeições, conciliação, restituições e reemissões exigem LAI ao MTE (dados agregados).
- **Camada de governança:** o Contrato 07/2026 e o TR foram obtidos. O IMR (Anexo V), os relatórios de fiscalização e o plano de ação do MTE ao TCU exigem LAI. O inteiro teor dos acórdãos é público, mas não foi obtido nesta rodada.

---

## (a) Sumário

- **O serviço tem quatro papéis, não dois.** O CODEFAT normatiza. O MTE gere o benefício, decide a habilitação, julga recursos e emite os documentos de pagamento em lotes semanais (Res. 957, arts. 4º, 28 e 65) [1]. A Caixa paga, como agente pagador (art. 64, § 1º) [1], por contrato com o MTE: o **Contrato 07/2026**, de 16/04/2026, remunera R$ 2,25 por parcela paga e foi firmado por inexigibilidade, "por exclusividade" da Caixa [5]. A Dataprev recebe os arquivos diários de pagamento (TR 5.3.8.17) [5]. A Portaria Interministerial 70/2002, que trataria a Caixa como agente operador, foi localizada só por busca [8] [NÃO CONFIRMADO no texto].
- **A URA 0800 726 0207 é canal da Caixa, mas o contrato do benefício não fala dela.** O Termo de Referência regula lotes, crédito, saque, contestação, devolução e documentos, sem cláusula de atendimento telefônico [5]. O operador e os níveis de serviço do 0800 seguem desconhecidos.
- **"Não caiu" pode significar doze coisas diferentes.** Entre o requerimento e o saque há decisão, emissão do lote, transmissão, batimento de CPF, disponibilização na primeira terça-feira após o lote, crédito em conta (que para o contrato já é "pagamento"), eventual devolução de TED/PIX, saque, retorno de pagos, fechamento de lote e devolução ao FAT [1][5]. A URA só vê parte disso [INFERÊNCIA].
- **O TCU (Acórdão 1621/2026) avaliou o serviço digital do MTE, não a URA.** Seus achados (mensagens genéricas, falta de memória de cálculo, divergência entre status exibido e pagamento real, recurso com limite de 500 caracteres e 1 MB, falta de notificações automáticas) comprovam falhas do **serviço digital** [20][22]. No canal telefônico da Caixa, as falhas equivalentes continuam **hipóteses a testar**.
- **O Decreto 13.135/2026 está vigente desde 02/11/2026** [9][11], mas regulamenta o CDC. No fluxo do benefício o trabalhador não remunera a Caixa: quem paga é a União. Leitura prudente: a Lei 13.460 se aplica com segurança; o Decreto alcança, no máximo, as demandas bancárias da conta onde o benefício cai [INFERÊNCIA].
- **A informação oficial continua contraditória.** A FAQ gov.br fala em revisão em "dois anos contados da data de demissão" e no app SINE-Fácil [26]; a Res. 957 fixa 120 dias contados da notificação (art. 27, § 2º) [1]; a página de recurso cita a Res. 467/2005, revogada [25].
- **O que ainda falta é evidência direta do canal:** gravação da URA, roteiros, indicadores de espera e abandono, contrato do operador do 0800, IMR do contrato 07/2026. A seção (e) separa o que é público, o que exige LAI e o que exige ligação de teste.

---

## (b) Etapas da jornada

### b.1 Arquitetura institucional (F2, F9)

| Função | Quem | Base | Grau |
|---|---|---|---|
| Normatizar | CODEFAT | Lei 7.998, art. 19 [4]; Res. 957 [1] | Comprovado |
| Gerir o benefício, habilitar, notificar, julgar recurso | MTE (Secretaria de Trabalho) | Res. 957, arts. 4º, 8º, 27 e 28 [1] | Comprovado |
| Emitir os DSD em lotes semanais e enviá-los ao pagador | MTE | Res. 957, art. 65 [1]; TR 5.3.6.2 [5] | Comprovado |
| Executar o sistema (motor de regras, bases, notificações) | Dataprev, por contrato com o MTE | TR 5.3.8.17 (Caixa envia arquivos à "DATAPREV/SEPRT") [5]; TCU 135/2024 (relação Strab–Dataprev) [23] | Parcial: o papel no motor de regras é [NÃO CONFIRMADO] |
| Pagar (crédito, saque, devolução, contestação) | Caixa, agente pagador | Res. 957, art. 64, § 1º [1]; Lei 7.998, art. 15 [4]; Contrato 07/2026 [5] | Comprovado |
| Agente operador do programa | Caixa | Portaria Interministerial MTE/MF 70/2002 [8] | [NÃO CONFIRMADO no texto integral] |
| Operar o 0800 726 0207 | Caixa (canal próprio); operador terceirizado desconhecido | FAQ Caixa [27]; CECOT 121/2026 sem vínculo provado [33] | [NÃO CONFIRMADO] |
| Fornecer dados de vínculo | Empregador (eSocial, Empregador Web) | Res. 957, arts. 4º, § 1º, e 40, § 1º [1] | Comprovado |

**Repartição de risco contratual.** O TR diz que a Caixa não responde por pagamentos "indevidos, recusados, estornados, suspensos, atrasados" decorrentes de inconsistências nos dados enviados pelo MTE (TR 5.3.6.8) [5]. Na prática, quando a falha nasce no dado, a Caixa tem base contratual para remeter o cidadão ao MTE. Isso explica, em parte, o transbordo de canal (FP2) [INFERÊNCIA].

### b.2 Matriz de competência por canal (F4, F19)

| Canal | Quem opera | Consulta situação da parcela | Mostra motivo da decisão | Requer / recorre | Contesta saque | Pede reemissão | Fonte e grau |
|---|---|---|---|---|---|---|---|
| URA 0800 726 0207 | Caixa | Sim, segundo a FAQ Caixa [27]; quais dados lê: [NÃO CONFIRMADO] | Não documentado [INFERÊNCIA: não] | Não | Não documentado | Não documentado | FAQ Caixa via busca [27] |
| Atendente humano do 0800 | Caixa (operador desconhecido) | [NÃO CONFIRMADO] | [NÃO CONFIRMADO] | Não | [NÃO CONFIRMADO] | [NÃO CONFIRMADO] | Sem fonte pública (F20) |
| CAIXA Tem | Caixa | Sim, para crédito em conta digital Caixa [27] | Não | Não | Sim, quando o crédito foi em conta Caixa ("ambiente da CONTRATADA", TR 5.3.14.1) [5] [INFERÊNCIA quanto ao canal exato] | Não documentado | FAQ via busca; TR |
| App Benefícios Sociais / Portal Cidadão | Caixa | Sim [27][30] | Não | Não | Não documentado | Não documentado | FAQ via busca |
| Agência, lotérica, Caixa Aqui | Caixa | Sim | Não | Não | Sim, para crédito em conta Caixa [5] | A FAQ gov.br manda procurar agência quando a parcela não está no cartão [26] | TR 5.3.8.11; FAQ gov.br |
| CTPS Digital / gov.br (Emprega Brasil) | MTE | Sim (datas das parcelas) [26] | Sim, aba "Notificações" [26] | Sim (Res. 957, arts. 5º e 27, § 1º) [1] | Não | Não documentado | Res. 957; FAQ gov.br |
| Central 158 | MTE | Orientação | Orientação | Agenda atendimento presencial [25] | Não | Não | Página de recurso [25]; MTE [31] |
| Sine / SRTE (presencial) | MTE e rede Sine | Sim | Sim | Sim (art. 27, § 1º) [1] | Recebe a contestação nas modalidades sem crédito em conta (TR 5.3.14.2) [5] | [INFERÊNCIA: provável] | Res. 957; TR |
| Banco destinatário (TED/PIX) | Outro banco | Extrato | Não | Não | Sim, se o crédito não foi devolvido (TR 5.3.14.1) [5] | Não | TR |

**Leitura da matriz.** Só os canais do MTE mostram o motivo da decisão e recebem recurso. Os canais da Caixa mostram o resultado financeiro. A contestação de saque se divide em três destinos, conforme o meio de pagamento. Reemissão não tem canal documentado.

### b.3 Eventos do pagamento: emissão, disponibilização, crédito e saque (F5, F6, F15, F16)

| # | Evento | Quem | Base | O que o cidadão vê | Falha possível |
|---|---|---|---|---|---|
| 1 | Requerimento (dia 0) | Trabalhador / MTE | Res. 957, arts. 5º e 12, I [1] | Comprovante no gov.br/CTPS Digital | Fora do prazo |
| 2 | Habilitação automática e decisão | Sistema do MTE | Art. 4º, § 1º; art. 8º [1] | Notificação digital | Dado do empregador (FP3) |
| 3 | Notificação presumida válida | Sistema do MTE | Art. 27, § 4º: cinco dias após a disponibilização [1] | Nada, se não abrir o app | Prazo corre sem ciência real (FP25) |
| 4 | Emissão do DSD em lote semanal | MTE | Art. 65, caput [1]; TR 5.3.6.2 [5] | Nada | Registro ausente do lote |
| 5 | Transmissão e confirmação de recebimento | MTE → Caixa | TR 5.3.18 e 5.3.19 [5] | Nada | Atraso leva à contingência; arquivo rejeitado sem reprocessamento (FP28) |
| 6 | Batimento com o CPF | Caixa | TR 5.3.5: primeiro nome e data de nascimento [5] | Nada | Parcela devolvida ao MTE (FP27) |
| 7 | Disponibilização para pagamento | Caixa | TR 5.3.6.1: a partir da 1ª terça-feira após o lote [5]; 1ª parcela 30 dias após o requerimento e as demais a cada 30 dias da emissão anterior (art. 12) [1] | Data no app | Atraso se o lote atrasar |
| 8 | Crédito em conta (efetivo pagamento para o contrato) | Caixa | Art. 20 e § 2º [1]; TR 5.13 e 5.3.6.4 [5] | Saldo na conta informada, ou em conta digital localizada ou aberta automaticamente | Crédito em conta que o cidadão não conhece (FP26) |
| 9 | Devolução de TED/PIX e nova tentativa | Banco destinatário → Caixa | TR 5.3.6.5 [5] | Atraso | Ciclo de devoluções |
| 10 | Saque | Trabalhador | TR 5.3.8.12 e 5.3.8.14: cartão e senha, biometria ou documento na agência [5] | Dinheiro | Saque por terceiro → contestação (art. 20, § 5º; TR 5.3.14) |
| 11 | Retorno de pagos e não pagos | Caixa → Dataprev/MTE | Art. 65, §§ 2º e 4º [1]; TR 5.3.8.17 a 5.3.8.19 e 5.3.21 [5] | Status no app do MTE | Status atrasado ou divergente (FP13/14) |
| 12 | Fim da janela, fechamento de lote e devolução ao FAT; reemissão | Caixa / MTE | Art. 21 e §§; art. 65, §§ 1º e 3º [1]; TR 5.3.17.1 [5] | Parcela some | Reemissão em até 2 anos da emissão, sem canal documentado (FP8) |

### b.4 Tabela de etapas (E1–E9)

A **Linha de Interação** passa entre "Ações do cidadão" e "Frontstage". A **Linha de Visibilidade** passa entre "Frontstage" e "Backstage": tudo à direita dela o cidadão não vê. Não há dado público de tempo de espera em nenhuma etapa telefônica; os tempos citados vêm de norma, contrato ou página de serviço.

| # | Etapa | Evidências físicas | Ações do cidadão | Frontstage | ‖ Linha de Visibilidade ‖ Backstage | Processos de suporte |
|---|---|---|---|---|---|---|
| E1 | **Percebe que a parcela não caiu** | Extrato da conta ou do CAIXA Tem sem crédito; data prevista vista antes no app (eventos 7 e 8 de b.3) | Espera a data; confere o saldo, às vezes na conta errada | — (sem contato) | Caixa processa o lote recebido; batimento de CPF (TR 5.3.5) [5] | Lote semanal do MTE (art. 65) [1]; disponibilização na 1ª terça-feira após o lote (TR 5.3.6.1); crédito em conta digital localizada se a conta informada falhar (art. 20, § 2º) [1][5] |
| E2 | **Procura o motivo por conta própria** | Tela "Consultar Seguro-Desemprego" e aba "Notificações" (CTPS Digital/gov.br) [26]; apps CAIXA Tem e Benefícios Sociais [27][30] | Abre os apps, pesquisa, compara informações e decide ligar | Apps do MTE (motivo) e da Caixa (situação financeira) | Sistema do MTE grava decisão e notificação [operador: NÃO CONFIRMADO] | Notificação só digital, com anuência (art. 8º); presunção de validade em cinco dias (art. 27, § 4º) [1]. O TCU recomendou motivo específico, memória de cálculo e status alinhado ao pagamento real [22] |
| E3 | **Liga para o 0800 726 0207 e ouve o menu** | Número 0800 726 0207 [27]; mensagens gravadas e opções [NÃO CONFIRMADO em 2026; registro histórico de 2018 [36]] | Disca, ouve e escolhe | URA 24h [NÃO CONFIRMADO em 2026] | Plataforma de URA e roteamento ACD/CTI [INFERÊNCIA: padrão de contact center] | Operador do canal e contrato desconhecidos; o Contrato 07/2026 não trata de telefone [5]; CECOT 121/2026 sem vínculo provado [33] |
| E4 | **Identifica-se e ouve o status automático** | Dados digitados (CPF ou NIS) [NÃO CONFIRMADO] | Digita e confirma | URA informaria a situação da parcela [NÃO CONFIRMADO em 2026] | Consulta à base de pagamento da Caixa [INFERÊNCIA a partir do art. 65 e da FAQ] | Retorno de pagos e não pagos (art. 65, § 4º; TR 5.3.8.17) [1][5]; janela de 67 dias (art. 21) [1] |
| E5 | **Pede atendente e espera** | Mensagem ou música de espera [NÃO CONFIRMADO]; tempo de espera não divulgado | Escolhe atendente; espera; pode desistir | Fila; atendimento humano seg.–sex. 8h–21h e sáb. 10h–16h [28] [NÃO CONFIRMADO em 2026] | Distribuição automática de chamadas [INFERÊNCIA] | Indicadores de espera e abandono: não localizados. Parâmetro do Decreto 13.135 (art. 15, I: 20 s para 80%; 300 s para as demais), com a ressalva do § 1º e incidência incerta (d.2) [9] |
| E6 | **Fala com o atendente** | Voz do atendente; protocolo [NÃO CONFIRMADO na prática] | Explica e informa dados | Atendente Caixa; canal Libras por videochamada, à parte [29] | Sistemas e permissões do atendente: [NÃO CONFIRMADO] (F20) | Se a falha vier do dado do MTE, o contrato isenta a Caixa (TR 5.3.6.8) [5]; em 2023 a Caixa remeteu ao MTE as informações sobre o benefício [34] |
| E7 | **É encaminhado a outro canal** | Indicação verbal de app, site, 158 ou agência; 158 gratuito só de telefone fixo [31] | Desliga e procura outro canal | Fala do atendente ou da URA | Transferência direta ao 158: não documentada [INFERÊNCIA: não há] | Canais do MTE: 158, Facilita, e-mail, Sine. O TCU achou trabalhadores encaminhados "de um lugar para outro" nesses canais [20] |
| E8 | **Resolve (ou tenta) no canal certo** | Notificação com motivo; formulário de recurso com limite de 500 caracteres e anexos de 1 MB [22] [NÃO CONFIRMADO no inteiro teor; a FAQ gov.br indicaria 1 MB por arquivo e 10 MB no total, segundo resultado de busca [26]] | Lê a notificação; recorre em até 120 dias da notificação; corrige dados; pede reemissão ou contesta saque | gov.br, CTPS Digital, Sine/SRTE com agendamento pelo 158 ou pela Facilita [25]; unidade do MTE para contestação (TR 5.3.14.2) [5] | Análise do recurso pela Secretaria de Trabalho, em instância única (art. 28) [1]; análise da contestação pela Caixa (TR 5.3.14.4) [5] | Recurso: arts. 27 a 31 [1]; Lei 9.784, art. 59, §§ 1º e 2º [14]; reemissão em até 2 anos da emissão (art. 21, § 2º) [1]; resultado do recurso só no gov.br e na CTPS Digital (art. 31) [1] |
| E9 | **Recebe, desiste ou reclama** | Crédito ou saque; protocolo de reclamação | Saca, abandona ou reclama | SAC e Ouvidoria Caixa; consumidor.gov.br; Fala.BR (MTE) | Tratamento da manifestação | Ouvidoria pública: 30 dias (Lei 13.460, art. 16) [15]; ouvidoria bancária: Res. CMN 4.860/2020 [38]; SAC do Decreto 13.135 (art. 21: 7 dias corridos) só se incidir (d.2) [9] |

**Notas.** E3 a E6 formam o "momento URA". E1, E2, E7 e E8 ficam fora da ligação, mas decidem se ela é útil. O ponto de virada é E6: ali o cidadão descobre se o problema é de **pagamento** (Caixa resolve, conforme b.3) ou de **concessão e dado** (MTE resolve). A E8 agora tem dois ramos que a v1 não separava: recurso (MTE) e contestação de saque (Caixa, com entrada pelo MTE em parte dos casos).

---

## (c) Fail points revisados

Domínios: **SD** = serviço digital do MTE (gov.br, CTPS Digital, Emprega Brasil e canais do MTE); **TEL** = canal telefônico da Caixa (URA e atendente do 0800 726 0207); **PAG** = retaguarda de pagamento MTE–Caixa–Dataprev; **INF** = informação oficial.

### c.1 Comprovados em fonte

| # | Falha | Etapa | Domínio | Evidência | Quem responde |
|---|---|---|---|---|---|
| FP2 | **Transbordo em cadeia:** o trabalhador é encaminhado de um canal a outro | E7 | SD (comprovado); TEL (hipótese) | TCU 1621/2026: "de um lugar para outro", respostas diferentes para casos parecidos, falta de base única de conhecimento nos canais do MTE e da rede Sine [20][22] | MTE |
| FP3 | **Dado errado ou duplicado do empregador** gera bloqueio e indeferimento | Antes de E1; aparece em E2 | SD / PAG | TCU 1621/2026: Empregador Web e eSocial em paralelo; determinação de integração em 180 dias [20]; Res. 957, arts. 4º, § 2º, e 40, § 1º [1] | MTE; empregador |
| FP5 | **Recurso lento, pouco previsível e sem governança** | E8 | SD | TCU 1621/2026: análise "demorada e imprevisível"; recomendação de metas e responsáveis [20][22]. TCU 135/2024: sem 2ª instância, recursos ilimitados, cerca de 4 mil recursos/ano sobre requerimentos já com dois indeferimentos, requerimento analisado 15 vezes [23] | MTE; Dataprev |
| FP6 | **Informação oficial contraditória** que pode fazer perder prazo | E2, E8 | INF | FAQ gov.br: revisão em "dois anos contados da data de demissão" e app SINE-Fácil [26]; página de recurso cita a Res. 467/2005, revogada [25]; Res. 957: 120 dias da notificação (art. 27, § 2º) [1] | MTE (Carta de Serviços, Lei 13.460, art. 7º) [15] |
| FP7 | **Falha de liquidação financeira** (evento único comprovado) | Entre E1 e E4 | PAG | Maio/2023: 45.335 parcelas por TED atrasadas, atribuídas à indisponibilidade do TED do Banco Central [35]. Recorrência: não medida (F24) | Caixa; Banco Central; MTE |
| FP10 | **Pagamentos indevidos e governança Strab–Dataprev** | Suporte | PAG | TCU 135/2024: inconsistências em mais de 300 mil solicitações (2018 a jun./2022); indícios de R$ 147 milhões e de R$ 544 mil [23] | MTE; Dataprev |
| FP13/14 | **Status exibido diverge da situação real do pagamento** (inclui F17) | E2, E4 | SD (comprovado); TEL (hipótese) | O TCU recomendou alinhar as informações exibidas à situação real dos pagamentos e informar procedimentos quando o valor não é liberado [22] [NÃO CONFIRMADO no inteiro teor] | MTE; Caixa (retorno de pagos) |
| FP19 | **Sem retorno ao cidadão após regularização de dado** | E8 | SD | O TCU recomendou informar o órgão responsável, se haverá reanálise automática e o prazo de sincronização [22] [INFERÊNCIA: hoje não se informa] | MTE |
| FP20 | **Recurso com barreiras técnicas** (500 caracteres, 1 MB por anexo, protocolo antes da documentação completa) | E8 | SD | TCU 1621/2026, segundo notícia especializada e resultado de busca [22]. A página de serviço diz que se pode anexar documentos "a qualquer tempo" [25], o que não afasta o limite de tamanho | MTE |
| FP25 | **Sem comunicação proativa** de mudança de status | E2, E9 | SD (indício); TEL (hipótese) | O TCU recomendou notificações automáticas pelo canal escolhido pelo cidadão [22]; a notificação se presume válida em cinco dias (art. 27, § 4º) [1] | MTE |

### c.2 Mecanismo comprovado em norma ou contrato; efeito a medir

| # | Falha | Etapa | Domínio | Evidência do mecanismo | O que falta medir | Quem responde |
|---|---|---|---|---|---|---|
| FP8 | **Parcela devolvida ao FAT** e reemissão sem canal documentado | E1, E8 | PAG / INF | Art. 21 e § 2º (2 anos da emissão de cada parcela) [1]; canal: não localizado | Quantidade de devoluções e reemissões; prazo | MTE; Caixa |
| FP21 | **"Pago" sem que o trabalhador reconheça o recebimento** | E4, E9 | PAG | TR 5.13: pagamento efetivado no crédito em conta; art. 20, § 5º; TR 5.3.14: contestação em três destinos, com ida a unidade do MTE em parte dos casos [1][5] | Volume e prazo das contestações | Caixa; MTE; banco destinatário |
| FP26 | **Crédito em conta que o trabalhador não conhece** (conta digital localizada ou aberta automaticamente) | E1, E4 | PAG | Art. 20, § 2º [1]; TR 5.3.6.4 [5] | Quantos créditos vão para conta aberta automaticamente; quantas ligações isso gera | Caixa; MTE |
| FP27 | **Parcela devolvida por incompatibilidade no CPF** (primeiro nome ou data de nascimento) | E1 | PAG | TR 5.3.5.2 [5] | Volume de devoluções por batimento | MTE (dado); Caixa (batimento) |
| FP28 | **Arquivo atrasado ou rejeitado** atrasa o lote inteiro | E1 | PAG | TR 5.3.18.2 (contingência) e 5.3.20.2 (sem reprocessamento) [5] | Frequência e efeito em dias | MTE; Caixa; Dataprev |

### c.3 Hipóteses a testar (canal telefônico e interfaces)

| # | Falha | Etapa | Domínio | Por que é plausível | Como testar | Quem responderia |
|---|---|---|---|---|---|---|
| FP1 | **A URA não explica o motivo** do bloqueio ou indeferimento | E4, E6 | TEL | O motivo está na notificação digital (art. 8º) e o resultado do recurso só no gov.br e na CTPS Digital (art. 31) [1] | Ligação de teste com CPF com notificação pendente (com consentimento do titular) | Caixa (roteiro); MTE (conteúdo) |
| FP4 | **Desistência na fila sem registro** (inclui FP23: abandono não monitorado) | E5 | TEL | Nenhum indicador público; o TCU recomendou ao MTE medir espera e abandono **nos canais do MTE** [22], não no 0800 | LAI à Caixa: tempo médio de espera, taxa de abandono, série mensal | Caixa |
| FP9 | **Horários e custos desalinhados** entre canais | E5, E7 | TEL / SD | Caixa até 21h [28] [NÃO CONFIRMADO em 2026]; 158 gratuito só de fixo [31] | Reconferir páginas; ligação fora de horário | Caixa; MTE |
| FP11 | **URA indisponível ou sem acesso à base de pagamento** | E3, E4 | TEL | Depende da integração com a base que recebe os lotes [INFERÊNCIA] | Ligações em horários e dias variados; LAI sobre incidentes | Caixa |
| FP12 | **Falha de identificação por CPF ou NIS** | E4 | TEL | O contrato prevê migrar para o CPF como identificador único (TR 5.3.5.3) [5]; a URA pode pedir outro dado [INFERÊNCIA] | Ligação de teste | Caixa |
| FP15 | **Atendente sem acesso ao histórico completo** | E6 | TEL | O atendente da Caixa não acessa, em princípio, a decisão do MTE [INFERÊNCIA] | LAI (perfis de acesso); ligação de teste | Caixa; MTE |
| FP16 | **Atendente não abre ocorrência rastreável** | E6 | TEL | Sem documento público | Pedir protocolo na ligação; LAI | Caixa |
| FP17 | **Transferência sem preservar o histórico** | E6, E7 | TEL | Não há integração documentada entre o 0800 e o 158 | Ligação de teste; LAI a ambos | Caixa; MTE |
| FP18 | **Encaminhamento a canal sem competência** | E7 | TEL / SD | A matriz b.2 mostra competências que não se sobrepõem | Ligação de teste com cenários (reemissão, contestação, recurso) | Caixa; MTE |
| FP22 | **Reemissão sem controle de duplicidade** | E8 | PAG | Procedimento não localizado (F14) | LAI ao MTE | MTE; Caixa |
| FP24 | **Protocolo da Caixa não se liga à demanda no MTE** | E6, E7 | TEL / SD | Não há canal documentado entre os dois atendimentos; o Portal de Demandas do contrato é entre instituições, não para o cidadão (TR 5.3.22) [5] | LAI a ambos | Caixa; MTE |

---

## (d) Normativos

### d.1 Tabela

| Norma | Artigo | O que exige ou prevê | Etapa |
|---|---|---|---|
| Constituição [40] | art. 7º, II; art. 201, III | Seguro-desemprego como direito do trabalhador; proteção ao desemprego involuntário | Todas |
| Lei 7.998/1990 [4] | arts. 3º, 6º, 7º, 8º | Requisitos, requerimento, suspensão e cancelamento | E2 |
| | art. 15 | Pagamento pelos bancos oficiais federais | E4 |
| | art. 19 | Competências do CODEFAT | Suporte |
| Res. CODEFAT 957/2022 (texto revisado, Portal do FAT) [1] | art. 4º, §§ 1º e 2º | Habilitação automática por CNIS, FGTS, GFIP, eSocial ou documento judicial; revisão por recurso se a inconsistência impedir a habilitação | Suporte, E2 |
| | art. 8º | Notificação exclusivamente digital, com anuência e cadastro no gov.br ou na CTPS Digital | E2 |
| | art. 12 e par. ún. | 1ª parcela 30 dias após o requerimento; as demais a cada 30 dias da emissão da anterior | E1 |
| | art. 20, §§ 1º a 5º | Crédito em conta sem ônus; conta digital localizada pelo agente pagador; outras formas; guarda de comprovantes por 5 anos; contestação de recebimento por procedimento administrativo | E1, E4, E8 |
| | art. 21, §§ 1º e 2º | 67 dias de disponibilidade; devolução ao FAT; retenção excepcional; reemissão em até 2 anos da emissão de cada parcela | E8 |
| | arts. 22 a 24 | Suspensão, cancelamento e defesa em 30 dias | E2, E8 |
| | art. 27, §§ 1º a 7º | Recurso no gov.br, na CTPS Digital ou presencial; 120 dias da notificação; presunção de notificação em 5 dias; limites de mérito | E8 |
| | arts. 28 a 31 | Instância única; novo recurso em 30 dias; prazos em dias corridos; resultado só no gov.br e na CTPS Digital | E8 |
| | art. 40, § 1º | Empregador transmite pelo Empregador Web | Antes de E1 |
| | art. 64, § 1º | Caixa é o agente pagador | Suporte |
| | art. 65, §§ 1º a 4º | Lotes semanais; fechamento em até 67 dias; restituição dos não pagos; pagos e não pagos informados ao sistema | Suporte |
| | art. 66 e par. ún. | Serviços bancários pagos conforme contrato com o Ministério; tarifa por DSD pago no mês | Suporte |
| Contrato MTE–Caixa 07/2026 e TR [5] | TR 5.3.5, 5.3.6, 5.3.8, 5.3.14 a 5.3.22; 5.13; cláusula 10 | Batimento de CPF; disponibilização na 1ª terça-feira; canais de saque; contestação; devolução; documentos; arquivos e retorno; Portal de Demandas; LGPD | E1, E4, E8, suporte |
| Portaria Interministerial MTE/MF 70/2002 [8] | — | Caixa como agente operador [NÃO CONFIRMADO no texto integral] | Suporte |
| Decreto 13.135/2026 [9] | art. 1º e par. ún., I e II | Regulamenta o CDC; SAC nas relações de consumo; alcança fornecedores regulados pelo Executivo federal conforme critérios do regulador (I) e serviços financeiros digitais supervisionados pelo BC (II) | E3 a E6 (se incidir) |
| | arts. 13 e 16 | Até cinco níveis (13: canais eletrônicos; 16: telefone); humano e retorno informados no 1º nível | E3 |
| | art. 14 | Telefone obrigatório; humano das 8h às 20h, sete dias por semana; retorno em 300 s se a ligação cair | E5 |
| | art. 15 e § 1º | Humano em todos os níveis; 20 s para 80% e 300 s para as demais; transferência ao setor competente; exceção por regra do regulador | E5, E6 |
| | arts. 18 e 21 | Protocolo e histórico; resposta em 7 dias corridos | E6, E9 |
| | arts. 24 e 25 | Revoga o Decreto 11.034/2022; vigência 20 dias após a publicação (02/11/2026) [11] | — |
| CDC, Lei 8.078/1990 [13] | art. 3º, § 2º; art. 22 | Serviço é atividade "mediante remuneração", inclusive bancária; órgãos públicos e suas empresas devem prestar serviço adequado | d.2 |
| Lei 9.784/1999 [14] | art. 49 | Decisão em até 30 dias após concluída a instrução, prorrogáveis | E8 |
| | art. 59, §§ 1º e 2º | Recurso decidido em até 30 dias do recebimento dos autos, prorrogável por igual período | E8 |
| Lei 13.460/2017 [15] | art. 1º; art. 5º, XIV; art. 6º; art. 7º; arts. 10, 16 e 23 | Aplicação à administração indireta; linguagem simples; acesso à situação do processo; Carta de Serviços; ouvidoria em 30 dias; avaliação anual | Todas |
| Lei 14.129/2021 [16] | art. 3º | Princípios do governo digital (linguagem clara, interoperabilidade, atendimento presencial) | E6, E7 |
| LGPD [17] | arts. 7º, III; 18; 23; 24, par. ún.; 26 | Tratamento para política pública; direitos do titular; Caixa tratada como órgão público ao operacionalizar política pública | E4, suporte |
| Lei 13.146/2015 [18] | — (verificar arts. de acessibilidade na comunicação) | Acessibilidade de serviços e comunicação | E3 a E6 |
| Decreto 8.373/2014 [19] | — | Institui o eSocial (base da determinação do TCU) | Antes de E1 |
| Res. CMN 4.860/2020 [38]; Res. CMN 4.949/2021 [41] | — | Ouvidoria e relacionamento com clientes nas instituições financeiras | E9 (lado bancário) |

### d.2 O Decreto 13.135/2026 incide sobre a URA do seguro-desemprego? (F7, F30)

**Fatos verificados.**
1. O decreto "regulamenta a Lei nº 8.078" e trata do SAC "nas relações de consumo" (art. 1º, caput) [9].
2. Estão sujeitos a ele (art. 1º, par. ún.): **(I)** fornecedores de serviços regulados pelo Executivo federal **que se enquadrem nos critérios** do órgão regulador; **(II)** fornecedores de serviços financeiros, de pagamento ou de crédito **por plataformas digitais** supervisionados pelo Banco Central [9][10].
3. O CDC define serviço como atividade fornecida "mediante remuneração", inclusive a bancária (art. 3º, § 2º) [13].
4. No benefício, quem remunera a Caixa é a União: R$ 2,25 por parcela paga (Contrato 07/2026, item 1.1; Res. 957, art. 66) [1][5]. O pagamento é "sem ônus para o trabalhador" (art. 20, caput) [1].
5. A Caixa trata os dados como órgão público quando operacionaliza política pública (LGPD, art. 24, par. ún.) [17], e a Lei 13.460 se aplica à administração indireta [15].
6. Não localizei ato do CMN ou do Banco Central que fixe os "critérios" do inciso I para bancos sob o Decreto 13.135.

**Análise [INFERÊNCIA].**
- **Na relação de benefício** (saber se a parcela foi liberada, por que não caiu, quando cai), o trabalhador não é consumidor da Caixa. Ele é titular de um direito social pago pela União por meio de um contratado, e não remunera o serviço. Falta o elemento "mediante remuneração" do art. 3º, § 2º, do CDC. Nessa parte, o regime é de serviço público: Lei 13.460, Lei 14.129, Res. 957 e Lei 9.784. O Decreto 13.135 serve de **parâmetro de qualidade**, não de obrigação exigível.
- **Na relação bancária** (conta digital onde o benefício caiu, cartão, senha, saque, contestação de saque em conta Caixa), há relação de conta entre o trabalhador e a instituição financeira. A aplicação do CDC às instituições financeiras é entendimento consolidado do STJ (Súmula 297) [NÃO CONFIRMADO nesta rodada: enunciado não reaberto]. O inciso II do decreto pode alcançar o CAIXA Tem, por ser plataforma digital de serviço financeiro supervisionada pelo BC; o inciso I depende de critérios do regulador que não localizei.
- **A URA 0800 726 0207 mistura as duas relações** no mesmo número. Se a Caixa for fornecedora sujeita ao decreto, as regras de SAC (cinco níveis, humano em todos os níveis, 20 s para 80%) valeriam ao menos para as demandas bancárias. Para as demandas de benefício, a obrigação é discutível. Mesmo onde incidir, o art. 15, § 1º, abre exceção para regra específica do regulador.
- **Conclusão cautelosa:** não é possível afirmar, com as fontes públicas, que os tempos e níveis do Decreto 13.135 são **obrigatórios** para a URA do seguro-desemprego. No blueprint, eles devem aparecer como **referência de qualidade**, com nota de incidência incerta. A Lei 13.460 é o piso seguro. Resolver a dúvida exige consulta à Caixa e ao Banco Central (LAI) sobre o enquadramento do canal.

### d.3 Matriz de escalonamento por natureza da manifestação (F22)

| Natureza da demanda | Primeiro canal | Escalonamento | Prazo de resposta | Regime |
|---|---|---|---|---|
| Benefício: concessão, motivo, valor, número de parcelas | gov.br / CTPS Digital; 158; Sine | Recurso (Res. 957, art. 27); Ouvidoria MTE via Fala.BR | Recurso: informado "em torno de 30 dias" [25]; Lei 9.784, art. 59, § 1º [14]; Ouvidoria: 30 dias (Lei 13.460, art. 16) [15] | Serviço público |
| Pagamento: parcela liberada e não creditada, devolução, reemissão | Caixa (0800, agência, apps) | MTE (reemissão); Ouvidoria Caixa | Não localizado | Serviço público prestado por contratada [INFERÊNCIA] |
| Saque não reconhecido | Caixa (crédito em conta Caixa); banco destinatário; unidade do MTE (demais modalidades) | Análise da Caixa (TR 5.3.14.4) | Lei 9.784 (TR 5.3.14.11) [5] | Misto |
| Conta, cartão, senha, atendimento bancário | SAC Caixa | Ouvidoria Caixa (Res. CMN 4.860/2020) [38]; consumidor.gov.br [37]; Banco Central | SAC: 7 dias corridos se o Decreto incidir (art. 21) [9] | Consumo [INFERÊNCIA] |
| Qualidade do atendimento do 0800 | Ouvidoria Caixa | Fala.BR (a Caixa é administração indireta) | 30 dias (Lei 13.460, art. 16) [15] | Serviço público |

---

## (e) Lacunas e plano de coleta de evidências

**Lacunas que permanecem.**
1. Menu, mensagens e identificação atuais da URA: só há registro de 2018 [36].
2. Operador, contrato e níveis de serviço do 0800 726 0207: não localizados. O Contrato 07/2026 não trata de telefone [5]; a CECOT 121/2026 não tem vínculo provado [33].
3. Tempos de espera e abandono: nenhum dado público.
4. Sistemas, permissões e roteiro do atendente (F20) e acessibilidade da URA (F21).
5. Procedimento de reemissão (F14) e portaria de contestação do art. 20, § 5º: não localizados.
6. Inteiro teor dos Acórdãos 1621/2026 e 135/2024: não aberto nesta rodada.
7. Texto da Portaria Interministerial 70/2002: não aberto (HTTP 403).
8. Anexo V (IMR) e relatórios de fiscalização do Contrato 07/2026.
9. Horários atuais do atendimento humano da Caixa (site em loop de redirecionamento).
10. Enquadramento da Caixa no Decreto 13.135 pelo regulador (d.2).

**Plano de coleta.**

| Evidência | Camada | Situação | Como obter |
|---|---|---|---|
| Contrato 07/2026 com TR; 8º apostilamento do Contrato 11/2021 | Governança | **Pública, obtida** [5][7] | — |
| Res. 957 consolidada | Normativa | **Pública, obtida** [1] | Reconferir no DOU quando o site responder |
| Inteiro teor do Acórdão 1621/2026 (TC 015.553/2025-6) e do 135/2024 (TC 006.464/2022-0) | Governança | Pública, não obtida | Pesquisa de jurisprudência do TCU ou pedido à Ouvidoria do TCU |
| Portaria Interministerial 70/2002 | Normativa | Pública, não obtida | DOU de 14/10/2002 (Imprensa Nacional) |
| Plano de ação do MTE em resposta ao TCU (180 dias contados de 24/06/2026) | Governança | Exige LAI | Pedido ao MTE via Fala.BR |
| Anexo V (IMR) do contrato; relatórios de fiscalização; penalidades | Governança / financeira | Exige LAI | Pedido ao MTE |
| Lotes, comprovantes de transmissão, relatórios de rejeição, conciliação, restituições, reemissões | Financeira | Exige LAI (dados agregados) | Pedido ao MTE e à Caixa, com dados anonimizados (LGPD) |
| Procedimento e prazo de reemissão; portaria de contestação | Normativa / financeira | Exige LAI | Pedido ao MTE |
| Contrato do operador do 0800 726 0207; níveis de serviço | Telefônica / governança | Pública em parte (licitacoes.caixa.gov.br, aba Transparência, cláusula 10.5 do contrato) [5]; se não estiver lá, LAI | Pesquisa no portal da Caixa; pedido LAI à Caixa |
| Tempo médio de espera, taxa de abandono, volume mensal de ligações sobre seguro-desemprego | Telefônica | Exige LAI | Pedido à Caixa |
| Roteiros de atendimento, base de conhecimento, perfis de acesso do atendente | Telefônica / tecnológica | Exige LAI (pode ser negado como informação interna) | Pedido à Caixa |
| Diagrama de arquitetura da URA, integrações, logs, incidentes, plano de contingência | Tecnológica | Só em auditoria formal | Fora do alcance de pesquisa acadêmica |
| Gravação do menu da URA; mensagens; tempo até o humano; protocolo; acessibilidade | Telefônica / evidência física | **Exige ligação de teste** | Roteiro abaixo |
| Enquadramento do canal no Decreto 13.135 | Normativa | Exige LAI | Pedido à Caixa e ao Banco Central |

**Roteiro da ligação de teste.** Fazer pelo menos seis ligações em dias e horários diferentes (incluindo um sábado e uma após as 20h), gravando com aviso, sem informar dados de terceiros. Registrar: opções do 1º nível; número de níveis até a opção de seguro-desemprego; se o humano é oferecido em todos os níveis; dados pedidos na identificação; o que a URA informa; tempo até o atendente; se há protocolo; o que o atendente sabe dizer sobre reemissão, contestação de saque e motivo de bloqueio; para onde encaminha. A consulta a dados pessoais só pode ser feita com o CPF do próprio pesquisador ou de titular que consinta por escrito.

---

## (f) Fontes

1. Res. CODEFAT 957/2022, texto revisado, Portal do FAT (PDF lido em 14/11/2026): https://portalfat.trabalho.gov.br/wp-content/uploads/2026/09/Resolucao-no-957-de-21-de-setembro-de-2022-Revisao-do-SD.pdf
2. Res. CODEFAT 957/2022, DOU (não respondeu nesta data): https://www.in.gov.br/web/dou/-/resolucao-codefat-n-957-de-21-de-setembro-de-2022-431328890
3. Portal do FAT, normas do seguro-desemprego: https://portalfat.mte.gov.br/resolucoes-2/resolucoes-por-assunto/seguro-desemprego/
4. Lei 7.998/1990: https://www.planalto.gov.br/ccivil_03/leis/l7998.htm
5. MTE, Termo de Contrato nº 07/2026 MTE–Caixa, com Termo de Referência (PDF, 32 p.): https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/licitacoes-e-contratos/pca/072026completo.pdf
6. PNCP, registro do Contrato 07/2026 (endereço impresso no PDF da fonte 5; não aberto diretamente): https://pncp.gov.br/app/contratos/23612685000122/2026/000012
7. MTE, 8º Termo de Apostilamento ao Contrato nº 11/2021 MTE–Caixa: https://www.gov.br/trabalho-e-emprego/pt-br/acesso-a-informacao/licitacoes-e-contratos/contratos/8Termo_de_Apostilamento.pdf
8. Portaria Interministerial MTE/MF nº 70/2002, reprodução do DOU de 14/10/2002 indicada por busca (HTTP 403 nesta data) [NÃO CONFIRMADO]: https://simrppn.sisicmbio.icmbio.gov.br/uploads/ato-criacao/2010_06_08/RJ_RPPN_Fattoria_Grigia.pdf
9. Decreto 13.135/2026, Planalto: https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2026/decreto/d13135.htm
10. Decreto 13.135/2026, Senado (Legislação): https://legis.senado.leg.br/norma/44154496/publicacao/44157502
11. Atlas Público, DOU de 13/10/2026 e vigência em 02/11/2026 (secundária): https://atlaspublico.com.br/regulacao/dou/decreto-n-13-135-de-9-de-outubro-de-2026-843116
12. Decreto 11.034/2022 (revogado): https://www.planalto.gov.br/ccivil_03/_Ato2019-2022/2022/Decreto/D11034.htm
13. CDC, Lei 8.078/1990: https://www.planalto.gov.br/ccivil_03/leis/l8078compilado.htm
14. Lei 9.784/1999: https://www.planalto.gov.br/ccivil_03/leis/l9784.htm
15. Lei 13.460/2017: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2017/lei/l13460.htm
16. Lei 14.129/2021: https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2021/lei/l14129.htm
17. LGPD, Lei 13.709/2018: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm
18. Lei 13.146/2015: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2015/lei/l13146.htm
19. Decreto 8.373/2014 (eSocial): https://www.planalto.gov.br/ccivil_03/_ato2011-2014/2014/decreto/d8373.htm
20. TCU, notícia do Acórdão 1621/2026: https://portal.tcu.gov.br/imprensa/noticias/tribunal-avalia-servico-digital-de-seguro-desemprego-para-trabalhadores-formais
21. TCU, sumário executivo da auditoria (24/06/2026): https://portal.tcu.gov.br/publicacoes-institucionais/sumario-executivo/auditoria-seguro-desemprego-emprega-brasil
22. Capital Digital, "TCU determina integração do seguro-desemprego ao eSocial e cobra reforma digital" (06/07/2026; secundária): https://capitaldigital.com.br/tcu-determina-integracao-do-seguro-desemprego-ao-esocial-e-cobra-reforma-digital/
23. TCU, notícia do Acórdão 135/2024: https://portal.tcu.gov.br/imprensa/noticias/inconsistencias-no-seguro-desemprego-causaram-prejuizo-a-administracao-publica
24. Agora RN, cifra de 29.535 pagamentos (via resultado de busca; secundária): https://agorarn.com.br/?p=831572
25. gov.br, Cadastrar recurso relativo ao seguro-desemprego (modificada em 25/09/2026): https://www.gov.br/pt-br/servicos/cadastrar-recurso-relativo-ao-seguro-desemprego
26. gov.br, Perguntas frequentes do Seguro-Desemprego: https://www.gov.br/pt-br/temas/perguntas-frequentes-seguro-desemprego
27. Caixa, FAQ do Seguro-Desemprego (loop de redirecionamento nesta data; conteúdo via resultado de busca): https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx
28. Caixa, Atendimento (horários; via v3; não reaberta): https://www.caixa.gov.br/atendimento/Paginas/default.aspx
29. Caixa, Libras por videochamada: https://www.caixa.gov.br/atendimento/libras/
30. Caixa, app Benefícios Sociais: https://www.caixa.gov.br/atendimento/aplicativos/beneficios-sociais-caixa/Paginas/default.aspx
31. MTE, Central Alô Trabalho 158: https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/inspecao-do-trabalho/acesso-a-informacao/central-alo-trabalho-158
32. Agência Gov, canais do MTE (06/07/2026): https://agenciagov.ebc.com.br/noticias/202607/saiba-como-acessar-os-canais-de-atendimento-do-ministerio-do-trabalho-e-emprego
33. PNCP, CECOT 121/2026 (API): https://pncp.gov.br/api/consulta/v1/orgaos/00360305000104/compras/2026/315
34. O Povo, "Usuários reclamam de atraso no seguro-desemprego" (19/05/2023): https://mais.opovo.com.br/jornal/economia/2023/05/19/usuarios-reclamam-de-atraso-no-seguro-desemprego.html
35. Seu Dinheiro, falha no TED atrasa 45 mil parcelas (19/05/2023): https://www.seudinheiro.com/2023/economia/falha-do-banco-central-atrasa-mais-de-45-mil-parcelas-do-seguro-desemprego-veja-quando-os-beneficios-serao-liberados-lvit
36. Jornal Contábil (2018; registro histórico): https://jornalcontabil.com.br/noticia/seguro-desemprego-fgts-e-pis-tem-novas-datas-de-pagamento/
37. consumidor.gov.br, sobre o serviço: https://www.consumidor.gov.br/pages/conteudo/sobre-servico
38. Res. CMN 4.860/2020 (ouvidoria; cópia secundária): https://www.ancord.org.br/wp-content/uploads/2021/01/ResolucaoBCB-4.860.pdf
39. Res. CODEFAT 392/2004 (revogada; LegisWeb, via resultado de busca): https://www.legisweb.com.br/legislacao/?id=100711
40. Constituição Federal: https://www.planalto.gov.br/ccivil_03/constituicao/constituicao.htm
41. Res. CMN 4.949/2021 (relacionamento com clientes; LegisWeb, secundária): https://www.legisweb.com.br/legislacao/?id=421170
