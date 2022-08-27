# ModelagemDB-Ecommerce-BootcampDIO - ⚠️ Projeto de estudos
### Desafio de Projeto do Bootcamp Database Experience da DIO

#### Contextualizando a situação do negócio para melhor entendimento da modelagem.

O desafio nos pede para modelar um projeto conceitual de um sistema de Ecommmerce.

#### Começando pela tabela cliente

* Para determinar se o cliente é CPF ou CNPJexiste um valor, entre seus valores, booleano. Na aplicação o cliente deverá escolher se é CPF (NÃO ATIVA a checkbox) ou CNPJ (ATIVA a checkbox). O dado que vamos guardar é TRUE para CPF ou FALSE para CNPJ.
* num_doc vai registrar ou o número do CPF, ou o número do CNPJ, após o usuário idenficar na aplicação qual tipo de cliente ele é.
* Deixei uma FK de cartão de crédito caso precise consultar os dados dos cartões de crédito cadastrados pelo cliente.


#### Tabela forma_pgto

* A aplicação irá determinar a forma escolhida.
* A Tabela cartao_de_credito irá salvar as informações do cartão ou cartões utilizados e o ID irá identificar cada um.
* Na tabela "forma_pgto", temos uma FK que também existe na tabela cliente. A FK de cartao_de_credito está nela para identificar qual o cartão de crédito foi utilizado pelo cliente através do seu ID.

#### Tabela entrega

* Possui um relacionamento N:M com a tabela "pedidos", assim dentro desse relacionamento temos o atributo status (da entrega).


#### As demais tabelas possuem relação com uma tabela em comum, produto.

* Era requisito para o projeto conceitual era que além dos produtos serem vendidos pela plataforma, eles também pudessem ser vendidos por terceiros nessa mesma plataforma. Para isso criamos a tabela vendedor_terceirizado que salva todas as informações desse vendedor, e durante seu relacionamento salva a quantidade de cada venda de cada produto.

### ⚠️ Este foi meu primeiro projeto conceitual de um Database, ainda preciso refiná-lo mais para deixar ele com a melhor desempenho possível.
