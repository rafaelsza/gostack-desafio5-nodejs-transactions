# Back-end com NodeJS e TypeScript

Desafio n°5 do bootcamp GoStack, onde desenvolvemos um back-end utilizando os conhecimentos adquiridos durante as aulas do primeiro módulo do segundo nível.

Sua funcionalidade é cadastrar transações em um array, salvando dados como:
- title: Título da transação.
- value: Valor da transação.
- type: Tipo da transação onde pode ter apenas os valores:
  - 'income' para transações de entrada.
  - 'outcome' para transações de sáida.

No método GET da rota /transaction além de retornar todas as transações retorna também o balanço de todas as transações.

Utilizado:
- express: para definir rotas e suas funcionalidades.
- uuidv4: para gerar ID's aleatórios e únicos.
- ts-node-dev: para criar um servidor local e converter códigos TypeScript em JavaScript.

Padronização de código utilizando:
- ESLint
- Prettier

<h2>Para utilizar em sua máquina:</h2>

<b>* Necessário ter o <a href="https://yarnpkg.com/getting-started/install">yarn</a> e o <a href="https://nodejs.org/en/download/">NodeJS</a> instalados em sua máquina.</b>

Para utilizar a rota do projeto será preciso utilizar o <a href="https://insomnia.rest/download/">Insomnia</a> ou o <a href="https://www.postman.com/downloads/">Postman</a>, conforme sua preferência.

Clone o projeto:
```
git clone https://github.com/rafaelsza/gostack-desafio5-nodejs-transactions.git
```

Entre na pasta raíz do projeto:
```
cd gostack-desafio5-nodejs-transactions
```

Execute yarn para instalar todas as dependências do projeto.
```
yarn
```

Para executar o projeto digite:
```
yarn dev:server
```

Agora com o Back-end rodando em sua máquina já pode começar a utilizar a rota e seus métodos HTTP.

<b>ROTA</b>: <a href="http://localhost:3333/transaction">http://localhost:3333/transaction</a>

<h2>Métodos HTTP:</h2>

- <b>POST</b>: para cadastrar uma nova transação.  <br/>
  Crie uma nova requisição do tipo POST no Insomnia/Postman colocando a rota acima e passando dentro do corpo os valores em formato JSON, conforme exemplificados abaixo:
  ```
  {
    "title": "Salário",
    "value": "200",
    "type": "income"
  }
  ```
  *Lembrando que type pode ser do tipo 'income' ou 'outcome' conforme informado no início.<br/>
  *Caso uma transação do tipo 'outcome' seja maior que seu saldo em conta, retornará uma mensagem de erro e não será realizado o registro da transação.

- <b>GET</b>: retorna todas as transações juntamente com o balanço das mesmas.<br/>
Crie uma nova requisição do tipo GET no Insomnia/Postman colocando a rota acima.
