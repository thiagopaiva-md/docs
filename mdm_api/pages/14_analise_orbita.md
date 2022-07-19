# 14 - Análise de órbita

**Objetivo:** Publicar na MDM API os dados da análise de órbita

## Entrada

**Nome da operação:** core_getOrbitAnalysis

**Parâmetros de entrada:**

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não           | O alias da base de dados utilizada no momento da chamada.
operation                | string         | Não           | core_getOrbitAnalysis
type                     | string         | Não           | Valores válidos:<br/> record / reference 
monitoredPointIds        | string[]       | Não           | Os Ids dos pontos monitorados que serão incluídos na análise.
recordOrReferenceIds     | string[]       | Não           | O ids de registros ou referências que serão incluídos na análise.

**JSON de exemplo - parâmetros de entrada**

```
{
  "databaseAlias": "ILS",
  "operation": 'core_getOrbitAnalysis',
  "type": 'record',
  "monitoredPointIds": ['{86A231E5-6DC6-4217-A85F-A89E8AE398BD}'],
  "recordOrReferenceIds": ['{17071861-5B7B-3A47-BCC8-71F7D21AF145}'],
}
```
