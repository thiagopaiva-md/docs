# Relatório Mensal - julho de 2020

## 1 - Streaming de dados em tempo real

Avançando nas novas funcionalidades do coletor, existe a previsão de o dispositivo estar online durante determinados momentos da coleta de dados. Neste caso, 
ao posicionar-se em um local onde exista conectividade , o software será capaz de transmitir dados ao servidor.\
Entre os principais dados, podemos destacar: rotas em execução, ponto atual da execução e informações de temporização. De posse destes dados,
será possível visualizá-los no servidor, em tempo real.

<p align="center">
  <img src="images/disconnected.jpg" />
</p>
<p align="center">
Aplicação sem conexão: Os dados são armazenados apenas na memória interna do aparelho.
 </p>
 
<p align="center">
  <img src="images/connected.jpg" />
</p>

<p align="center">
  Aplicação conectada: Dados continuam sendo armazenados na memória, porém também são enviados ao servidor.
</p>
