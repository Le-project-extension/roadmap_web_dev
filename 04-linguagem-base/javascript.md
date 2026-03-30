# JavaScript: A Linguagem da Web

## Objetivo de Estudo
O objetivo deste modulo e compreender os fundamentos da linguagem que move o desenvolvimento web moderno. Voce deve investigar como o JavaScript funciona internamente, sua sintaxe baseada nos padroes ECMAScript e como ele gerencia o fluxo de dados de forma assincrona.

## Temas para Pesquisa
Pesquise e defina os conceitos que formam a base da linguagem:

1. **Motores JavaScript (Engines):** O que e o motor V8 e qual o papel dele no navegador e no Node.js?
2. **ECMAScript (ES6+):** O que e o comite TC39 e por que o lancamento do ES6 em 2015 foi um marco para a linguagem?
3. **Tipagem Dinamica e Fraca:** O que significa dizer que o JavaScript e dinamicamente tipado? Quais os riscos e beneficios disso?
4. **Ambientes de Execucao:** Qual a diferenca pratica entre executar JavaScript no Browser (Navegador) e no Node.js?

## Pilares Tecnicos
Utilize a tabela abaixo para guiar sua pesquisa sobre os recursos essenciais da sintaxe moderna:

| Conceito | Desafio de Pesquisa |
| :--- | :--- |
| Variaveis | Qual a diferenca de escopo e comportamento entre var, let e const? |
| Tipos de Dados | Diferencie tipos Primitivos de tipos de Referencia (Objetos/Arrays). |
| Arrow Functions | O que muda na sintaxe e no comportamento do "this" em relacao as funcoes tradicionais? |
| Desestruturacao | Como extrair dados de objetos e arrays de forma simplificada (Destructuring)? |
| Manipulacao de Arrays | Como funcionam os metodos map, filter e reduce? |
| Assincronismo | O que sao Promises e qual a vantagem de usar a sintaxe Async/Await? |

---

## Materiais de Apoio
1. **MDN Web Docs (Mozilla):** A documentacao de referencia oficial e mais completa para desenvolvedores web.
2. **Eloquent JavaScript (Livro):** Uma das obras mais respeitadas sobre a linguagem (disponivel online gratuitamente).
3. **JavaScript.info:** Um guia moderno que vai do basico ao avancado com explicacoes detalhadas.

---

## Missao Pratica: Logica de Ativos
Para validar sua pesquisa, voce deve criar um script funcional que simule a manipulacao de dados do nosso projeto de extensao:

1. Crie um arquivo chamado `estudo-js.js` no seu computador.
2. Declare um Array de Objetos chamado `ativos`. Cada objeto deve representar um ativo com as propriedades: `nome` (string), `tipo` (string) e `valor` (number).
3. Utilize o metodo `filter` para criar uma nova lista apenas com ativos acima de um determinado valor.
4. Utilize o metodo `map` para gerar uma lista apenas com os nomes dos ativos em caixa alta (Uppercase).
5. Crie uma funcao assincrona (Async) que simule a busca de um ativo pelo nome e utilize `console.log` para exibir o resultado.
