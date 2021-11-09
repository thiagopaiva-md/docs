## Executar análise personalizada

**Objetivo:** Executar, dentro da interface do EAMon, uma análise personalizada cadastrada no Sistema MDM.

Esta requisição será realizada em 2 etapas.

**Etapa 1:** Obter a lista de análises cadastradas no MDM.

**Nome da operação Etapa 1:** core_getCustomAnalysis

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Exemplo no MDM:**\
[Seleção Análise personalizada](../images/ExecutarAnalisePersonalizada.jpg)

**Etapa 2:** Executar a análise solicitada.

**Nome da operação Etapa 2:** core_getCustomAnalysisData

**Parâmetros de entrada:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
analysisId       | string

**Parâmetros de saída:**

Nome       |  Tipo
:---------:|:---------------:
status     | number 
content    | string ou object[]

**Exemplo no MDM:**\
[Análise sequencial](../images/AnaliseSequencial.jpg)\
[Análise comparativa](../images/AnaliseComparativa.jpg)
