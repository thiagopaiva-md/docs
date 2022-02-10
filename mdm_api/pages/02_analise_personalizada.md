## Executar análise personalizada

**Objetivo:** Executar, dentro da interface do EAMon, uma análise personalizada cadastrada no Sistema MDM.

Esta requisição será realizada em 2 etapas.

**Etapa 1:** Obter a lista de análises cadastradas no MDM.

**Nome da operação Etapa 1:** core_getCustomAnalysis

**Parâmetros de entrada - etapa 1:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string

**JSON de exemplo - parâmetros de entrada:**
```
{
  "databaseAlias": "ILS",
  "operation": "core_getCustomAnalysis",
}
```

## Saída - Etapa 1

**Descrição dos parâmetros de saída em caso de sucesso, presentes no array de objetos "content":**

**Atenção:** A tabela abaixo descreve cada um dos objetos presentes no array.

Nome                           |  Tipo           | Descrição
:-----------------------------:|:---------------:|:-------------
id                             | string              | Id da análise personalizada
nome                           | string              | Nome da análise personalizada
qtdeTempo                      | integer             | Quantidade de tempo para a busca de registros
periodo                        | integer             | Período da busca de registros (dias, meses ou anos)
ferramenta                     | string              | Nome da ferramenta de análise
tipoDeDado                     | integer             | Tipo de dado da análise (2850 - referência, 2851 - registro)
descricao                      | string              | Descrição da análise personalizada
idsInstrumentosSelecionados    | string              | Ids dos pontos monitorados ou equipamentos, separados por ponto e vírgula (;)
tipoInstrumento                | integer             | Tipo de instrumento (ponto monitorado ou equipamento)

**Etapa 2:** Executar a análise solicitada.

**Nome da operação Etapa 2:** core_getCustomAnalysisData

**Parâmetros de entrada - etapa 2:**

Nome       |  Tipo
:---------:|:---------------:
databaseAlias    | string
operation        | string
analysisId       | string

**JSON de exemplo - parâmetros de entrada:**
```
{
  "databaseAlias": "ILS",
  "operation": "core_getCustomAnalysisData",
  "analysisId": "{F5F739B0-E409-4298-A69A-DB178820C273}"
}
```

**Exemplo no MDM:**\
[Seleção Análise personalizada](../images/ExecutarAnalisePersonalizada.jpg)

### [Saída - Etapa 2 - Análise sequencial](./02a_analise_personalizada_saida_sequencial.md)


[Análise comparativa](../images/AnaliseComparativa.jpg)
