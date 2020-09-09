# Dashboard Rotas - Relatório de teste

Neste relatório será definido o projeto de testes da funcionalidade de dashboard de rotas no Sistema MDM, visando validar seu funcionamento. Os requisitos da ferramenta foram avaliados para determinar se foram plenamente cumpridos.\
Um caso de teste especifica uma maneira de testar o sistema: o que testar, quais os valores e pré-condições de entrada e os valores e pós-condições de saída.

## 1 - Teste unitário

### 1.1 - Objetivo

O teste unitário é um programa de teste que verifica correta execução dos métodos do sistema. Para este projeto foi utilizado o framework de testes Jest.

### 1.2 - Método utilizado

Foi realizada uma abordagem qualitativa, priorizando o maior número de situações possível. Foram realizados 14 testes unitários, dentre os quais 12 tiveram sucesso e 2 apresentaram erros, sendo prontamente solucionados.

### 1.3 - Resultados obtidos

O erro mais comum foi o erro do tipo "cannot read property of undefined", que acontece quando era necessário atribuir valores a determinadas variáveis, porém estas não estavam inicializadas. Com os testes unitários, foi possível encontrar e corrigir estas exceções.

## 2 - Teste de comunicação

### 2.1 - Objetivo

Assegurar a correta comunicação entre o coletor e o Sistema MDM.

### 2.2 - 

## 3 - Testes de interface

### 3.1 - Objetivo

O teste de interface tem como objetivo garantir o melhor fluxo de interação do usuário com o sistema. O teste visa garantir um sistema interativo que seja operado de maneira eficiente, sem deixar de ser agradável para o usuário final.\
O principal critério de avaliação é a eficácia da interação humano-computador. A partir da eficiência desta interação, avaliamos os recursos empregados (tempo, passos desnecessário, busca de ajuda, etc) e, a partir destes dados, obter índices de satisfação ou insatisfação que possa trazer ao usuário.

### 3.2 - Método utilizado

Os testes foram implementados utilizando modelos de protótipos em papel e no computador. As técnicas de verificação se basearam nos conhecimentos ergonômicos e na experiência dos avaliadores que interagindo com a interface identificaram alguns problemas de interação humano-computador.

### 3.3 - Resultados obtidos

Após utilização do software por nossa equipe de testes, observamos que a interação com a interface foi completamente integrada. O feedback dos testadores foram avaliados e, baseados em decisões conjuntas, a interface foi ajustada para a melhor experiência possível em nossa avaliação.
