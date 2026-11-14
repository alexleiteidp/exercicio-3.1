# D — Diagrama da jornada AS-IS

O diagrama traz a jornada decidida no `/grill-me` (`C_grill_transcript.md`) e detalhada em `C_blueprint_asis.md`. São 9 etapas, com as camadas separadas pelas três linhas do blueprint e os 6 fail points (⚠). A seta de retorno E8 → E3 (FP-E) vem da decisão D2 do aluno: a jornada só termina com a solução.

```mermaid
flowchart TD
    subgraph CID["Ações do Cidadão"]
        E1["E1 Percebe que a parcela não caiu"]
        E2["E2 Procura o motivo nos apps<br/>⚠ FP-D status divergente"]
        E3["E3 Liga para o 0800 726 0207"]
        E4["E4 Identifica-se e ouve o status"]
        E5["E5 Pede atendente e espera na fila<br/>⚠ FP-B desistência"]
        E6["E6 Fala com o atendente"]
        E7["E7 É encaminhado a outro canal"]
        E8["E8 Tenta resolver no canal do MTE"]
        E9["E9 Recebe, desiste ou reclama"]
    end

    subgraph FRONT["Frontstage — acima da Linha de Visibilidade"]
        APP["Telas da CTPS Digital / app Benefícios Sociais"]
        URA["Voz da URA: menu e status<br/>[não confirmado em 2026]<br/>⚠ FP-A sem motivo do indeferimento"]
        ATD["Atendente terceirizado da Caixa<br/>⚠ FP-C encaminha sem histórico"]
        MTEC["gov.br · CTPS Digital · Central 158 · SRTE/Sine"]
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

    E1 --> E2 --> E3 --> E4 --> E5 --> E6 --> E7 --> E8 --> E9
    E8 -. "⚠ FP-E não resolveu: religa" .-> E3

    E2 --> APP
    E3 --> URA
    E4 --> URA
    E5 --> ACD
    E6 --> ATD
    E7 --> ATD
    E8 --> MTEC

    URA --> SPC
    ATD --> SPC
    ATD --> PROT
    ACD --> ATD
    APP --> MOTOR

    SPC --> LOTE
    LOTE --> MOTOR
    MOTOR --> BASES
    MTEC --> REC
    REC --> MOTOR
    CONTR --> ACD
    LOTE --> E9
```

## Como ler

- **Setas sólidas:** o caminho normal e as dependências. Cada ação do cidadão aciona um ponto do frontstage. O frontstage depende do backstage, e o backstage depende dos processos de suporte.
- **Seta tracejada E8 → E3 (FP-E):** a peregrinação. Quando o canal do MTE não resolve, o cidadão volta a ligar para a URA.
- **⚠:** os 6 fail points decididos na Rodada 4 (D7).
