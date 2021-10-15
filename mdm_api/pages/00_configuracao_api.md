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
      instanceName?: string;
    },
  ];
  balancing: number;
  anaq: {
    rabbitMQ: {
      host: string;
      username: string;
      password: string;
      vhost: string;
      timeout: number;
    };
  };
```

## Descrição da assinatura do arquivo config.json

### Seção "rabbitMQ" - **Opcional: Sim**
Caso a seção "rabbitMQ" esteja declarada no arquivo, os parâmetros abaixo deverão ser configurados.\
Caso a seção "rabbitMQ" não esteja declarada no arquivo, os valores default abaixo serão aplicados.

Nome                     |  Tipo           | Opcional     | Descrição | Default
:-----------------------:|:---------------:|:------------:|:------------|:------------
host                     | string         | Não           | O host rabbitMQ ao qual a API se conecta para receber requisições. | localhost
username                 | string         | Não           | Username do rabbitMQ ao qual a API se conecta para receber requisições. | anaq
password                 | string         | Não           | Password do rabbitMQ ao qual a API se conecta para receber requisições. | anaq
vhost                    | string         | Sim           | vHost rabbitMQ ao qual a API se conecta para receber requisições. | 
rpcQueueName             | string         | Não           | Nome da fila de RPC do serviço MDM API | q_mdm.api.rpc
helperQueueName          | string         | Não           | Nome da fila para requisições ao Helper (serviço de processamento de sinais) | q_mdm.api.helper
publishQueueName         | string         | Não           | Nome da fila para publicações do serviço MDM API | q_mdm.api.publish.<DATABASE_ALIAS><br/>**Exemplo:**<br/>q_mdm.api.publish.ILS
timeout                  | integer        | Não           | Valor de timeout em ms para falha em consultas RPC | 40000ms (40s)
