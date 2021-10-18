# Configurações da MDM API

A configuração da MDM API é realizada através do arquivo config.json, que deve estar presente na pasta raiz do projeto.

## Assinatura do arquivo config.json

```
{
  rabbitMQ: {
    host: string;
    username: string;
    password: string;
    vhost: string;
    rpcQueueName: string;
    helperQueueName: string;
    publishQueueName: string;
    timeout: number;
  };
  databases: [
    {
      type: 'mssql' | 'oracle';
      alias: string;
      name: string;
      host: string;
      username: string;
      password: string;
      instanceName: string;
    },
  ];
  balancing: number;
  anaq: [
    {
      name: string;
      alias: string;
      rabbitMQ: {
        host: string;
        username: string;
        password: string;
        vhost: string;
        timeout: number;
        config: {
          getConfigRoutingKey: string;
          oilStockViName: string;
        }
      };
    };
  ]
```

## Descrição da assinatura do arquivo config.json

### Seção "rabbitMQ" - **Opcional: Sim**
Caso a seção "rabbitMQ" esteja declarada no arquivo, os parâmetros abaixo deverão ser configurados.\
Caso a seção "rabbitMQ" não esteja declarada no arquivo, os valores default abaixo serão aplicados.

Nome                     |  Tipo           | Opcional     | Descrição | Default
:-----------------------:|:---------------:|:------------:|:------------|:------------
host                     | string         | Sim           | O host rabbitMQ ao qual a API se conecta para receber requisições. | localhost
username                 | string         | Sim           | Username do rabbitMQ ao qual a API se conecta para receber requisições. | anaq
password                 | string         | Sim           | Password do rabbitMQ ao qual a API se conecta para receber requisições. | anaq
vhost                    | string         | Sim           | vHost rabbitMQ ao qual a API se conecta para receber requisições. | "" (String vazia - Sem vHost)
rpcQueueName             | string         | Sim           | Nome da fila de RPC do serviço MDM API | q_mdm.api.rpc
helperQueueName          | string         | Sim           | Nome da fila para requisições ao Helper (serviço de processamento de sinais) | q_mdm.api.helper
publishQueueName         | string         | Sim           | Nome da fila para publicações do serviço MDM API | q_mdm.api.publish.<DATABASE_ALIAS><br/>**Exemplo:**<br/>q_mdm.api.publish.ILS
timeout                  | integer        | Sim           | Valor de timeout em ms para falha em consultas RPC | 40000ms (40s)

### Seção "databases" - **Opcional: Não**
A seção databases é formada por um array, o qual pode-se configurar várias bases de dados. Cada parâmetro do objeto do array é descrito na tabela abaixo:

Nome                     |  Tipo           | Opcional     | Descrição | Default
:-----------------------:|:---------------:|:------------:|:------------|:------------
type                     | string         | Sim           | Valores válidos: "mssql" ou "oracle" | mssql
alias                    | string         | Não           | O "apelido", ou alias, da base de dados. Será utilizado na identificação da base a ser trabalhada na requisição. | 
name                     | string         | Não           | O nome da base de dados configurada no SGBD. |
host                     | string         | Sim           | O Host onde o SGBD está instalado. | localhost
username                 | string         | Sim           | O usuário configurado no SGBD. | dba
password                 | string         | Sim           | A senha do usuário configurado no SGBD | sql
instanceName             | string         | Sim           | Nome da instância no SGBD onde a base está configurada | Default instance

### Seção "anaq" - **Opcional: Não**
A seção anaq é formada por um array, o qual pode-se configurar vários ANAQs para consulta. Cada parâmetro do objeto do array é descrito na tabela abaixo:

Nome                     |  Tipo           | Opcional     | Descrição | Default
:-----------------------:|:---------------:|:------------:|:------------|:------------
name                     | string         | Não           | O nome do ANAQ. |
alias                    | string         | Não           | O "apelido", ou alias, do Anaq. Será utilizado na identificação do ANAQ a ser trabalhada na requisição. <br/><b>ATENÇÃO: Utilizar o mesmo alias do banco de dados!</b> | 

#### Subseção "rabbitMQ"

Nome                     |  Tipo           | Opcional     | Descrição | Default
:-----------------------:|:---------------:|:------------:|:------------|:------------
host                     | string         | Sim           | O host rabbitMQ onde se encontra o ANAQ. | localhost
username                 | string         | Sim           | Username do host rabbitMQ onde se encontra o ANAQ. | anaq
password                 | string         | Sim           | Password do host rabbitMQ onde se encontra o ANAQ. | anaq
vhost                    | string         | Sim           | vHost do rabbitMQ onde se encontra o ANAQ. | "" (String vazia - Sem vHost)
timeout                  | integer        | Sim           | Valor de timeout em ms para falha em consultas RPC | 40000ms (40s)

#### Subseção "rabbitMQ.config"

Nome                     |  Tipo           | Opcional     | Descrição | Default
:-----------------------:|:---------------:|:------------:|:------------|:------------
getConfigRoutingKey      | string         | Sim           | Routing Key para consultas à função "GetConfig". | <Nome_Anaq>.GetConfig<br>Ex: ANAQ_CHV.GetConfig
oilStockViName           | string         | Sim           | Nome da Vi utilizada para estoque de óleo.<br/><b>ATENÇÃO:</B>Apenas os pontos virtualizados vinculados ao nome dessa vi serão considerados para  a consulta do valor do estoque de óleo.| estoque.vi

### Parâmetro "balancing" - Opcional: Sim

O parâmetro "balancing" determina a segmentação das consultas de sinais em múltiplas partes, evitando assim o erro de query timeout.
Valor padrão: 3 (a consulta é dividida em 3 partes).
