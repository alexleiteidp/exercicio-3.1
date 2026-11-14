# D — Diagrama da jornada AS-IS

O diagrama traz a jornada decidida no `/grill-me` (`C_grill_transcript.md`) e detalhada em `C_blueprint_asis.md`. São 9 etapas, com as camadas separadas pelas três linhas do blueprint e os 6 fail points (⚠). **Cada seta tem um rótulo** que diz o que passa de um ator ao outro: pedido, dado, transferência ou decisão. A seta de retorno E8 → E3 (FP-E) vem da decisão D2 do aluno: a jornada só termina com a solução.

## 1. Fluxo da jornada com os atores

```mermaid
flowchart TD
    subgraph CID["Ações do Cidadão"]
        E1["E1 Percebe que a parcela não caiu"]
        E2["E2 Procura o motivo nos apps<br/>⚠ FP-D status divergente"]
        E3["E3 Liga para o 0800 726 0207"]
        E4["E4 Identifica-se e ouve o status"]
        E5["E5 Pede atendente e espera na fila<br/>⚠ FP-B desistência (hipótese)"]
        E6["E6 Fala com o atendente"]
        E7["E7 É encaminhado a outro canal"]
        E8["E8 Tenta resolver no canal do MTE"]
        E9["E9 Recebe, desiste ou reclama"]
    end

    subgraph FRONT["Frontstage — acima da Linha de Visibilidade"]
        APP["CTPS Digital / app Benefícios Sociais"]
        URA["URA (voz e menu)<br/>[não confirmado em 2026]<br/>⚠ FP-A sem motivo do indeferimento"]
        ATD["Atendente terceirizado da Caixa<br/>⚠ FP-C encaminha sem histórico"]
        MTEC["gov.br · Central 158 ·<br/>atendimento presencial SRTE/Sine"]
    end

    subgraph BACK["Backstage — abaixo da Linha de Visibilidade"]
        ACD["ACD / roteamento da fila"]
        SPC["Sistema de pagamento da Caixa"]
        PROT["Registro do protocolo"]
    end

    subgraph SUP["Processos de Suporte — abaixo da Linha de Interação Interna"]
        MOTOR["Motor de habilitação MTE/Dataprev"]
        BASES["Bases eSocial · CNIS · FGTS<br/>⚠ FP-F dado errado do empregador"]
        LOTE["Lotes semanais MTE → Caixa<br/>(Res. CODEFAT 957/2022, art. 65)"]
        REC["Análise do recurso pelo MTE"]
        CONTR["Contrato de teleatendimento e fiscal"]
    end

    E1 -->|"parcela não aparece"| E2
    E2 -->|"não entende o status"| E3
    E3 -->|"escolhe a opção"| E4
    E4 -->|"status não basta"| E5
    E5 -->|"chamada atendida"| E6
    E6 -->|"atendente não resolve"| E7
    E7 -->|"segue a orientação"| E8
    E8 -->|"problema resolvido"| E9
    E8 -. "⚠ FP-E não resolveu: religa" .-> E3

    E2 -->|"consulta"| APP
    APP -->|"mostra o status gravado"| E2
    E3 -->|"liga"| URA
    URA -->|"lê o status"| E4
    E5 -->|"pede atendente"| URA
    URA -->|"transborda a chamada"| ACD
    ACD -->|"distribui a chamada"| ATD
    ATD -->|"consulta a parcela"| SPC
    SPC -->|"devolve situação do pagamento"| ATD
    URA -->|"consulta a parcela"| SPC
    ATD -->|"abre"| PROT
    PROT -->|"número de protocolo"| E6
    ATD -->|"orienta: procure o 158 ou o gov.br"| E7
    E8 -->|"pede revisão ou recorre"| MTEC
    MTEC -->|"registra o recurso"| REC

    APP -->|"lê a decisão"| MOTOR
    MOTOR -->|"consulta vínculos"| BASES
    BASES -->|"dado do empregador bloqueia ou libera"| MOTOR
    REC -->|"decisão reprocessa a habilitação"| MOTOR
    MOTOR -->|"habilitação gera parcelas"| LOTE
    LOTE -->|"envia ordens de pagamento"| SPC
    SPC -->|"credita a parcela"| E9
    CONTR -->|"dimensiona a fila"| ACD
    CONTR -->|"define o que o atendente pode fazer"| ATD
```

## 2. Quem passa o quê a quem (handoffs entre atores)

| De | Para | O que passa | Etapa | Fail point |
|---|---|---|---|---|
| Cidadão | CTPS Digital / app Benefícios Sociais | Consulta do status | E2 | FP-D |
| Cidadão | URA | Ligação e CPF/NIS | E3–E4 | FP-A |
| URA | Sistema de pagamento da Caixa | Consulta da parcela [não confirmado em 2026] | E4 | FP-D |
| URA | ACD / roteamento da fila | Transbordo para atendente | E5 | FP-B |
| ACD | Atendente terceirizado | Distribuição da chamada | E5–E6 | — |
| Atendente | Sistema de pagamento da Caixa | Consulta da situação do pagamento | E6 | — |
| Atendente | Registro do protocolo | Abertura do protocolo | E6 | FP-C |
| Atendente | Cidadão | Orientação "procure o 158 ou o gov.br" | E7 | FP-C |
| Cidadão | gov.br / Central 158 / SRTE ou Sine | Pedido de revisão ou recurso | E8 | FP-E |
| gov.br / SRTE ou Sine | Análise do recurso pelo MTE | Recurso registrado | E8 | — |
| Análise do recurso | Motor de habilitação MTE/Dataprev | Decisão que reprocessa | E8 | — |
| Bases eSocial/CNIS/FGTS | Motor de habilitação | Dado de vínculo do empregador | Suporte | FP-F |
| Motor de habilitação | Lotes semanais MTE → Caixa | Parcelas habilitadas | Suporte | — |
| Lotes semanais | Sistema de pagamento da Caixa | Ordens de pagamento | Suporte | FP-D (causa: "pago" antes do crédito) |
| Sistema de pagamento da Caixa | Cidadão | Crédito na conta | E9 | — |
| Contrato de teleatendimento e fiscal | ACD e atendente | Dimensionamento da fila e escopo do atendimento | Suporte | FP-B |

## Como ler

- **Setas sólidas com rótulo:** o caminho normal e cada passagem entre atores.
- **Seta tracejada E8 → E3 (FP-E):** a peregrinação. Quando o canal do MTE não resolve, o cidadão volta a ligar para a URA.
- **⚠:** os 6 fail points decididos na Rodada 4 (D7) e ajustados na Rodada 7 (D13, D14).
