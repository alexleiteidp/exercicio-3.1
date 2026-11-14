# C — Service Blueprint AS-IS

**Serviço:** Atendimento ao Seguro-Desemprego pela URA da Caixa (0800 726 0207).
**Situação retratada:** o trabalhador formal, dispensado sem justa causa, percebe que a parcela não caiu. O retrato é de **como o serviço funciona hoje** (novembro de 2026), não de como deveria funcionar.
**Metodologia:** Service Blueprint de G. Lynn Shostack (1984), com 5 camadas e 3 linhas.
**Base:** `B_relatorio_assistente_v3.md` e as decisões D1 a D12 de `C_grill_transcript.md`.

## Decisões do grill que moldam o blueprint

| Decisão | Efeito no blueprint |
|---|---|
| D1 | A jornada começa **antes da ligação**, no gatilho (E1) e na tentativa frustrada no app (E2). |
| D2 | A jornada só termina com a **solução** ou com um **encaminhamento satisfatório**. O aluno divergiu da recomendação do agente, que parava no fim da ligação. Por isso há o laço E8 → E3. |
| D3 | A **Linha de Visibilidade** deixa acima a voz da URA, o atendente e as mensagens. A tela do sistema de pagamento da Caixa fica abaixo, no backstage. |
| D4 / D9 | A **Linha de Interação Interna** separa o backstage (ACD, sistema de pagamento da Caixa, protocolo) dos Processos de Suporte (motor de habilitação MTE/Dataprev, bases eSocial/CNIS/FGTS, lotes semanais, análise do recurso pelo MTE, contrato de teleatendimento e fiscal). |
| D5 / D6 | São **9 etapas**. O retorno E8 → E3 é uma seta marcada como fail point (FP-E). |
| D7 | São **6 fail points**, de FP-A a FP-F. |
| D8 | São **9 evidências físicas**, uma por etapa. |
| D10 | O que a URA faz sem prova atual aparece marcado **[não confirmado em 2026]**. |
| D11 | O frontstage do E8 tem o gov.br, a CTPS Digital, a Central 158 e a SRTE/Sine. |

## Blueprint (etapas em colunas, camadas em linhas)

| Camada | E1 Percebe que a parcela não caiu | E2 Procura o motivo nos apps | E3 Liga para o 0800 e ouve o menu da URA | E4 Identifica-se e ouve o status automático | E5 Pede atendente e espera na fila | E6 Fala com o atendente | E7 É encaminhado a outro canal | E8 Tenta resolver no canal do MTE | E9 Recebe, desiste ou reclama |
|---|---|---|---|---|---|---|---|---|---|
| **1. Evidências Físicas** | Extrato ou saldo zerado no CAIXA Tem | Tela da CTPS Digital ou do app Benefícios Sociais | Número 0800 726 0207 | Voz e menu gravado da URA | Música e mensagem de espera | Número de protocolo do atendimento | Orientação verbal: "procure o 158 ou o gov.br" | Tela do recurso no gov.br | Crédito na conta ou notificação no app |
| **2. Ações do Cidadão** | Consulta o saldo no dia previsto e não vê o crédito | Abre a CTPS Digital ou o app Benefícios Sociais e não entende o status ⚠ **FP-D** | Disca o 0800 e escolhe a opção do seguro-desemprego | Digita CPF/NIS e ouve o status | Pede para falar com um atendente e espera ⚠ **FP-B** | Explica o caso ao atendente | Anota o canal indicado e desliga | Entra no gov.br ou na CTPS Digital, liga para a Central 158 ou vai à SRTE/Sine ↩ ⚠ **FP-E** (volta ao E3) | Recebe a parcela, desiste ou reclama |
| ═══ *Linha de Interação* ═══ | | | | | | | | | |
| **3. Frontstage** (visível) | — (nenhum contato com o serviço) | Telas do app: status da parcela e mensagens | Voz da URA: saudação e menu | Voz da URA lê o status [não confirmado em 2026] ⚠ **FP-A** | Mensagem gravada de espera; transbordo para atendente | Atendente terceirizado da Caixa | Atendente indica o canal do MTE ⚠ **FP-C** | gov.br, CTPS Digital, Central 158, atendimento presencial na SRTE ou no Sine | Crédito no CAIXA Tem; notificação da decisão no app |
| ═══ *Linha de Visibilidade* ═══ | | | | | | | | | |
| **4. Backstage** (invisível) | — | Leitura do status gravado pelo motor de habilitação | URA (sistema automatizado) recebe a chamada | URA consulta a base de pagamento da Caixa | ACD/roteamento da fila distribui a chamada | Atendente consulta o sistema de pagamento da Caixa (só pagamento, não a concessão) | Registro do protocolo, sem vínculo com a demanda no MTE ⚠ **FP-C** | Registro do recurso no sistema do MTE | Caixa registra o crédito |
| ═══ *Linha de Interação Interna* ═══ | | | | | | | | | |
| **5. Processos de Suporte** | Lote semanal de pagamento MTE → Caixa (Res. CODEFAT 957/2022, art. 65) | Motor de habilitação MTE/Dataprev cruza eSocial, CNIS e FGTS ⚠ **FP-F** | Contrato de teleatendimento e fiscal do contrato definem a capacidade | Base de pagamento da Caixa, alimentada pelos lotes do MTE ⚠ **FP-D** | Contrato de teleatendimento (dimensionamento) e fiscal | Contrato de teleatendimento define o que o atendente pode consultar | — | Análise do recurso pelo MTE; correção do dado do empregador no eSocial ⚠ **FP-F** | Novo lote semanal MTE → Caixa, se o recurso for deferido |

## As três linhas

- **Linha de Interação:** separa o que o cidadão faz (camada 2) do que o serviço mostra a ele (camada 3).
- **Linha de Visibilidade:** separa o que o cidadão vê ou ouve diretamente da retaguarda. Acima dela ficam a voz da URA, o atendente, as mensagens e as telas dos apps. A tela do atendente fica abaixo (D3).
- **Linha de Interação Interna:** separa quem trabalha para esta ligação (backstage) do que existe independentemente dela (Processos de Suporte), conforme D9.

## Fail points

| # | Fail point | Etapa | Camada | Quem responde | Evidência (v3) |
|---|---|---|---|---|---|
| FP-A | A URA informa que o benefício foi negado, mas não explica o motivo | E4 | Frontstage | Caixa (canal) e MTE (decisão) | Mapa 2.1; pesquisa v3; achado do TCU sobre decisões sem motivo claro (Acórdão 1621/2026) |
| FP-B | O cidadão desiste na fila antes de falar com o atendente | E5 | Ações do cidadão | Caixa, contrato de teleatendimento e fiscal | Hipótese a testar: não há dado público de abandono [NÃO CONFIRMADO] |
| FP-C | O atendente só consulta o pagamento e manda o cidadão para outro canal. A demanda passa sem histórico e sem protocolo ligado a ela | E6 / E7 | Frontstage e backstage | Caixa e MTE | TCU 1621/2026: trabalhador "encaminhado de um lugar para outro" |
| FP-D | O status do app e o da URA não batem com o crédito real | E2 / E4 | Ações do cidadão e suporte | MTE e Caixa | TCU 1621/2026 (divergência de informação de pagamento); auditoria v1, F17 |
| FP-E | Laço E8 → E3: o encaminhamento não resolve e o cidadão volta a ligar | E8 → E3 | Ações do cidadão | Caixa e MTE | Consequência da decisão D2 do aluno |
| FP-F | Um dado errado do empregador no eSocial ou no CNIS bloqueia a parcela | E2 / E8 | Processos de suporte | Empregador e MTE/Dataprev | Res. CODEFAT 957/2022, art. 4º, § 1º; TCU 1621/2026 (integração com o eSocial) |

## Pontos marcados como não confirmados (D10)

- **E4:** não há fonte de 2026 que comprove que a URA lê o status e a data da parcela. A descrição vem de 2018. Como confirmar: uma ligação de teste gravada ou um pedido de acesso à informação à Caixa (Lei 12.527/2011).
- **E5:** não há dado público sobre o tempo de espera e o abandono da fila. Como confirmar: pedido pela LAI sobre os relatórios do contrato de teleatendimento.
