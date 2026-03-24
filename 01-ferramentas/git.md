# 🗃️ Git: O sistema de Versionamento

## 🎯 Objetivo de Estudo
Sua missão neste módulo é entender o conceito de versionamento de código, como o Git gerencia o histórico do seu projeto e dominar os comandos essenciais para trabalhar no seu próprio computador.

## 🔍 Tópicos para Pesquisa
Antes de digitar qualquer comando no terminal, garanta que você sabe explicar com suas próprias palavras:
1. O que é o Git e qual é o principal problema que ele resolve na vida de um desenvolvedor?
2. Qual a diferença fundamental entre **Git** e **GitHub**?
3. O que são e como funcionam os três estados principais de um arquivo no Git (*Modified*, *Staged* e *Committed*)?

## ⚙️ Radar de Comandos
Pesquise a sintaxe e utilidade de cada um dos comandos abaixo. Eles formarão a base do seu dia a dia no projeto:

* `git init`
* `git clone`
* `git remote`
* `git status`
* `git add` (e entenda o que faz o `git add .`)
* `git commit -m "..."`
* `git log`
* `git branch`
* `git checkout` (pesquise também sobre o `git switch`)

---

## 📚 Material de Apoio 
Para ajudar na sua pesquisa, consulte estes materiais oficiais e interativos:
1. **[Learn Git Branching](https://learngitbranching.js.org/?locale=pt_BR)**: Um jogo interativo e visual excelente para entender como as branches funcionam na prática.
2. **[Livro Oficial Pro Git (PT-BR)](https://git-scm.com/book/pt-br/v2)**: A bíblia do Git. Os capítulos 1 e 2 são leitura obrigatória para qualquer dev.
3. **[Guia Prático do Git](https://rogerdudler.github.io/git-guide/index.pt_BR.html)**: Um tutorial simples, direto e sem enrolação.

---

## 🚀 Missão Prática: O Primeiro Histórico
Esta etapa vale pontos na nossa jornada de capacitação! Para provar que você configurou e entendeu o básico do Git localmente, cumpra o desafio abaixo no seu terminal:

1. Crie uma pasta no seu computador chamada `meu-primeiro-repo`.
2. Entre na pasta e inicialize o Git.
3. Crie um arquivo chamado `hello.txt` e escreva uma frase nele.
4. Adicione o arquivo à *stage area* (área de preparação).
5. Faça um commit com a mensagem `"Meu primeiro commit no projeto"`.
6. Altere o texto do arquivo `hello.txt`, adicione novamente e faça um segundo commit com a mensagem `"Atualiza o arquivo com nova frase"`.
7. Rode o comando que exibe o histórico de commits.
