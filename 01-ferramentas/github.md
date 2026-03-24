# GitHub: A Vitrine e o Motor Colaborativo

## 🎯 Objetivo de Estudo
Sua missão neste módulo é tirar o seu código do "isolamento" do seu computador e levá-lo para a nuvem. Você vai entender como times inteiros de desenvolvimento colaboram no mesmo projeto sem sobrescrever o trabalho uns dos outros, usando o GitHub como plataforma central.

## 🔍 Tópicos para Pesquisa
Antes de subir qualquer código, garanta que você consegue explicar:
1. O que é um repositório "Remote" (remoto) no contexto do Git?
2. O que é um **Pull Request (PR)** e por que ele é a cerimônia mais importante na cultura de engenharia de software?
3. Para que servem as **Issues** do GitHub e como elas se conectam com a organização do trabalho?
4. Qual a diferença prática entre fazer um *Clone* e fazer um *Fork* de um repositório?

## ⚙️ Radar de Comandos e Conceitos
Descubra o que cada um destes comandos faz. Eles são a ponte entre a sua máquina local e a nuvem:

* `git remote add origin [URL]`
* `git push` (e entenda o que a flag `-u` ou `--set-upstream` faz na primeira vez)
* `git pull` (e a diferença básica para o `git fetch`)
* **Pull Request (PR)** (Conceito na interface do GitHub)
* **Merge** (Conceito na interface do GitHub)

---

## 📚 Material de Apoio (Curadoria)
Para dominar o fluxo de trabalho na plataforma, estude estes links:
1. **[Hello World - GitHub Docs](https://docs.github.com/pt/get-started/quickstart/hello-world)**: O tutorial oficial e obrigatório do próprio GitHub ensinando o fluxo de criar repo, branch, commit e PR.
2. **[Entendendo o fluxo do GitHub (GitHub Flow)](https://docs.github.com/pt/get-started/quickstart/github-flow)**: Um guia visual e conceitual de como o trabalho flui em equipes profissionais.

---

## 🚀 Missão Prática: O Primeiro Deploy de Código
Chegou a hora de mostrar o seu trabalho para o mundo (e garantir mais pontos na nossa gamificação!). Para esta missão, vamos conectar o repositório local que você criou na missão de Git com a nuvem do GitHub.

1. Acesse sua conta no [GitHub](https://github.com/).
2. Crie um **novo repositório público** chamado `missao-extensao-git` (não inicialize com README, .gitignore ou licença, deixe-o 100% em branco).
3. No seu terminal local, navegue até aquela pasta `meu-primeiro-repo` da missão anterior (que já tem o Git inicializado e os seus commits).
4. Use o comando `git remote add origin` com a URL do seu novo repositório no GitHub para criar a ponte entre eles.
5. Envie (faça o *push*) do seu código local para a nuvem.
6. Atualize a página do seu repositório no navegador e veja os seus arquivos e histórico de commits aparecerem lá!
