# Gitflow: O Tráfego de Branches

## Objetivo de Estudo
Sua missão neste módulo é entender como organizar as ramificações (branches) do código em um projeto em equipe. Você vai descobrir como proteger o código que está em produção (sendo usado pelos clientes) enquanto vários desenvolvedores criam novas funcionalidades ao mesmo tempo, sem quebrar o sistema.

## Tópicos para Pesquisa
Imagine o cenário de um sistema real em produção, com centenas de usuários ativos neste exato segundo. Se um desenvolvedor cometer um erro direto no código principal, o sistema inteiro cai. Para evitar isso, o mercado adota o **Gitflow**. Pesquise e responda:
1. No fluxo do Gitflow, qual é o papel exclusivo da branch `main` (ou `master`)? Quem tem autorização para alterar ela diretamente?
2. Por que a branch `develop` existe e qual a relação dela com as novas funcionalidades criadas pela equipe?
3. Imagine que um erro crítico (um bug que impede o acesso, por exemplo) foi descoberto no sistema que já está no ar. Como o Gitflow orienta a correção desse problema sem misturar com códigos incompletos que ainda estão sendo desenvolvidos por outros devs?

## Radar de Branches
No padrão Gitflow, cada branch tem uma nomenclatura específica e um momento exato para nascer e para ser finalizada (fazer o *Merge*). Pesquise a utilidade, de onde nascem e para onde vão cada uma destas branches:

* `main` (ou `master`)
* `develop`
* `feature/`
* `release/`
* `hotfix/`

---

## Material de Apoio (Curadoria)
Para entender visualmente como essas branches nascem e se conectam ao longo do tempo, estude:
1. **[Fluxo de Trabalho Gitflow - Atlassian](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow)**: O guia definitivo do mercado sobre como aplicar o Gitflow na prática.
2. **[A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)**: O artigo original (em inglês) que definiu este modelo na comunidade de desenvolvimento.

---

## Missão Prática: O Primeiro Pull Request com Gitflow
Agora vamos simular o desenvolvimento de uma funcionalidade usando as regras rigorosas do Gitflow!

1. No seu terminal, abra a pasta do seu repositório `meu-primeiro-repo`.
2. A partir da sua branch `main`, crie uma nova branch chamada `develop` e mude para ela.
3. Agora, simulando que você vai começar a trabalhar em uma nova tarefa, crie uma branch de *feature* a partir da `develop` (exemplo: `feature/tela-login`).
4. Crie um arquivo chamado `login.md`, escreva algo dentro dele, adicione (`git add`) e faça o commit.
5. Envie a sua branch de feature para o GitHub (`git push`). *Dica: você pode precisar configurar o upstream na primeira vez.*
6. Acesse o seu repositório no GitHub e abra um **Pull Request (PR)** da sua branch de *feature* apontando para a branch `develop` (Atenção: não aponte para a `main`!).
