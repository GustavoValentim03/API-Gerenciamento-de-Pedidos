# API de Gerenciamento de Pedidos

## 1. Objetivo

Desenvolver uma API REST para gerenciamento de pedidos de uma pequena loja, utilizando Node.js, Express e JavaScript.

O projeto permite cadastrar pedidos, consultar informações, listar pedidos existentes e atualizar seus status, aplicando validações e regras de negócio.

## 2. Tecnologias utilizadas

- Node.js
- Express
- JavaScript
- Jest
- Postman
- Git e GitHub

## 3. Como instalar e executar

1. Instale o Node.js.
2. Abra o terminal na pasta do projeto.
3. Instale as dependências:

   `npm install`

4. Inicie a aplicação:

   `npm start`

A API estará disponível em:

`http://localhost:3000`

## 4. Funcionalidades

- Cadastrar novos pedidos.
- Listar todos os pedidos cadastrados.
- Consultar pedidos pelo identificador.
- Atualizar o status de pedidos.
- Validar os dados informados.
- Rejeitar cadastros com informações inválidas.
- Informar quando um pedido não for encontrado.
- Impedir transições de status não permitidas.

## 5. Endpoints da API

| Método | Rota | Descrição |
|---|---|---|
| POST | /pedidos | Cadastrar um pedido |
| GET | /pedidos | Listar todos os pedidos |
| GET | /pedidos/:id | Consultar um pedido pelo ID |
| PATCH | /pedidos/:id/status | Atualizar o status de um pedido |

### Códigos HTTP

- **200 OK:** consulta, listagem ou atualização realizada com sucesso.
- **201 Created:** pedido cadastrado com sucesso.
- **400 Bad Request:** dados inválidos ou transição de status não permitida.
- **404 Not Found:** pedido não encontrado.

## 6. Exemplo de cadastro de pedido

**Método:** POST

**Endereço:** `http://localhost:3000/pedidos`

**Corpo da requisição (JSON):**

```json
{
  "cliente": "Gustavo Valentim",
  "tipo": "entrega",
  "valor": 350,
  "prioridade": "normal"
}
```

**Exemplo de resposta HTTP 201:**

```json
{
  "id": 1,
  "cliente": "Gustavo Valentim",
  "tipo": "entrega",
  "valor": 350,
  "prioridade": "normal",
  "status": "recebido"
}
```

## 7. Validações e regras de negócio

A API realiza verificações para garantir a integridade das informações.

Entre as validações confirmadas nos testes estão:

- O nome do cliente não pode estar vazio.
- O valor do pedido deve ser maior que zero.
- A consulta de um identificador inexistente deve retornar erro.
- As alterações de status devem respeitar as transições permitidas pelo sistema.

Os valores completos aceitos para tipo, prioridade e transições de status devem ser consultados na implementação do serviço.

## 8. Estrutura do projeto

- `src/app.js`: configuração e inicialização do servidor.
- `src/routes/pedidoRoutes.js`: definição das rotas.
- `src/controllers/pedidoController.js`: tratamento das requisições e respostas.
- `src/services/pedidoService.js`: implementação das regras de negócio.
- `tests/pedidoService.test.js`: testes automatizados.
- `evidencias/`: capturas de tela dos testes manuais.

## 9. Testes automatizados com Jest

Os testes foram executados no terminal utilizando:

`npm test`

### Cenários testados

1. Cadastro de pedido válido.
2. Rejeição de cadastro com cliente vazio.
3. Rejeição de pedido com valor menor ou igual a zero.
4. Rejeição de identificador inexistente.

### Resultado da execução

| Indicador | Resultado |
|---|---|
| Suítes executadas | 1 |
| Suítes aprovadas | 1 |
| Testes executados | 4 |
| Testes aprovados | 4 |
| Testes reprovados | 0 |

**Resultado: todos os quatro testes automatizados foram aprovados.**

## 10. Testes manuais com Postman

Foram realizados testes manuais utilizando o Postman para verificar as respostas da API.

As cinco evidências estão disponíveis na pasta `evidencias/`.

| Arquivo | Teste |
|---|---|
| 01-criacao.png | Cadastro de pedido |
| 02-validacao.png | Validação de dados obrigatórios |
| 03-listagem.png | Listagem de pedidos |
| 04-consulta-inexistente.png | Consulta de pedido inexistente |
| 05-atualizacao.png | Atualização de status |

Os testes demonstraram respostas HTTP 201, 200, 400 e 404 conforme os cenários executados.

## 11. Uso de Inteligência Artificial

Utilizei o ChatGPT como ferramenta de apoio durante o desenvolvimento e a execução do projeto.

A inteligência artificial auxiliou na compreensão dos requisitos, configuração do ambiente, interpretação de erros e orientação para execução dos testes.

Durante os testes no Postman, identifiquei um erro HTTP 404 causado por um endereço de requisição incorreto, que foi corrigido.

Também verifiquei uma tentativa de alteração de status que retornou HTTP 400 por uma transição não permitida. Posteriormente, a atualização para o status `cancelado` retornou HTTP 200.

Os testes foram executados por mim no ambiente local, e as evidências foram registradas e publicadas no meu repositório GitHub.

## 12. Identificação acadêmica

**Aluno:** Gustavo Valentim dos Santos  
**RGM:** 42190703  
**Instituição:** Universidade Cruzeiro do Sul  
**Disciplina:** Tópicos Avançados em Sistemas de Informação II  
**Projeto:** API de Gerenciamento de Pedidos  
**GitHub:** GustavoValentim03

## 13. Repositório do projeto

https://github.com/GustavoValentim03/API-Gerenciamento-de-Pedidos

---

**Projeto acadêmico desenvolvido por Gustavo Valentim dos Santos.**
