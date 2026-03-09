# 🌿 Módulo 02 – Branching, Commits e Workflows

>Neste módulo, vamos aprofundar o uso do Git em um contexto colaborativo. Você aprenderá como ramificar o seu projeto (branching), seguir boas práticas para escrever mensagens de commit e entender os principais workflows usados em times de desenvolvimento. Esses conceitos são essenciais para trabalhar de forma organizada e eficiente em equipe.

## 🎯 Objetivos
✅ Aprender como criar branches     
✅ Aplicar padrões semânticos em mensagens de commit    
✅ Compreender e aplicar workflows de desenvolvimento colaborativo  

---

## 📖 Materiais Recomendados

*Escolha os recursos que melhor se adaptam ao seu estilo de aprendizagem:*

**Se você aprende melhor lendo**
- 📄 [Pro Git (Capítulos 3 e 5)](https://git-scm.com/book/pt-br/v2)
- 📄 [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)

**Se você aprende melhor com vídeos**
- 🎥 [Git Branches de forma fácil e com exemplo - Curso de Git e GitHub](https://www.youtube.com/watch?v=xAOBQtSVI_k)
- 🎥 [Usando várias branches no GIT e GITHUB!](https://www.youtube.com/watch?v=lWhe6tUITUU)
- 🎥 [Essa é a forma que eu crio meus commits (conventional commits)](https://www.youtube.com/watch?v=sStBPj7JJpM)

---

## 🌿 Branching

>**Branching** (ou "ramificação") é uma funcionalidade do Git que permite criar uma linha paralela de desenvolvimento. Com ela, você pode trabalhar em novas funcionalidades, corrigir bugs ou testar ideias sem afetar o código da `main` (linha principal do projeto).

**Branches são fundamentais para manter a organização do projeto e evitar conflitos quando várias pessoas trabalham simultaneamente.**

### 🔹 Convenção sugerida para nomes de branches:
- `feature/nome-da-funcionalidade` → Para novas funcionalidades
- `fix/nome-do-bug` → Para correção de bugs
- `docs/nome-da-doc` → Para alterações na documentação
- `refactor/nome-da-alteracao` → Para melhorias internas de código (sem mudar comportamento)

>Essas convenções facilitam a leitura do histórico e a organização do trabalho na equipe.

---

## 📝 Commits

>Commits são os registros das alterações feitas no repositório. Cada commit deve representar uma mudança lógica e coesa no código, isso torna o histórico mais limpo, útil e fácil de entender.

⚠️ Evite mensagens genéricas como “update” ou “ajustes”. Prefira mensagens claras e descritivas.

### 🔹 Padrão de Commits Semânticos ([Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/))

**Formato:**  

```bash
<tipo>: descrição curta
```

**Exemplos:**  

- `feat: adicionar função de busca de usuários`
- `fix: corrigir bug na função de login`
- `docs: atualizar README com exemplos`

**Tipos mais usados:**  

- `feat` → nova funcionalidade  
- `fix` → correção de bug  
- `docs` → documentação  
- `style` → ajustes de formatação (espaços, quebras de linha etc.)
- `refactor` → melhoria no código sem alterar a funcionalidade  
- `test` → criação/alteração de testes  

---

## 🔄 Workflows

>**Workflows** definem a forma como uma equipe estrutura o desenvolvimento de software com Git. Eles variam conforme o tamanho e a complexidade do projeto.

### 📌 GitHub Flow (ideal para projetos simples e contínuos)

1. Criar uma branch a partir da `main`
2. Fazer commits com alterações relacionadas
3. Abrir um Pull Request (PR)
4. Solicitar revisão
5. Após aprovação, realizar merge com a `main`

>Esse fluxo é ideal para projetos em que novas versões são liberadas com frequência.

### 📌 Git Flow (ideal para projetos mais complexos ou com versões bem definidas)

**Principais branches:**

* `main` → versão de produção
* `develop` → onde novas funcionalidades são integradas antes da produção

**Branches auxiliares:**

* `feature/nome` → novas funcionalidades
* `release/nome` → preparação de uma nova versão
* `hotfix/nome` → correções urgentes diretamente na produção

>Esse fluxo é mais estruturado e ideal para equipes maiores.

---

## 🚀 Checklist do Módulo

* [ ] Criar uma nova branch e navegar até ela (`git checkout -b`)
* [ ] Fazer alterações e criar commits com mensagens semânticas
* [ ] Enviar a branch para o repositório remoto (`git push -u origin`)
* [ ] Abrir um Pull Request no GitHub
* [ ] Revisar e fazer merge da branch na `main`

---
---

> ℹ️ **Importante:**
>
> Estratégias de branching, padrões de commits e workflows de desenvolvimento **podem variar bastante** entre empresas e equipes.
> O que estou apresentando aqui é uma abordagem comum e funcional, mas:
>
> * Algumas equipes usam [**Git Flow**](https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar), outras preferem [**GitHub Flow**](https://docs.github.com/pt/get-started/using-github/github-flow) ou [**Trunk-Based Development**](https://www.objective.com.br/insights/trunk-based-development/).
> * Os commits podem seguir o padrão **Conventional Commits**, usar mensagens livres ou incluir **IDs de tickets** (ex: `feat(JIRA-123): novo componente`).
> * O fluxo de trabalho pode exigir **revisão de código obrigatória**, **integração contínua**, **políticas de merge**, entre outros processos.
>
> ✅ **Dica:** Sempre consulte as diretrizes da sua equipe ou projeto e adapte-se ao que fizer mais sentido no seu contexto de trabalho.

---
---