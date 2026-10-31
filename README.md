# API de Gerenciamento de Pedidos

## Objetivo

Desenvolver uma API REST para gerenciar pedidos de uma pequena loja, utilizando Node.js, Express e JavaScript.

## Tecnologias utilizadas

- Node.js
- Express
- JavaScript
- Jest
- Postman
- Git e GitHub

## Como instalar e executar

1. Instale o Node.js.
2. Abra o terminal na pasta do projeto.
3. Instale as dependências:

   `npm install`

4. Inicie a API:

   `npm start`

A API ficará disponível em `http://localhost:3000`.

## Como executar os testes

Para executar os testes automatizados, utilize:

`npm test`

## Funcionalidades

- Cadastrar pedidos.
- Listar todos os pedidos.
- Consultar um pedido pelo ID.
- Atualizar o status de um pedido.
- Validar os dados informados no cadastro.
- Rejeitar pedidos com dados inválidos.
- Informar quando um pedido não for encontrado.

## Testes realizados

Os testes automatizados verificam o cadastro de pedidos válidos, a rejeição de clientes vazios, a rejeição de valores menores ou iguais a zero e a consulta de identificadores inexistentes.

Os testes foram executados com sucesso utilizando Jest.

## Estrutura do projeto

- `src/app.js`: configura e inicia o servidor.
- `src/routes/pedidoRoutes.js`: define as rotas da API.
- `src/controllers/pedidoController.js`: controla as requisições e respostas.
- `src/services/pedidoService.js`: contém as regras de negócio.
- `tests/pedidoService.test.js`: contém os testes automatizados.
- `evidencias/`: pasta destinada às capturas de tela dos testes.

## Endereço da API

`http://localhost:3000/pedidos`

## Identificação Acadêmica

**Aluno:** Gustavo Valentim dos Santos  
**RGM:** 42190703  
**Instituição:** Universidade Cruzeiro do Sul  
**Disciplina:** Tópicos Avançados em Sistemas de Informação II  
**Projeto:** API de Gerenciamento de Pedidos  
**GitHub:** GustavoValentim03

## Uso de Inteligência Artificial

Utilizei o ChatGPT como ferramenta de apoio para compreender os requisitos do projeto, configurar o ambiente de execução e realizar os testes manuais utilizando o Postman.

Durante a execução, identifiquei e corrigi um problema no endereço de uma requisição que retornava HTTP 404.

Também investiguei uma tentativa de atualização de status que retornava HTTP 400, devido a uma transição não permitida. Após testar a alteração para o status `cancelado`, a API retornou HTTP 200, confirmando o funcionamento da atualização.

A sugestão de testar o status `cancelado` foi aceita após a rejeição da transição anterior. Os testes foram executados por mim, e as cinco evidências foram registradas e publicadas no meu repositório GitHub.

## Evidências dos testes

As cinco evidências estão disponíveis na pasta `evidencias/` do repositório e demonstram as operações de cadastro, validação, listagem, consulta de pedido inexistente e atualização de status.
