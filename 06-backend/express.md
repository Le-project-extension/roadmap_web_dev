# Express.js: Construcao de APIs RESTful

## Objetivo de Estudo
O Node.js puro permite criar servidores web, mas o processo é verboso e complexo. O objetivo deste módulo é entender como o micro-framework Express.js simplifica o roteamento, a manipulação de requisições e a estruturação de APIs que farão a ponte entre o banco de dados e o frontend.

## Fundamentos (Conceitos Essenciais)
O Express atua como um gerenciador de tráfego. Ele escuta uma porta do servidor e, dependendo da URL (Rota) e da intenção (Verbo HTTP) da requisição, direciona o usuário para o bloco de código correto.

### O Ciclo Request / Response
Toda rota no Express lida com dois objetos fundamentais:
* **`req` (Request):** Contém os dados de quem está chamando a API (parâmetros da URL, corpo da mensagem, cabeçalhos de autenticação).
* **`res` (Response):** O objeto usado para devolver a resposta ao cliente (um JSON com os dados, uma mensagem de erro ou um código de status).

```javascript
// Exemplo da base de um servidor Express
const express = require('express');
const app = express();

// Rota básica
app.get('/status', (req, res) => {
  res.json({ mensagem: "Servidor operando normalmente!" });
});

app.listen(3000, () => {
  console.log('Servidor rodando na porta 3000');
});
```
## Temas para Pesquisa e Aprofundamento
Construir uma API profissional exige seguir os padrões do mercado. Pesquise e documente os seguintes conceitos:

1. **Padrão REST:** O que significa construir uma API "RESTful"? Quais são as boas práticas para nomear rotas (ex: `/listarAtivos` vs `/ativos`)?

2. **Métodos HTTP (Verbos):** Qual o propósito semântico de cada um dos métodos abaixo na manipulação de recursos?

- GET

- POST

- PUT

- PATCH

- DELETE

3. **Códigos de Status HTTP:** O que significam as famílias de códigos de status na resposta de uma API? Pesquise os códigos: 200, 201, 400, 401, 404 e 500.

4. **Middlewares:** Este é o conceito mais poderoso do Express. O que é uma função Middleware? Como ela intercepta o fluxo entre o Request e o Response?

## Materiais de Apoio
1. **Documentação Oficial do Express:** Guia de roteamento e middlewares.

2. **MDN Web Docs (HTTP):** Referência técnica sobre códigos de status e métodos HTTP.

3. **Ferramentas de Teste de API:** Pesquise sobre o Insomnia ou Postman para testar suas rotas sem precisar de um frontend.

## Missao Pratica: A Primeira API de Ativos
Para validar seu aprendizado, você vai construir a primeira versão da API do nosso sistema de gestão, utilizando dados em memória (sem banco de dados real ainda).

1. Inicie um projeto Node.js (`npm init -y`) e instale o Express (`npm install express`).

2. Crie um arquivo `server.js`.

3. Declare um array vazio chamado `ativos` para simular nosso banco de dados em memória.

4. Crie uma rota GET em `/ativos` que retorne a lista completa de ativos (o array).

5. Crie uma rota POST em `/ativos` que receba os dados de um novo ativo no corpo da requisição (JSON), adicione esse objeto ao array e retorne um código de status de "Criado" com sucesso.

Dica: Você precisará habilitar um middleware nativo do express (`express.json()`) para ler o corpo (body) da requisição.