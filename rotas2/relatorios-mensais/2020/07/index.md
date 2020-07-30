# Relatório Mensal - julho de 2020

## 1 - Streaming de dados em tempo real

Avançando nas novas funcionalidades do coletor, existe a previsão de o dispositivo estar online durante determinados momentos da coleta de dados. Neste caso, 
ao posicionar-se em um local onde exista conectividade , o software será capaz de transmitir dados ao servidor.\
Entre os principais dados, podemos destacar: rotas em execução, ponto atual da execução e informações de temporização. De posse destes dados,
será possível visualizá-los no servidor, em tempo real.

### 1.1 - Arquitetura de comunicação

Enquanto a aplicação estiver sem conexão, os dados de coleta são armazenados apenas na memória interna do dispositivo.\
Quando a conexão for realizada, os dados continuam sendo armazenados na memória, porém o coletor iniciará uma publicação de dados para o servidor.

<p align="center">
  <img src="images/disconnected.jpg" />
</p>
<p align="center">
Aplicação sem conexão: Os dados são armazenados apenas na memória interna do aparelho.
 </p> 
 <br/><br/>
<p align="center">
  <img src="images/connected.jpg" />
</p>
<p align="center">
  Aplicação conectada: Dados continuam sendo armazenados na memória, porém também são enviados ao servidor.
</p>

#### 1.2 - Dados disponíveis para consulta

- Rotas em execução no momento
- Ponto atual da execução das rotas
- Percentuais de conclusão
- Informações sobre temporização

### 1.3 - Informações sobre o dashboard
