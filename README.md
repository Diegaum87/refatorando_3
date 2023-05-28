# Tarefa 3 | Refatorando

Introdução
Essa é uma parte do projeto semanal. Não será necessário entregar parte a parte, mas sim o projeto inteiro ao fim da semana. Leia atentamente aos requerimentos e desenvolva o que é pedido.

Leia o enunciado até o final antes de começar, assim terá uma visão macro sobre tudo que deve ser feito!

Quando concluir a tarefa, adicione as alterações e faça um commit, seguindo o seguinte padrão:

feat: tarefa x finalizada

Refatorando
Nessa tarefa, começaremos refatorando algumas funções já desenvolvidas.

Refatorando get_product_by_id
Refatore sua função get_product_by_id para que, caso o parâmetro passado não seja do tipo inteiro, uma exceção TypeError seja levantada com a seguinte mensagem: "product id must be an int".

Refatorando get_product_by_type
Refatore sua função get_products_by_type para que, caso o parâmetro passado não seja do tipo string, uma exceção TypeError seja levantada com a seguinte mensagem: "product type must be a str".

Adicionando report
Você deverá adicionar uma função ao módulo product_handler para retornar um report sobre alguns dados do menu:

menu_report
Parâmetro(s):
Essa função não recebe parâmetros.
Procedimento(s):
Você deverá montar um report sobre algumas características do menu de produtos:
Product Count: Contagem do total de produtos do menu.
Average Price: Média dos preços de todos os produtos do menu, arredondada para 2 casas decimais no máximo.
Most Common Type: O tipo de produto mais comum, ou seja, o tipo que contém maior quantidade de produtos no menu.
O retorno deve ser uma string formatada exatamente como no exemplo abaixo, com o devido dinamismo de cada característica:
"Products Count: <contagem_de_produtos> - Average Price: $<preco_medio> - Most Common Type: <tipo_mais_comum>"

EXTRA
Não será cobrado esse desafio extra na entrega final.

add_product_extra
Como desafio extra, você criará uma função no módulo product_handler, chamada add_product_extra. Essa função terá algumas regras a mais que a função padrão desenvolvida anteriormente. Você não deverá alterar a função add_product desenvolvida anteriormente.

Parâmetro(s):
[Comportamento Mantido] - Variável menu, uma lista representando o menu em questão para o produto ser adicionado.
[Comportamento Mantido] - Quantidade indefinida de argumentos nomeados, representando o produto a ser adicionado.
[Comportamento Novo] - Quantidade indefinida de argumentos, representando as chaves obrigatórias.
Procedimento(s):
[Comportamento Novo]
- Você deverá fazer duas verificações nas chaves do produto a ser adicionado antes de prosseguir:
Verificar se todas as chaves obrigatórias estão contidas no produto a ser adicionado. Caso alguma não esteja, deve ser levantada uma exceção KeyError, com a mensagem: "field <chave> is required". Caso contrário, continuar o fluxo do código.
Verificar se existem chaves a mais do que as obrigatórias nas chaves do produto a ser adicionado. Caso existam, eliminá-las do produto, o deixando apenas com as chaves obrigatórias.
[Comportamento Mantido] - Você deverá gerar um novo id único para o produto adicionado. O novo id único deve ser armazenado na chave "_id" do novo produto, e deve ser referente ao maior id de produto do menu, somado com 1. Caso não haja produtos no menu, o id gerado deve ser 1.
[Comportamento Mantido] - Após o id ser gerado e anexado ao produto, você deve adicioná-lo ao menu e retornar apenas o produto adicionado com o id gerado.
