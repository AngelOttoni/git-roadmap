# 🌿 **Módulo 02 – Branching and History**

Neste módulo você vai aprofundar o uso do Git trabalhando com **branches**, **histórico de commits** e boas práticas para registrar mudanças no projeto.

Esses conceitos são essenciais para manter projetos organizados, especialmente quando várias pessoas trabalham no mesmo repositório.

Ao final deste módulo você compreenderá como o Git gerencia **múltiplas linhas de desenvolvimento** e como integrar mudanças de forma segura.

---

## 🎯 **Objetivos**

Ao concluir este módulo você deverá ser capaz de:

* criar e gerenciar **branches**
* compreender como o Git organiza o **histórico de commits**
* integrar mudanças utilizando **merge**
* entender o conceito de **rebase**
* resolver **conflitos de merge**
* explorar o histórico do projeto

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

>Uma **branch** é uma linha paralela de desenvolvimento.

Ela permite trabalhar em novas funcionalidades, correções ou experimentos **sem alterar diretamente a branch principal (`main`)**.

*Esse mecanismo é essencial para permitir que várias pessoas trabalhem simultaneamente no mesmo projeto.*

---

## Criando e navegando entre branches

Criar uma nova branch:

```bash
git branch minha-branch
```

Criar e mudar para uma nova branch:

```bash
git checkout -b minha-branch
```

Listar branches existentes:

```bash
git branch
```

### Convenção sugerida para nomes de branches

> Embora o Git permita qualquer nome para branches, muitos projetos utilizam
convenções para facilitar a organização do trabalho.

Alguns exemplos comuns:

- `feature/nome-da-funcionalidade`
- `fix/nome-do-bug`
- `docs/descricao-da-alteracao`
- `refactor/nome-da-melhoria`

Essas convenções ajudam a entender rapidamente o propósito da branch e são frequentemente utilizadas em workflows colaborativos.

---

# 🔄 Integrando mudanças com merge

Após finalizar o trabalho em uma branch, você pode integrá-la à `main`.

```bash
git checkout main
git merge minha-branch
```

O Git irá combinar o histórico das duas branches.

Quando as alterações não entram em conflito, o merge acontece automaticamente.

---

# 🔀 Rebase (conceito)

O **rebase** é uma alternativa ao merge para integrar mudanças entre branches.

Enquanto o **merge preserva o histórico original das branches**, o **rebase reescreve o histórico**, movendo commits para uma nova base.

Exemplo conceitual:

```text
main:     A---B---C
feature:       D---E
```

Após um `rebase` da branch `feature` sobre `main`:

```text
main:     A---B---C
feature:           D'---E'
```

⚠️ *O rebase pode deixar o histórico mais linear, mas deve ser usado com cuidado em branches compartilhadas.*

---

🔄 **Sobre `merge` e `rebase` veja mais detalhes em:**

➡️ [Merge vs Rebase](./merge-vs-rebase.md)

---

# 🚨 Resolução de conflitos

Conflitos podem ocorrer quando **duas branches modificam a mesma parte de um arquivo**.

Quando isso acontece durante um merge ou rebase, o Git pede que você resolva manualmente o conflito.

Use:

```bash
git status
```

para identificar arquivos em conflito.

O Git marcará as diferenças diretamente no arquivo:

```text
<<<<<<< HEAD
código atual
=======
código da outra branch
>>>>>>> minha-branch
```

Você deve editar o arquivo escolhendo qual versão manter (ou combinando as duas).

Depois de resolver o conflito:

```bash
git add <nome_do_arquivo>
git commit "mensagem"
```

---

# 📜 Explorando o histórico do Git

O Git registra toda a evolução do projeto.

Alguns comandos úteis:

```bash
git log
git log --oneline
git log --oneline --graph
git log --oneline --graph --decorate --all
```

Esses comandos ajudam a entender como o projeto evoluiu ao longo do tempo.

Para um resumo rápido dos principais comandos Git, consulte:

➡️ [`resources/cheatsheets.md`](../../resources/cheatsheets.md)

---

# 🚀 Checklist do módulo

* [ ] Criar uma nova branch (`git checkout -b`)
* [ ] Fazer alterações no projeto
* [ ] Criar commits com mensagens claras
* [ ] Visualizar o histórico com `git log`
* [ ] Integrar a branch com `merge`
* [ ] Resolver um conflito simples de merge
