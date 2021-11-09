## Árvore de análise

**Objetivo:** Trazer para o EAMon toda a informação da árvore de análise do Sistema MDM, incluindo a estrutura de equipamentos, subsistemas, componentes e pontos monitorados.

**Nome da operação:** core_getMonitoredPointsTree

**Parâmetros de entrada:** 

Nome                     |  Tipo           | Opcional     | Descrição
:-----------------------:|:---------------:|:------------:|:------------
databaseAlias            | string         | Não           | O alias da base de dados utilizada no momento da chamada.
operation                | string         | Não           | core_getMonitoredPointsTree  

**JSON de exemplo - parâmetros de entrada:**
```
{
  "databaseAlias": "ILS",
  "operation": "core_getOilTankLevels",
}
```

## Saída

**Descrição dos parâmetros de saída em caso de sucesso, presentes no array de objetos "content":**

**Atenção:** A tabela abaixo descreve cada um dos objetos presentes no array.

**Primeiro nível no JSON:** Plantas

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string              | Id da planta
nome               | string              | Nome da planta
endereco           | string              | Endereço da planta
empresa            | string              | Nome da empresa
equipamentos       | object<Equipment>[] | Array de objetos equipamento desta planta, apresentado a seguir
  
**Segundo nível no JSON:** Equipamentos

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string              | Id da planta
idPlanta           | string              | Id da planta associada ao equipamento
idAnalisador       | string              | Id do analisador associado ao equipamento
idUnidadeAquisicao | string              | Id da unidade de aquisição associada ao equipamento
nome               | string              | Nome do equipamento
fabricante         | string              | Nome do fabricante
modelo             | string              | Modelo do equipamento
descricao          | string              | Descricao do equipamento
localizacao        | string              | Localização do equipamento
nroSerie           | string              | Número de série do equipamento
tipoEquipamento    | integer             | Numeral do tipo de equipamento
subsistemas        | object<Subsystem>[] | Array de objetos subsistema deste equipamento, apresentado a seguir
  
**Terceiro nível no JSON:** Subsistemas

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string              | Id do subsistema
idEquipamento      | string              | Id do equipamento associado ao subsistema
nome               | string              | Nome do subsistema
descricao          | string              | Descrição do subsistema
componentes        | object<Component>[] | Array de objetos componente deste subsistema, apresentado a seguir
  
**Terceiro nível no JSON:** Componentes

Nome               |  Tipo           | Descrição
:-----------------:|:---------------:|:-------------
id                 | string                   | Id do subsistema
idSubsistema       | string                   | Id do subsistema associado ao componente
nome               | string                   | Nome do componente
descricao          | string                   | Descrição do componente
pontosMonitorados  | object<MonitoredPoint>[] | Array de objetos pontos monitorados deste componente, apresentado a seguir
  
**Quarto nível no JSON:** Pontos Monitorados

Nome                     |  Tipo           | Descrição
:-----------------------:|:---------------:|:-------------
id                       | string                   | Id do ponto monitorado
idCanal                  | string                   | Id do canal associado ao ponto monitorado
idTipoSensor             | string                   | Id do Tipo Sensor associado ao ponto monitorado
idPlanoMedicao           | string                   | Id do plano de medição associado ao ponto monitorado
idComponente             | string                   | Id do componente associado ao ponto monitorado
idGrupoPontosMonitorados | string                   | Id do grupo de pontos associado ao ponto monitorado
nome                     | string                   | Nome do ponto monitorado
descricao                | string                   | Descrição do ponto monitorado
localizacao              | string                   | Localização do ponto monitorado
direcao                  | integer                  | Direção do ponto monitorado em graus (0, 90, 180, 270)
ativo                    | integer                  | Indica se o ponto está ativo (0 ou 1)
tipoSensor               | object<MonitoredPoint>[] | Array de objetos tipo sensor deste ponto monitorado, apresentado a seguir

**Exemplo no MDM:**\
[Árvore de análise](images/ArvoreAnalise.jpg)

  
