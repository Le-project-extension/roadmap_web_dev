# TypeScript: Tipagem Estatica e Escalabilidade

## Objetivo de Estudo
O JavaScript puro é flexível, mas essa flexibilidade se torna um risco em projetos grandes. O objetivo deste módulo é entender como o TypeScript adiciona uma camada de segurança ao código, capturando erros durante o desenvolvimento (em tempo de compilação) antes que eles cheguem ao usuário final.

## Fundamentos (Conceitos Essenciais)
O TypeScript é um *Superset* (superconjunto) do JavaScript. Isso significa que todo código JavaScript válido é um código TypeScript, mas o TS adiciona regras de tipagem estática.

### 1. Inferência vs. Tipagem Explícita
O TypeScript é inteligente o suficiente para deduzir o tipo de uma variável pelo seu valor inicial (Inferência), mas em estruturas complexas, precisamos ser explícitos.
```typescript
// Inferência (O TS sabe que é string, não precisa tipar)
let nomeDoProjeto = "Sistema de Ativos"; 

// Tipagem Explícita
let valorTotal: number = 1500.50;
let estaAtivo: boolean = true;
let categorias: string[] = ["Hardware", "Software", "Mobiliário"];
```
## 2. Interfaces e Types
A principal vantagem do TypeScript é criar "contratos" de dados. Se o backend promete enviar um ativo, o frontend precisa saber exatamente quais campos existem nesse ativo. Fazemos isso através de `Interfaces` ou `Types`.

```typeScript
// Criando o contrato de um Ativo
interface Ativo {
  id: string;
  nome: string;
  valor: number;
  dataAquisicao?: Date; // O "?" indica que este campo é opcional
}

// O TypeScript vai acusar erro se faltar o 'id', 'nome' ou 'valor'
const novoNotebook: Ativo = {
  id: "NTB-001",
  nome: "MacBook Pro",
  valor: 15000
};
```
## Temas para Pesquisa e Aprofundamento
Agora que você entendeu o básico da tipagem, pesquise como o TypeScript lida com cenários dinâmicos e configurações:

1. **O perigo do `any`:** Por que usar o tipo `any` é considerado uma má prática e anula o propósito do TypeScript? Qual a diferença entre `any` e `unknown`?

2. **Generics (`<T>`):** Como criar funções ou interfaces que funcionam com múltiplos tipos de dados sem perder a tipagem forte? (Pesquise a sintaxe de Generics).

3. **Utility Types:** O TypeScript possui ferramentas nativas para manipular tipos existentes. Pesquise o que fazem os utilitários `Partial<T>`, `Omit<T, K>` e `Pick<T, K>`.

4. **O arquivo `tsconfig.json:`** O que é o Strict Mode (modo estrito) e por que ele deve estar sempre ativado em projetos profissionais?

## Materiais de Apoio
1. **Documentação Oficial do TypeScript (Handbook):** A fonte da verdade para entender a sintaxe e os conceitos.

2. **TypeScript Cheat Sheets:** Resumos visuais oficiais de tipagem básica e avançada.

## Missao Pratica: Refatoracao Tipada
Para validar seu aprendizado, você vai evoluir o desafio do módulo de JavaScript adicionando segurança e previsibilidade ao código.

1. Instale o TypeScript globalmente na sua máquina (npm install -g typescript) ou utilize o `ts-node` para execução direta.

2. Crie um arquivo chamado `estudo-ts.ts`.

3. Crie uma `Interface` chamada `Funcionario` contendo os campos obrigatórios: `matricula` (número), `nome` (texto) e `departamento` (texto).

4. Crie uma `Interface` chamada `Equipamento` contendo: `codigoTag` (texto), `modelo` (texto), e um campo responsavel que deve ser obrigatoriamente do tipo `Funcionario`.

5. Crie um objeto que represente um equipamento válido seguindo o contrato acima.

6. Tente atribuir um texto (string) ao campo `matricula` do funcionário e observe o erro que o TypeScript vai gerar no seu editor de código.