# Banco de Dados e SQL: Persistencia e Relacionamentos

## Objetivo de Estudo
Ate agora, os dados que manipulamos em variaveis e arrays desaparecem assim que o servidor e reiniciado. O objetivo deste modulo e introduzir o conceito de persistencia de dados estruturada. Voce deve compreender o modelo relacional, como as informacoes se conectam e como utilizar a linguagem SQL para interagir com essas bases.

[Ilustracao visual de tabelas relacionais conectadas por chaves primarias e estrangeiras]

## Fundamentos (Conceitos Essenciais)
Um banco de dados relacional armazena dados em tabelas, de forma muito semelhante a uma planilha do Excel. No entanto, ele impoe regras rigidas sobre os tipos de dados e garante que as informacoes nao se percam ou se corrompam.

A linguagem padrao para conversar com esses bancos de dados relacionais (como PostgreSQL, MySQL, SQL Server e SQLite) e o **SQL (Structured Query Language)**. E atraves do SQL que pedimos ao banco para ler, inserir, atualizar ou deletar registros.

## Temas para Pesquisa e Modelagem
Antes de escrever comandos, e preciso saber estruturar a informacao. Pesquise e documente os conceitos fundamentais de modelagem relacional:

1. **Entidades e Atributos:** No contexto de banco de dados, o que representam as Entidades (Tabelas) e os Atributos (Colunas)?
2. **Chave Primaria (Primary Key - PK):** Qual a funcao desta chave em uma tabela? Por que ela deve ser unica e nunca nula?
3. **Chave Estrangeira (Foreign Key - FK):** Como esta chave e utilizada para criar relacionamentos entre duas tabelas diferentes?
4. **Propriedades ACID:** Na engenharia de software, bancos relacionais garantem transacoes ACID. O que significam Atomicidade, Consistencia, Isolamento e Durabilidade?

## Radar de Comandos SQL (CRUD)
O acronimo CRUD (Create, Read, Update, Delete) define as quatro operacoes basicas de armazenamento. Utilize a tabela abaixo para pesquisar a sintaxe e as armadilhas dos comandos SQL:

| Comando SQL | Desafio de Pesquisa |
| :--- | :--- |
| `CREATE TABLE` | Como definir os tipos de dados (texto, numero, data) ao criar uma tabela nova? |
| `INSERT INTO` | Qual a sintaxe correta para inserir multiplos registros de uma unica vez? |
| `SELECT` | Como utilizar a clausula `WHERE` para filtrar apenas os resultados que atendem a uma condicao especifica? |
| `UPDATE` | Qual o perigo fatal de executar um comando UPDATE ou DELETE esquecendo a clausula `WHERE`? |
| `JOIN` (INNER JOIN) | Como este comando funciona para unir dados de duas tabelas separadas em uma unica consulta (ex: unir Funcionario com Departamento)? |

---

## Materiais de Apoio
1. **W3Schools SQL Tutorial:** Um guia interativo excelente para testar comandos SQL direto no navegador.
2. **PostgreSQL Tutorial:** Documentacao educacional do banco de dados relacional mais adotado pelo mercado atual.

---

## Missao Pratica: Primeiras Consultas (Sem Instalacao)
Para focar puramente na linguagem SQL sem se preocupar em instalar servidores de banco de dados pesados na sua maquina neste momento, vamos utilizar um ambiente de simulacao online.

1. Acesse a plataforma online **DB Fiddle** (ou SQL Fiddle).
2. Na secao de "Schema SQL" (ou lado esquerdo), escreva o comando `CREATE TABLE` para criar uma tabela chamada `Categoria`. Ela deve ter duas colunas: `id` (numero inteiro) e `nome` (texto).
3. Logo abaixo, escreva o comando `INSERT INTO` para adicionar tres categorias ao banco: "Hardware", "Software" e "Mobiliario".
4. Na secao de "Query SQL" (ou lado direito), escreva um comando `SELECT` para listar todas as categorias cadastradas.
5. Escreva um segundo comando `SELECT` utilizando a clausula `WHERE` para buscar especificamente a categoria cujo nome seja "Hardware".
6. Clique no botao de executar (Run) e observe a tabela de resultados aparecer na tela.
