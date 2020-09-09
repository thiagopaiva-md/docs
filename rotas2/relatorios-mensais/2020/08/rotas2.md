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
