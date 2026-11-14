# B — Auditoria v1 (assistente 2)

> **Assistente 2:** ChatGPT (OpenAI), usado sem login no navegador embutido do Claude Desktop. É um modelo diferente do assistente 1 (Claude).
> **Data:** 14/11/2026.
> **Entrada:** o prompt adversarial do tutorial (passo B2) seguido do texto integral de `B_relatorio_assistente_v1.md`.
> **Tratamento:** o texto abaixo é a resposta do ChatGPT, copiada na íntegra. Só converti tabelas e listas para Markdown e retirei os rótulos de link da interface (ex.: "Tribunal de Contas da União +1"), que marcavam as fontes citadas.

---

# Auditoria rigorosa — Atendimento ao Seguro-Desemprego pela URA da CAIXA (0800 726 0207)

**Data de referência:** 14/11/2026
**Objeto:** verificar a precisão factual, a completude operacional, a sustentação documental e a identificação dos riscos da pesquisa apresentada.

## 1. Resultado executivo

A pesquisa tem uma boa estrutura de jornada de serviço, identifica corretamente a separação institucional entre concessão do benefício e pagamento e reconhece várias limitações de evidência.

Entretanto, há problemas importantes. O mais grave é que ela mistura três objetos diferentes:

1. O processamento e a concessão do seguro-desemprego pelo MTE.
2. A execução financeira e o atendimento bancário pela CAIXA.
3. O atendimento telefônico específico da URA 0800 726 0207.

Esses objetos se relacionam, mas não são intercambiáveis. Uma auditoria do serviço telefônico precisa demonstrar quais informações a URA efetivamente consulta, quais transações consegue realizar, quais sistemas estão integrados e quais ocorrências consegue resolver. A pesquisa não demonstra isso.

Há também uma deficiência particularmente relevante: o Acórdão 1621/2026 do TCU contém achados operacionais muito mais específicos do que os reproduzidos no relatório, inclusive problemas de mensagens de erro, notificações, informações de pagamento, limitações do formulário de recurso e ausência de acompanhamento adequado. Esses achados deveriam ter sido incorporados à análise.

**Conclusão:** auditoria incompleta. Necessita revisão documental.

**Critério de gravidade:**

- **Alta:** erro que pode alterar a compreensão do funcionamento, dos direitos do usuário ou da responsabilidade institucional.
- **Média:** omissão ou inferência que compromete a análise operacional ou a identificação de riscos.
- **Baixa:** imprecisão localizada, com impacto limitado na conclusão.

A seguir, separo falhas demonstráveis de lacunas que não podem ser tratadas como erros factuais sem documentação adicional.

## 2. Falhas identificadas

### F1 — O Acórdão 1621/2026 foi subutilizado (Alta)

**Trecho auditado:** "O TCU confirmou em 2026 os fail points do canal. O Acórdão 1621/2026 aponta canais que não resolvem com rapidez, falta de base de conhecimento única e trabalhador 'encaminhado de um lugar para outro'."

**Problema:** O acórdão é muito mais abrangente. Ele avaliou o serviço digital do seguro-desemprego do trabalhador formal, incluindo o Portal Emprega Brasil e a Carteira de Trabalho Digital. Entre os achados e encaminhamentos estão:

- Mensagens de erro e decisões que não explicam adequadamente o motivo.
- Ausência de orientação específica sobre como corrigir inconsistências em bases externas.
- Falta de informação sobre sincronização e reprocessamento de dados.
- Ausência de memória de cálculo em situações pertinentes.
- Informações insuficientes sobre procedimentos de pagamento atrasado ou não liberado.
- Falta de informação sobre o estágio e o prazo dos recursos.
- Limitação do campo de justificativa a 500 caracteres.
- Limite de 1 MB por anexo.
- Necessidade de protocolar o recurso antes da juntada completa dos documentos.
- Divergência entre as informações de pagamento apresentadas ao trabalhador e a situação real do crédito.
- Ausência de notificações automáticas sobre eventos importantes.

Esses pontos constam do dispositivo e dos encaminhamentos do Acórdão 1621/2026-TCU-Plenário. [fonte: Tribunal de Contas da União]

**Por que é uma falha:** a pesquisa utiliza o TCU como confirmação genérica de problemas de atendimento, mas deixa de extrair justamente os achados que permitiriam construir uma análise mais precisa dos pontos de ruptura da jornada.

**Correção necessária:** acrescentar os achados do TCU à matriz de falhas, distinguindo os que afetam diretamente o atendimento telefônico daqueles que afetam os sistemas digitais e o processo de pagamento.

### F2 — Confusão entre agente pagador e agente operador (Alta)

**Trecho auditado:** "O MTE concede o benefício, com habilitação automática [...] A Caixa paga: é o agente pagador."

**Problema:** A divisão está parcialmente correta, mas simplifica excessivamente as atribuições da CAIXA. A Resolução CODEFAT 957/2022, art. 64, § 1º, designa a CAIXA como agente pagador. Entretanto, existe também a Portaria Interministerial 70/2002, que instituiu a CAIXA como agente operador do seguro-desemprego e atribuiu competências operacionais próprias. A distinção entre agente operador e agente pagador é relevante para uma auditoria de processos.

A pesquisa deveria ter examinado:

- Quais operações cabem à CAIXA na qualidade de agente operador.
- Quais operações são executadas pelo MTE.
- Quais sistemas são mantidos ou operados pela Dataprev.
- Quais responsabilidades decorrem do contrato de prestação de serviços bancários.
- Quem responde por inconsistências de processamento, disponibilização e pagamento.

A Resolução 957 confirma a atribuição de pagamento, mas não é suficiente para descrever toda a arquitetura institucional. [fonte: Portal do FAT]

**Correção necessária:** incluir a Portaria Interministerial 70/2002 e distinguir formalmente as funções de gestão, operação, processamento tecnológico e pagamento.

### F3 — A jornada telefônica foi descrita com funcionalidades não comprovadas (Alta)

**Trecho auditado:** "URA informa se o requerimento foi liberado, se a parcela está agendada ou paga e a data da próxima."

**Problema:** A pesquisa utiliza uma matéria de 2018 como evidência de identificação e consulta telefônica, mas apresenta a descrição como se fosse uma funcionalidade atual da URA. Não foi apresentada documentação da CAIXA que confirme, em novembro de 2026:

- A existência dessa opção específica.
- A sequência atual do menu.
- Os campos de identificação exigidos.
- A consulta ao status de cada parcela.
- A leitura da data de pagamento.
- A possibilidade de consulta por CPF ou NIS.
- A existência de consulta automatizada ou transferência para atendente.

A própria pesquisa reconhece que o menu atual não foi confirmado.

**Por que é uma falha:** não se pode transformar uma descrição histórica em uma especificação funcional atual.

**Correção necessária:** classificar essas funcionalidades como não verificadas e exigir gravação da URA, teste de chamadas e documentação funcional da CAIXA.

### F4 — A pesquisa não distingue os diferentes canais oficiais de consulta (Média)

**Trecho auditado:** "A URA 0800 726 0207 fica do lado do pagamento."

**Problema:** A FAQ atual da CAIXA informa que o trabalhador pode consultar a liberação das parcelas por diversos canais:

- Aplicativo Benefícios Sociais CAIXA.
- CAIXA Tem.
- Portal Cidadão.
- Carteira de Trabalho Digital.
- Atendimento pelo 0800 726 0207.
- Portal Emprega Brasil.

Portanto, a URA não deve ser analisada isoladamente como se fosse a única interface de consulta da camada financeira. Também é importante observar que a FAQ atribui ao MTE a definição do número de parcelas e dos respectivos valores. [fonte: Caixa]

**O que faltou:** mapear as interfaces, as informações apresentadas em cada uma e a possibilidade de divergência entre elas. Esse ponto ganha importância diante do achado do TCU sobre divergências entre informações de pagamento exibidas e a situação real do crédito.

### F5 — O relatório não identifica adequadamente a diferença entre disponibilização, pagamento e saque (Alta)

**Trecho auditado:** "A 1ª parcela 30 dias após o requerimento e as demais a cada 30 dias."

**Problema:** A afirmação é compatível com o art. 12 da Resolução 957/2022, mas está incompleta para explicar operacionalmente um atraso. É necessário distinguir:

- Data de emissão da parcela.
- Data de disponibilização para saque.
- Data em que o crédito é efetivamente realizado.
- Data em que o trabalhador consulta o saldo.
- Data em que o valor é efetivamente sacado.

O art. 20 estabelece as modalidades de crédito e a responsabilidade pelas informações bancárias. O art. 21 estabelece o período de disponibilidade de 67 dias. Esses eventos não são equivalentes. [fonte: Portal do FAT]

**Por que é uma falha:** a pesquisa trata o evento percebido pelo cidadão — ausência de crédito — como se fosse um único evento técnico. Isso dificulta identificar se o problema ocorreu na geração do documento, na transmissão, na liquidação, na conta de destino ou na consulta.

### F6 — O fluxo de devolução dos valores ao FAT foi simplificado incorretamente (Média)

**Trecho auditado:** "Prazo de 67 dias e devolução ao FAT (art. 21)."

**Problema:** O relatório mistura dois dispositivos:

- **Art. 21:** determina que a parcela fique disponível durante 67 dias, após os quais deve ser devolvida ao FAT.
- **Art. 65:** disciplina o fechamento dos lotes, a apuração de documentos pagos e não pagos e a restituição dos saldos.

O art. 65, § 4º, também determina que os documentos pagos e não pagos sejam informados diretamente ao sistema informatizado, permitindo ao MTE gerenciar os lotes e atestar os serviços. O fluxo financeiro e a prestação de contas, portanto, são mais detalhados do que a descrição apresentada. [fonte: Portal do FAT]

**O que faltou:** identificar o processo de conciliação entre documentos emitidos, valores disponibilizados, pagamentos confirmados, parcelas não sacadas e restituições. Esse é um backstage essencial para investigar divergências entre o status apresentado ao trabalhador e o crédito efetivamente realizado.

### F7 — O Decreto 13.135/2026 foi tratado sem resolver sua aplicabilidade (Alta)

**Trecho auditado:** "O Decreto 13.135/2026 serve de parâmetro." E: "Se ele se aplica à URA do seguro-desemprego é [INFERÊNCIA]."

**Problema:** O decreto existe. A Câmara dos Deputados confirma que foi publicado no DOU em 13/10/2026. Sua vigência, conforme a publicação original, começa 20 dias depois da publicação. Portanto, em 14/11/2026, já está vigente. [fonte: Portal da Câmara dos Deputados]

Entretanto, o ponto decisivo é o âmbito de aplicação. O art. 1º regulamenta o SAC nas relações de consumo. O fato de a CAIXA prestar um serviço público como agente pagador não demonstra, por si só, que toda a operação da URA esteja submetida a esse regime. A pesquisa deveria investigar a natureza jurídica da relação de atendimento em cada hipótese, a incidência do CDC, a regulamentação setorial e a condição da CAIXA como prestadora do serviço bancário.

Outro problema: o relatório atribui ao art. 16 a regra dos cinco níveis de menu. No texto do decreto, o art. 16 trata especificamente dos canais telefônicos; há também disposição correspondente para canais eletrônicos no art. 13.

**Correção necessária:** fazer uma análise jurídica de incidência, em vez de usar os dispositivos como obrigações já comprovadamente aplicáveis.

### F8 — O parâmetro de 20 segundos foi apresentado sem a ressalva sobre exceções (Média)

**Trecho auditado:** "Até 20 s para 80% das chamadas."

**Problema:** O art. 15, I, do Decreto 13.135/2026 estabelece até 20 segundos para pelo menos 80% das demandas atendidas e até 300 segundos para as demais. Entretanto, o § 1º prevê exceção quando houver regra específica disciplinada pelas agências ou órgãos reguladores competentes. Além disso, o decreto prevê que a pessoa humana seja oferecida em todos os níveis do atendimento telefônico, e que a chamada seja transferida ao setor competente quando o primeiro atendente não puder resolver a demanda. [fonte: Anvisa Legis]

**O que faltou:** examinar a ressalva regulatória e verificar como o indicador seria calculado, qual seria o universo de chamadas e se chamadas abandonadas entrariam no denominador. A aplicação à URA específica continua dependendo da conclusão jurídica de F7.

### F9 — A pesquisa atribui o processamento automático a uma arquitetura tecnológica não demonstrada (Média)

**Trecho auditado:** "Motor de habilitação (MTE/Dataprev) grava o status e a notificação."

**Problema:** O art. 4º, § 1º, da Resolução 957 estabelece que os critérios de habilitação são aferidos automaticamente pelo sistema do seguro-desemprego, a partir de informações de bases determinadas. O dispositivo não identifica, por si só, qual componente de software executa cada operação, quem mantém o motor de regras, qual sistema persiste as notificações ou qual serviço tecnológico transmite o resultado à CAIXA. A atribuição ao MTE/Dataprev é plausível, mas precisa de documentação arquitetural, contratual ou técnica.

**Correção necessária:** separar obrigação normativa de implementação tecnológica. [fonte: Portal do FAT]

### F10 — A análise da notificação digital omite uma condição fundamental (Média)

**Trecho auditado:** "Notificação só digital, mediante anuência (Res. 957, art. 8º)."

**Problema:** O relatório acerta ao identificar a necessidade de anuência e cadastro no gov.br ou na Carteira de Trabalho Digital. Entretanto, não examina as consequências operacionais dessa condição:

- Como a anuência é registrada?
- Como o trabalhador é informado de que existe uma notificação?
- Como se comprova a disponibilização?
- O que ocorre quando o usuário não acessa o aplicativo?
- Como são tratadas falhas de entrega?
- Como o sistema registra a ciência da decisão?

O art. 8º permite notificações exclusivamente digitais nas condições nele estabelecidas. Isso não equivale a comprovar que o usuário tomou conhecimento efetivo da decisão. [fonte: Portal do FAT]

**Importância:** a notificação é um evento que pode iniciar a contagem de prazos de defesa e recurso. Sua confiabilidade precisa ser auditada.

### F11 — A duplicidade Empregador Web × eSocial foi descrita de forma imprecisa (Média)

**Trecho auditado:** "Duplicidade Empregador Web × eSocial, que gera bloqueios e indeferimentos."

**Problema:** O Acórdão 1621/2026 determina a integração do serviço ao eSocial, com centralização das obrigações trabalhistas e eliminação da exigência de entrada duplicada em sistemas paralelos. A determinação é mais específica do que a formulação do relatório. O TCU também destaca a necessidade de processamento tempestivo de eventos que impactam o benefício, inclusive nos casos de readmissão. [fonte: Tribunal de Contas da União]

**O que faltou:**

- Identificar quais eventos são duplicados.
- Identificar quais sistemas recebem cada informação.
- Distinguir duplicidade de informação de divergência entre bases.
- Identificar o momento em que a inconsistência provoca bloqueio.
- Examinar o prazo de sincronização entre sistemas.
- Verificar se a regularização do vínculo provoca reprocessamento automático ou exige intervenção.

**Correção necessária:** construir um fluxo específico de tratamento de inconsistências cadastrais, em vez de tratar a duplicidade como uma causa genérica de indeferimento.

### F12 — A análise do TCU 135/2024 não é suficiente para sustentar o fail point FP5 (Média)

**Trecho auditado:** "TCU 135/2024: cerca de 4 mil recursos por ano sobre pedidos já com dois recursos negados."

**Problema:** O Acórdão 135/2024 trata de inconsistências e pagamentos potencialmente irregulares, mas também identifica problemas de governança dos recursos administrativos. O documento registra, entre seus achados:

- Ausência de instância revisora.
- Possibilidade de múltiplos recursos.
- Falta de avaliação contínua e sistemática dos resultados dos recursos administrativos.
- Problemas de controle de pagamentos indevidos.

Também identifica indícios de pagamentos irregulares superiores a R$ 1 bilhão em um dos achados e 29.535 pagamentos a requerentes com vínculos formais com a Administração Pública, no valor de R$ 147 milhões. [fonte: Tribunal de Contas da União]

O relatório apresenta uma estatística de aproximadamente quatro mil recursos anuais sem contextualizar suficientemente sua origem, universo, período e relação com a população de recursos.

**Por que é uma falha:** um número isolado não demonstra lentidão, taxa de insucesso ou reincidência de recursos.

**Correção necessária:** utilizar o inteiro teor do acórdão e distinguir volume de recursos, demora de análise, ausência de revisão e pagamentos indevidos.

### F13 — A pesquisa não examina o contrato de prestação dos serviços bancários (Alta)

**Trecho auditado:** "Níveis de serviço do contrato [NÃO CONFIRMADO]."

**Problema:** A própria Resolução 957/2022 contém um elemento documental que deveria ter orientado a investigação. O art. 66 estabelece que os serviços bancários realizados para pagamento dos benefícios serão remunerados conforme contrato firmado com o Ministério do Trabalho e Previdência. Isso indica uma relação contratual operacional entre o Ministério e o agente pagador. O relatório cita a licitação CECOT 121/2026, mas não demonstra que tenha investigado o contrato específico de execução dos pagamentos do seguro-desemprego. [fonte: Portal do FAT]

**Documentos que faltaram:**

- Contrato MTE–CAIXA referente à execução bancária do benefício.
- Termo de referência e anexos técnicos.
- Indicadores de desempenho contratual.
- Metas de disponibilidade dos sistemas.
- Prazos de processamento e conciliação.
- Procedimentos para falhas de pagamento.
- Relatórios de fiscalização contratual.
- Registros de incidentes e penalidades.
- Regras de remuneração por transação.

**Importância:** a licitação de atendimento multimeios da CAIXA não substitui a investigação do contrato específico que sustenta a operação financeira do benefício.

### F14 — A análise de reemissão não identifica o procedimento administrativo previsto na norma (Média)

**Trecho auditado:** "Parcela devolvida ao FAT após 67 dias; canal de reemissão não documentado."

**Problema:** O art. 21, § 2º, da Resolução 957 estabelece que a parcela devolvida pode ser reemitida mediante solicitação do beneficiário ou decisão judicial, no prazo de até dois anos. O relatório identifica a possibilidade, mas não investiga como essa solicitação é operacionalizada. Deveria examinar:

- Qual canal recebe a solicitação.
- Qual unidade analisa o pedido.
- Como é verificado se a parcela foi devolvida.
- Como é impedido o pagamento em duplicidade.
- Como é gerada uma nova ordem de pagamento.
- Como o trabalhador acompanha a reemissão.
- Qual é o prazo de processamento.
- Como o sistema informa a decisão.

Há ainda uma questão importante: o prazo de dois anos não significa que o trabalhador tenha necessariamente dois anos para fazer qualquer solicitação sem outras condições. O dispositivo estabelece o prazo máximo para a possibilidade de reemissão, contado da emissão de cada parcela. [fonte: Portal do FAT]

### F15 — A pesquisa não analisa a contestação de pagamento não reconhecido (Alta)

**Trecho auditado:** "Recebe, desiste ou reclama."

**Problema:** A Resolução 957, art. 20, § 5º, prevê que o trabalhador que não confirmar o recebimento de parcelas pode contestar o recebimento por procedimento administrativo. Esse é um fluxo operacional diferente da reemissão de parcela não sacada. A pesquisa não o separa adequadamente. São situações distintas:

- A parcela foi disponibilizada, mas não foi sacada.
- O pagamento foi registrado como realizado, mas o trabalhador afirma não ter recebido.
- O valor foi creditado em conta diferente daquela esperada.
- O crédito foi realizado, mas não está visível no canal consultado.
- O trabalhador não reconhece a operação.

Cada cenário demanda investigação e tratamento diferentes.

**O que faltou:** examinar o procedimento administrativo de contestação, sua regulamentação complementar, seus controles antifraude e a responsabilidade pela apuração. [fonte: Portal do FAT]

### F16 — A pesquisa não identifica os pontos de falha da transmissão de dados entre MTE e CAIXA (Alta)

**Trecho auditado:** "O MTE processa os documentos de pagamento em lotes semanais e os entrega à Caixa."

**Problema:** A afirmação reproduz corretamente o art. 65, mas a descrição não representa um fluxo técnico auditável. A norma demonstra a existência de lotes semanais e a comunicação dos documentos ao agente pagador. Não demonstra como essa comunicação ocorre tecnicamente. Uma análise operacional deveria identificar, pelo menos:

- Geração do lote.
- Validação dos registros.
- Identificação única das parcelas.
- Transmissão ao agente pagador.
- Confirmação de recebimento do arquivo.
- Rejeição de registros inconsistentes.
- Reprocessamento de registros rejeitados.
- Processamento das ordens de pagamento.
- Retorno dos resultados.
- Conciliação entre os registros do MTE e da CAIXA.

**Fail points omitidos:**

- Lote gerado incorretamente.
- Registro ausente no lote.
- Arquivo transmitido, mas não recebido.
- Registro rejeitado por inconsistência.
- Processamento parcial do lote.
- Retorno de pagamento não processado.
- Atualização tardia do status no sistema do MTE.
- Divergência entre o banco de dados da CAIXA e o aplicativo do trabalhador.

**Por que é importante:** o art. 65, § 4º, prevê a comunicação dos documentos pagos e não pagos ao sistema informatizado. Essa comunicação é um ponto de controle essencial, mas a pesquisa não a transforma em objeto de auditoria. [fonte: Portal do FAT]

### F17 — O fail point da informação divergente sobre pagamento não foi incorporado à matriz (Alta)

**Trecho auditado:** "FP7 — Falha na liquidação financeira atrasa parcelas em massa."

**Problema:** O relatório concentra o risco de pagamento em uma falha de liquidação financeira, exemplificada pelo episódio de maio de 2023. Mas o TCU identificou outro risco operacional: a divergência entre a informação de pagamento exibida ao trabalhador e a situação real do crédito. Esse problema pode ocorrer mesmo quando não existe pane no sistema de liquidação financeira. Exemplos:

- O sistema informa pagamento, mas o crédito não aparece.
- A CAIXA registra pagamento, mas o MTE ainda não atualizou a situação.
- A carteira digital apresenta status desatualizado.
- A informação de parcela liberada não corresponde à disponibilidade efetiva.

**Correção necessária:** criar um fail point independente para inconsistência de status de pagamento e conciliação de informações entre sistemas. [fonte: Tribunal de Contas da União]

### F18 — A estimativa de 30 dias para análise de recurso não foi adequadamente fundamentada (Média)

**Trecho auditado:** "Análise do recurso pela Secretaria de Trabalho, 'em regra' cerca de 30 dias."

**Problema:** O relatório não apresenta uma fonte primária que sustente esse prazo como tempo efetivo de análise. É necessário distinguir:

- Prazo legal para decisão administrativa.
- Meta administrativa.
- Prazo informado ao usuário.
- Tempo médio observado.
- Tempo mediano observado.
- Tempo de recursos pendentes.

A Lei 9.784/1999, art. 49, estabelece prazo de até 30 dias para decisão administrativa após concluída a instrução, prorrogável por igual período mediante motivação expressa. Esse prazo não equivale automaticamente a 30 dias contados do protocolo do recurso. O relatório deveria explicar essa diferença e verificar a duração real da tramitação. O próprio TCU 1621/2026 recomenda controle e acompanhamento dos prazos de análise dos recursos. [fonte: Tribunal de Contas da União]

### F19 — A pesquisa não separa corretamente os canais de recurso e de atendimento (Média)

**Trecho auditado:** "Procura CTPS Digital, gov.br, 158 ou agência."

**Problema:** Esses canais desempenham funções diferentes:

- CTPS Digital e gov.br permitem executar serviços digitais, inclusive requerimentos e recursos.
- O 158 oferece informações e orientação sobre serviços do MTE.
- As unidades do SINE e as Superintendências Regionais do Trabalho possuem funções presenciais próprias.
- A CAIXA atua na execução bancária e na consulta de informações de pagamento.

A pesquisa trata os canais como alternativas equivalentes, sem estabelecer o que cada um pode efetivamente fazer. A FAQ da CAIXA também direciona o requerimento para o gov.br, CTPS Digital e atendimento presencial nas unidades indicadas. [fonte: Caixa]

**O que faltou:** uma matriz de competências por canal, incluindo serviços disponíveis, limitações, transferências e responsabilidade pela conclusão da demanda.

### F20 — O relatório não examina suficientemente os procedimentos de atendimento humano (Média)

**Trecho auditado:** "Atendente consulta a situação de pagamento; não decide a concessão."

**Problema:** A afirmação é razoável como delimitação geral de competência, mas não está demonstrada para todas as funcionalidades do atendimento humano. É necessário saber:

- Quais sistemas o atendente consegue acessar.
- Se consegue visualizar o histórico do pagamento.
- Se consegue identificar a causa de uma rejeição.
- Se consegue abrir uma ocorrência interna.
- Se consegue encaminhar uma solicitação para área responsável.
- Se consegue registrar contestação de pagamento.
- Se consegue iniciar uma investigação de divergência.
- Se consegue informar o andamento de uma reemissão.

O TCU identificou falta de base de conhecimento integrada e treinamento periódico dos atendentes dos canais relacionados ao seguro-desemprego. [fonte: Tribunal de Contas da União]

**Correção necessária:** não presumir que o atendente apenas consulta informações. É preciso testar as permissões e operações disponíveis.

### F21 — A pesquisa não identifica as barreiras de acessibilidade do atendimento telefônico (Média)

**Trecho auditado:** "Intérprete de Libras por videochamada para pessoas surdas."

**Problema:** O relatório identifica corretamente uma possibilidade de atendimento em Libras, mas não avalia a acessibilidade da URA em si. Deveria investigar:

- Compatibilidade com pessoas com deficiência auditiva.
- Alternativas ao menu exclusivamente sonoro.
- Compatibilidade com leitores de tela nos canais digitais associados.
- Facilidade de acesso ao atendimento humano.
- Acessibilidade das mensagens gravadas.
- Disponibilidade de informações em linguagem simples.
- Possibilidade de concluir a jornada sem depender de terceiros.

O Acórdão 1621/2026 também recomenda avaliações periódicas de acessibilidade digital. [fonte: Tribunal de Contas da União]

**Por que é uma falha:** oferecer Libras em um canal específico não comprova acessibilidade da jornada integrada.

### F22 — A pesquisa não distingue reclamação de consumidor de manifestação de usuário de serviço público (Média)

**Trecho auditado:** "SAC e Ouvidoria Caixa; consumidor.gov.br; Fala.BR."

**Problema:** Esses instrumentos não possuem necessariamente a mesma natureza jurídica nem o mesmo campo de aplicação. O relatório deveria distinguir:

- SAC da CAIXA.
- Ouvidoria da instituição financeira.
- Consumidor.gov.br, destinado a relações de consumo.
- Fala.BR, plataforma de manifestações de ouvidoria e acesso à informação na Administração Pública.
- Ouvidoria do MTE.

Também deveria verificar a quem pertence a responsabilidade de responder a cada tipo de demanda. O prazo da Lei 13.460/2017 para manifestações de ouvidoria não deve ser automaticamente confundido com o prazo de resposta do SAC ou com o prazo de solução do problema bancário.

**Correção necessária:** elaborar uma matriz de escalonamento por natureza da manifestação e instituição responsável.

## 3. Evidências físicas e documentais importantes que ficaram de fora

Esta é uma das maiores deficiências metodológicas do relatório. Ele apresenta uma jornada de serviço, mas não apresenta um plano consistente de coleta de evidências que permita confirmar o funcionamento real do serviço. Em uma auditoria operacional da URA, eu consideraria indispensáveis os seguintes elementos.

### 3.1. Evidências da camada telefônica (omissão de alta relevância)

| Evidência | O que permite comprovar |
|---|---|
| Gravação integral da URA | Menu, mensagens, opções e comportamento efetivo |
| Gravações de chamadas humanas | Orientações, procedimentos e encaminhamentos |
| Logs de chamadas | Horário, duração, abandono e transferência |
| Relatórios de tráfego telefônico | Volume de chamadas e picos de demanda |
| Relatórios de indisponibilidade | Quedas e interrupções do serviço |
| Relatórios de tempo de espera | Desempenho da fila |
| Registros de transferência | Quantidade e destino das transferências |
| Scripts de atendimento | Orientações formalmente autorizadas |
| Base de conhecimento dos atendentes | Informações disponíveis para resolução |
| Protocolos de atendimento | Rastreabilidade das demandas |

### 3.2. Evidências da camada tecnológica

| Evidência | O que permite comprovar |
|---|---|
| Diagrama de arquitetura da URA | Sistemas e componentes envolvidos |
| Documentação das integrações | Quais bases são consultadas |
| Especificação das APIs | Dados enviados e recebidos |
| Logs de consulta | Se a consulta realmente aconteceu |
| Logs de autenticação | Falhas de identificação |
| Logs de erro | Falhas de comunicação entre sistemas |
| Monitoramento de disponibilidade | Indisponibilidade dos componentes |
| Histórico de alterações da URA | Mudanças nos menus e funcionalidades |
| Registros de incidentes | Causas e soluções das falhas |
| Plano de contingência | Procedimentos durante indisponibilidades |

### 3.3. Evidências da camada financeira

| Evidência | O que permite comprovar |
|---|---|
| Lotes semanais de DSD | Geração e envio dos documentos |
| Comprovantes de transmissão | Recebimento dos lotes pela CAIXA |
| Relatórios de rejeição | Registros não processados |
| Retornos de pagamento | Resultado da execução financeira |
| Extratos das contas suprimento | Movimentação dos recursos |
| Relatórios de conciliação | Correspondência entre MTE e CAIXA |
| Relatórios de restituição ao FAT | Tratamento de parcelas não pagas |
| Registros de reemissão | Recuperação de parcelas devolvidas |
| Comprovantes de crédito | Confirmação da disponibilização financeira |

### 3.4. Evidências da camada de governança

- Contrato MTE–CAIXA e respectivos aditivos.
- Contrato MTE–Dataprev e respectivos aditivos.
- Termos de referência dos serviços tecnológicos.
- Relatórios de fiscalização dos contratos.
- Indicadores de desempenho.
- Relatórios de auditoria interna.
- Relatórios de ouvidoria.
- Planos de ação para correção de falhas.
- Atas de reuniões de governança.
- Relatórios de cumprimento das recomendações do TCU.

**Observação importante:** não estou afirmando que todos esses documentos sejam necessariamente públicos. São evidências que deveriam ser solicitadas em uma auditoria formal. A pesquisa deveria distinguir documentos públicos disponíveis, documentos internos necessários e documentos cuja existência ainda não foi comprovada.

## 4. Outros fail points que deveriam ser investigados

Além dos problemas já apresentados no relatório, identifico os seguintes riscos operacionais que não receberam tratamento adequado. Não os classifico como falhas comprovadamente ocorridas. São hipóteses de falha que uma auditoria rigorosa deveria testar.

| Código | Fail point | Etapa | Gravidade |
|---|---|---|---|
| FP11 | URA indisponível ou sem acesso à base de pagamento | E3/E4 | Alta |
| FP12 | Falha de identificação por CPF/NIS | E4 | Média |
| FP13 | Consulta retorna informação desatualizada | E4 | Alta |
| FP14 | Sistema de pagamento e aplicativo apresentam status divergentes | E2/E4 | Alta |
| FP15 | Atendimento humano não consegue acessar histórico completo | E6 | Alta |
| FP16 | Atendente não consegue abrir ocorrência rastreável | E6 | Média |
| FP17 | Transferência sem preservação do histórico da demanda | E6/E7 | Alta |
| FP18 | Encaminhamento para canal que não possui competência para resolver | E7 | Alta |
| FP19 | Falta de retorno ao cidadão após regularização de dados | E8 | Alta |
| FP20 | Recurso protocolado sem documentação suficiente e sem possibilidade adequada de complementação | E8 | Alta |
| FP21 | Pagamento registrado como realizado sem confirmação do recebimento pelo trabalhador | E4/E9 | Alta |
| FP22 | Reemissão sem controle adequado de duplicidade | E8 | Alta |
| FP23 | Ausência de monitoramento de taxa de abandono telefônico | E5 | Média |
| FP24 | Falta de rastreabilidade entre protocolo da CAIXA e demanda encaminhada ao MTE | E6/E7 | Alta |
| FP25 | Falta de comunicação proativa sobre alteração de status da parcela | E2/E9 | Média |

Esses riscos não devem ser apresentados como ocorrências confirmadas. Para isso, seria necessário testar amostras de chamadas, registros de sistemas e casos reais de usuários.

## 5. Problemas de qualidade das fontes e inferências

Há ainda problemas na forma como as fontes foram utilizadas.

| Código | Trecho ou fonte | Problema | Gravidade |
|---|---|---|---|
| F23 | Jornal Contábil, 2018 | Fonte antiga para descrever a URA atual | Alta |
| F24 | O Povo e Seu Dinheiro, 2023 | Reportagens sobre incidente específico não demonstram frequência ou recorrência | Média |
| F25 | Licitação CECOT 121/2026 | A existência da licitação não comprova sua vinculação ao 0800 | Média |
| F26 | Página geral de atendimento da CAIXA | Não demonstra funcionalidades específicas da URA | Média |
| F27 | LegisWeb para a Resolução 957 | Fonte secundária desnecessária quando existe texto oficial do MTE | Média |
| F28 | TCU 1621/2026 | Escopo digital foi generalizado para o atendimento telefônico | Alta |
| F29 | TCU 135/2024 | Estatística de recursos apresentada sem contextualização metodológica suficiente | Média |
| F30 | Decreto 13.135/2026 | Aplicabilidade jurídica presumida sem análise da relação de consumo | Alta |
| F31 | FAQ gov.br e Resolução 957 | A divergência foi identificada, mas não investigada até sua origem | Média |

**F23 — Fonte de 2018 não serve para comprovar a URA de 2026.** A matéria do Jornal Contábil pode servir como evidência histórica. Não deve sustentar a descrição atual do menu, identificação e funcionalidades telefônicas. Seria necessário obter documentação da CAIXA ou realizar testes documentados.

**F24 — O incidente de maio de 2023 não demonstra uma falha recorrente.** O episódio das 45.335 parcelas atrasadas é relevante, mas não demonstra: frequência de falhas semelhantes; taxa anual de indisponibilidade; tempo médio de recuperação; quantidade de trabalhadores afetados em outros episódios; existência de controles corretivos. O relatório transforma um evento histórico em uma categoria de risco sem desenvolver indicadores de recorrência.

**F25 — A licitação não identifica o fornecedor da URA.** A pesquisa corretamente reconhece essa limitação, mas poderia aprofundar a investigação. Seria necessário procurar o contrato específico de operação, os lotes da contratação, o escopo de atendimento, as unidades atendidas e os eventuais contratos anteriores. Não é válido concluir que a CECOT 121/2026 opera o 0800 apenas porque envolve atendimento multimeios.

**F28 — O escopo do TCU foi extrapolado.** O Acórdão 1621/2026 examina o serviço digital do trabalhador formal. Seus achados são relevantes para compreender o ecossistema do atendimento, mas não comprovam automaticamente que a URA apresenta as mesmas falhas. É necessário manter duas categorias: falhas comprovadas no serviço digital; falhas comprovadas no canal telefônico. A interseção entre elas precisa ser demonstrada.

**F30 — A análise jurídica do SAC não foi concluída.** A publicação e a vigência do Decreto 13.135/2026 estão confirmadas. Mas há outra questão: a aplicabilidade à operação da CAIXA. A auditoria deveria examinar a legislação consumerista, a natureza da prestação bancária e as normas específicas aplicáveis. Não basta identificar que o atendimento é telefônico e pertence a uma instituição financeira.

**F31 — A divergência entre fontes oficiais não foi investigada.**

Trecho auditado: "A FAQ do gov.br fala em revisão em 'dois anos' e no app SINE-Fácil, enquanto a Res. 957 fixa 120 dias para o recurso."

O relatório identificou corretamente a necessidade de conciliar as informações, mas deveria ter aprofundado:

- Qual é a versão vigente da página.
- Se o prazo de dois anos se refere à reemissão, e não ao recurso.
- Se a página mistura procedimentos diferentes.
- Se o SINE-Fácil continua sendo indicado oficialmente.
- Se houve atualização parcial do conteúdo.
- Se a divergência pode induzir o trabalhador a perder prazo.

O serviço oficial de recurso informa expressamente 120 dias contados da notificação. [fonte: Serviços e Informações do Brasil]

## 6. Normativos e documentos que deveriam integrar a pesquisa

A pesquisa já apresenta uma boa seleção normativa, mas precisa ampliar e corrigir o enquadramento documental.

| Documento | Relevância para a auditoria |
|---|---|
| Lei 7.998/1990 | Regras legais do programa e competências institucionais |
| Resolução CODEFAT 957/2022 | Concessão, processamento, pagamento e reemissão |
| Portaria Interministerial 70/2002 | CAIXA como agente operador |
| Lei 9.784/1999 | Processo administrativo, instrução e decisão |
| Lei 13.460/2017 | Direitos dos usuários dos serviços públicos |
| Lei 14.129/2021 | Governo digital e integração de serviços |
| Decreto 8.373/2014 | eSocial e integração das informações trabalhistas |
| LGPD — Lei 13.709/2018 | Tratamento de dados pessoais e segurança |
| Lei 13.146/2015 | Acessibilidade e direitos das pessoas com deficiência |
| Decreto 13.135/2026 | SAC, condicionado à aplicabilidade jurídica |
| Acórdão TCU 135/2024 | Pagamentos irregulares e governança dos recursos |
| Acórdão TCU 1621/2026 | Qualidade do serviço digital e canais de atendimento |

Duas observações adicionais:

- A Lei 9.784/1999 deveria ter sido tratada com mais destaque, especialmente na análise de recursos e decisões administrativas.
- O Decreto 8.373/2014 é relevante porque o TCU fundamentou nele parte da determinação de integração ao eSocial.

Fontes primárias especialmente importantes: Resolução CODEFAT 957/2022 (texto oficial do MTE); Decreto 13.135/2026 (publicação original); Acórdão 1621/2026 (TCU); Acórdão 135/2024 (TCU); FAQ oficial da CAIXA — Seguro-Desemprego; serviço oficial de recurso do seguro-desemprego; Portaria Interministerial 70/2002 (CAIXA como agente operador).

## 7. O que eu mudaria na arquitetura da auditoria

A pesquisa original organiza a jornada em nove etapas. Eu manteria essa abordagem, mas acrescentaria uma visão de arquitetura operacional.

**Arquitetura que precisa ser auditada:**

1. **Trabalhador:** solicitação, acompanhamento, identificação do problema e contato.
2. **Canais de atendimento:** URA 0800 · Atendente humano · Apps · Portal Cidadão.
3. **3A. MTE:** gestão do benefício, habilitação, decisões e recursos. **3B. CAIXA:** operação bancária, pagamento e consulta financeira.
4. **Integração tecnológica:** Dataprev · eSocial · CNIS · Sistemas do seguro-desemprego · Interfaces bancárias.
5. **Controle financeiro e governança:** FAT · Lotes · Conciliação · Auditoria · Contratos · Indicadores.

O objetivo seria verificar não somente se cada componente funciona, mas se a informação percorre todo o fluxo sem perda, atraso, divergência ou ausência de rastreabilidade.

## 8. Veredito final

Minha avaliação é que a pesquisa é um bom levantamento exploratório, mas ainda não é uma auditoria operacional suficientemente comprovada.

| Avaliação qualitativa | |
|---|---|
| Precisão normativa | Boa, com ressalvas |
| Qualidade das fontes | Razoável |
| Comprovação da URA atual | Insuficiente |
| Mapeamento de backstage | Incompleto |
| Identificação de fail points | Parcial |
| Evidências físicas | Insuficiente |

*Notas qualitativas ilustrativas da auditoria, não indicadores estatísticos ou notas oficiais.*

**Síntese das falhas:**

- 7 falhas de alta gravidade identificadas entre os problemas principais.
- Diversas omissões de média gravidade.
- 31 apontamentos numerados no conjunto das seções F1–F31, incluindo problemas de fundamentação, completude e qualidade das fontes.
- 15 novos riscos operacionais propostos para investigação na matriz complementar de fail points.

A principal conclusão é que o relatório descreve razoavelmente o ecossistema do seguro-desemprego, mas não demonstra suficientemente a operação da URA.

O que falta para transformar o levantamento em auditoria de verdade: evidência direta do canal telefônico, documentação das integrações, contrato de operação, logs, testes de jornada e conciliação entre os registros de pagamento e as informações disponibilizadas ao trabalhador.

Minha recomendação é não utilizar a pesquisa original como diagnóstico definitivo da operação do 0800 726 0207 sem uma segunda rodada de verificação documental e testes operacionais.
