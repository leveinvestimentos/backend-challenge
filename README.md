# Teste Back-end Leve Investimentos

Este teste tem como objetivo conhecer um pouco mais como você programa, e como você vai se organizar para montar um pequeno sistema de compra e venda de criptomoedas.

## 1. O que você precisa fazer?

Esperamos que você desenvolva um serviço que forneça uma API REST que implemente os recursos a seguir e respeite os seguintes requisitos técnicos:

### 1.1 Linguagens

Você poderá utilizar qualquer uma das linguagens abaixo descritas:

- Node.JS (Express, Adonis, Happi)
- PHP (Laravel ou Lumen)

### 1.2. Autenticação

  Nossa aplicação demandará de autenticação utilizando JWT / Passport.

### 1.3. Cadastro de usuarios

  Crie recursos para usuários c/ 2 níveis de acesso (Administrador, Cliente).

  * Apenas Administradores podem:
  - Gerenciar Contas
  - Gerenciar Carteiras & Transações

- #### 1.3.1. Endpoints Necessários
    - Listagem geral
    - Listagem por (uuid ou id)
    - Criação
    - Edição

### 1.4 Carteiras
  Todo cliente deve possuir as seguintes carteiras após o registro:

  - BRL
  - BTC

- #### 1.4.1. Dados Indispensáveis
    - ID do Ativo (BRL, BTC)
    - ID do cliente
    - Saldo
    - Data Ultima modificação

### 1.5. Transações
    Crie recursos para depósito e saque em BRL e compra e venda de Bitcoin.

    ** O valor da cotação dos ativos devem ser capturados na api da binance
  
- ### Deposito
    A operação de deposito deve adicionar saldo a Wallet BRL do cliente para que ele possa comprar Bitcoin

- ### Saque
    Para o cliente solicitar é preciso ter saldo em sua Wallet (BRL), as maneiras de ter o saldo em sua Wallet (BRL) é por meio 
    de depósito ou na venda do seu ativo (BTC)

    * quando o saque é solicitado, é requerido que o valor seja bloqueado da sua Wallet (BRL).

    Ex: César soliciou o saque de R$ 50,00 e o mesmo possui R$ 100,00 em sua Wallet, até que a transação seja finalizada o cliente poderá operar
    apenas os R$ 50,00 restantes.

- ### Compra
    O valor utilizado para a compra de Bitcoin (BTC) deve sair de sua Wallet BRL.

- ### Venda
    Após vender o valor da operação deve ser acrescentado a sua Wallet BRL

- #### 1.5.1. Dados Indispensáveis
    - ID da carteira
    - ID do cliente
    - Preço médio
    - Quantidade (em caso de compra e venda)
    - Valor em R$
    - Status
    - Data de processamento

- #### 1.5.2. Endpoints Necessários
    - Listagem geral.
    - Listagem por id do cliente.
    - Criação.
    - Edição (cancelar caso não tenha sido finalizado ou esteja em andamento)
    - Deleção (caso o status seja = aguardando)

## 2. Observações

- Não se esqueça de criar um README explicando como faremos para rodar sua aplicação e demais informações que ache necessário.
- Poderá ser utilizado qualquer banco de dados SQL ou NoSQL.
- As transações devem ser processadas após um minuto de sua criação
- Documentação da api

## 3. Seria legal se você utilizasse

- Filas
- Docker.
- Design Patterns.
- Testes Unitários e de Integração.

## 4. Método de avaliação

Avaliaremos seu desafio de código com base em alguns atributos de qualidade do sistema. Alguns nós consideramos indispensáveis, como correção, e serão avaliados em uma abordagem binária (funciona / segue ou não). Os outros, por não serem objetivos, não poderão sozinhos desabonar seu desafio. Estes são todos os atributos de qualidade que esperamos que você aborde:

- Correção: Seu código deve seguir todos os requisitos apresentados no item 1 e seus subsequentes até 1.5.2.
- Desempenho: Quanto mais dados você puder lidar e mais rápido você consultar, melhor.
- Testabilidade: Quão bem testado seu código é e quão fácil é adicionar novos testes ao seu código.
- Capacidade de manutenção: Como é fácil adicionar recursos extras ao seu código.
- Separação de Conceitos: (https://en.wikipedia.org/wiki/Separation_of_concerns).

## 5. Como enviar?

Crie um repositório público no Github e envie um e-mail para ti@leve.app.br com o link do mesmo.

## 6. Dúvidas?

Assunto: Challenge Backend
E-mail: ti@leve.app.br

Boa sorte! :)