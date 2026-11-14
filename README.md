# Exercício 3.1 — Service Blueprint AS-IS de um Serviço Público

**Aluno:** Alexander Andrade Leite
**Disciplina:** IDP-TD 2026 — Governo Digital e Transformação de Serviços Públicos no Brasil
**Serviço:** Atendimento ao Seguro-Desemprego pela URA da Caixa (0800 726 0207). Órgãos: Caixa Econômica Federal e Ministério do Trabalho e Emprego. Continua o mapa de atores do exercício 2.1.

## Assistentes usados

| Papel | Assistente |
|---|---|
| Assistente 1 (meta-prompt, pesquisa v1, v2 e v3) | Claude (Anthropic, Claude Opus 5.5), com busca web |
| Assistente 2 (auditorias v1 e v2) | ChatGPT (OpenAI), sem login |
| Sessão `/grill-me` | Claude Code, com a skill `grill-me` (7 rodadas, 14 perguntas) |

## Índice

1. [A_meta_prompt.md](A_meta_prompt.md): meta-prompt (Parte A)
2. [B_relatorio_assistente_v1.md](B_relatorio_assistente_v1.md): pesquisa inicial do assistente 1
3. [B_relatorio_auditoria_v1.md](B_relatorio_auditoria_v1.md): auditoria adversarial da v1 pelo assistente 2
4. [B_relatorio_assistente_v2.md](B_relatorio_assistente_v2.md): v2, que trata cada falha da auditoria v1 como corrigida, defendida ou pendente
5. [B_relatorio_auditoria_v2.md](B_relatorio_auditoria_v2.md): segunda auditoria
6. [B_relatorio_assistente_v3.md](B_relatorio_assistente_v3.md): versão final, com cada delta ligado ao gatilho da auditoria v2
7. [C_grill_transcript.md](C_grill_transcript.md): transcript do `/grill-me`, com 7 rodadas e as decisões D1 a D14
8. [C_blueprint_asis.md](C_blueprint_asis.md): Service Blueprint AS-IS (5 camadas, 3 linhas, 9 etapas, 6 fail points)
9. [D_diagrama_asis.md](D_diagrama_asis.md): diagrama mermaid da jornada AS-IS
