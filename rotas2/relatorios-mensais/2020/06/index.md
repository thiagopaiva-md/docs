# Relatório mensal - junho de 2020
## 1 - Coletor em modo online durante a coleta de dados
Uma nova funcionalidade foi desenvolvida foi desenvolvida para a nova versão do coletor, que prevê o caso de o mesmo estar online durante a rota de inspeção. Neste caso, ao posicionar-se em um local onde exista conectividade durante a coleta de dados, o software de rota será capaz de transmitir dados ao servidor. Entre os principais dados, podemos destacar: status da execução, métricas de tempo decorrido, interrupções e suas devidas justificativas, alterações na ordem da coleta, entre outros.\
Com esta nova funcionalidade, será possível visualizar no servidor, em tempo real, o status da execução das rotas.
### 1.1 - Ícone de status da conexão
Para determinar se o coletor está online e apto para a transferência de dados, foi adicionado um ícone na interface, com o símbolo de uma conexão wi-fi. A conectividade é verificada periodicamente de forma automática. Caso seja possível conectar-se, o ícone será exibido na cor verde. Caso contrário, será exibido na cor vermelha.

![](images/welcome.jpg)
