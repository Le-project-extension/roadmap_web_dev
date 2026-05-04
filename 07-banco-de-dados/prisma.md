# Prisma ORM: Banco de Dados com Tipagem Segura

## Objetivo de Estudo
Escrever comandos SQL manualmente (Raw SQL) diretamente no código da aplicacao pode ser repetitivo e propenso a erros. O objetivo deste modulo e entender como um ORM (Object-Relational Mapping) abstrai a complexidade do banco de dados, permitindo manipular registros como se fossem simples objetos JavaScript/TypeScript, garantindo segurança de tipagem e produtividade.

## Fundamentos (Conceitos Essenciais)
O Prisma se destaca por ser fortemente tipado. O coracao do Prisma e o arquivo `schema.prisma`. E nele que modelamos a estrutura do nosso banco de dados utilizando uma sintaxe propria, limpa e declarativa. A partir desse arquivo, o Prisma gera o cliente que usaremos na aplicacao.

### O Arquivo de Schema
Abaixo temos um exemplo de como declarar uma tabela (Model) no Prisma:
```prisma
// Exemplo de um arquivo schema.prisma
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "sqlite" // Pode ser postgresql, mysql, etc.
  url      = env("DATABASE_URL")
}

model Categoria {
  id        String   @id @default(uuid())
  nome      String   @unique
  createdAt DateTime @default(now())
}
```

## Temas para Pesquisa e Aprofundamento
O uso de um ORM facilita a vida, mas esconde a complexidade do banco. Para nao ser refem da ferramenta, pesquise os conceitos abaixo:

1. **O que e um ORM?** Pesquise o conceito de Object-Relational Mapping. Quais sao as vantagens de usa-lo em comparacao a escrever consultas SQL puras (Raw SQL)? Qual e o impacto na performance?

2. **Migrations (Migracoes):** O que sao as Migrations no contexto de banco de dados? Por que elas sao essenciais quando se trabalha em equipe, operando como um "Git para o banco de dados"?

3. **Relacionamentos (Relations):** Como representar as ligacoes entre tabelas? Pesquise como o Prisma mapeia as relacoes "1 para N" (Um para Muitos) e "N para N" (Muitos para Muitos).

4. **Prisma Client:** Pesquise como utilizar os metodos assincronos do Prisma Client (`findUnique`, `findMany`, `create`, `update`, `delete`) para realizar um CRUD completo.

## Materiais de Apoio
1. **Documentacao Oficial do Prisma:** Referencia obrigatoria. Pesquise a secao "Prisma Schema Reference" para entender todos os atributos disponiveis.

2. **Prisma Quickstart:** Tutorial oficial de inicializacao rapida do Prisma com SQLite e TypeScript.

## Missao Pratica: Modelagem e Migracao Inicial
Para validar seu aprendizado, vamos configurar o Prisma localmente utilizando um banco de dados SQLite (que dispensa a instalacao de um servidor de banco pesado neste primeiro momento) e criar a tabela principal do nosso sistema.

1. No seu projeto Node.js, instale o Prisma como dependencia de desenvolvimento e inicialize-o utilizando o SQLite:

  - `npm install prisma --save-dev`

  - `npx prisma init --datasource-provider sqlite`

2. Abra o arquivo prisma/schema.prisma gerado.

3. Crie um `model` chamado `Ativo`. Este model deve conter os seguintes campos:

  - `id` (Uma String, chave primaria e gerada automaticamente como UUID).

  - `codigoPatrimonio` (Uma String, obrigatoria e unica).

  - `nome` (Uma String obrigatoria).

  - `valor` (Um Float).

  - `dataAquisicao` (Um DateTime com valor padrao sendo a data atual).

4. Execute o comando para gerar a primeira migration do banco de dados: `npx prisma migrate dev --name init`

5. Abra a interface de administracao visual do Prisma executando: `npx prisma studio`

6. Atraves da interface web do Prisma Studio, adicione manualmente um novo Ativo ao banco de dados.

