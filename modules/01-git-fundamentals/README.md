# 📘 Módulo 01 – Git Fundamentals

Neste módulo você aprenderá os **conceitos fundamentais do Git** e os comandos básicos utilizados no dia a dia.

Ao final deste módulo você será capaz de:

- criar um repositório Git
- registrar alterações com commits
- visualizar o histórico de mudanças
- conectar um repositório local a um repositório remoto

Este é o primeiro passo para trabalhar com **versionamento de código em projetos reais**.

---

## 🎯 Objetivos

Ao concluir este módulo você deverá ser capaz de:

- entender o que é **controle de versão**
- instalar e configurar o **Git**
- utilizar comandos essenciais:

    ```bash
    init
    clone
    add
    commit
    status
    log
    push
    pull
    ```

---

## 📖 Materiais recomendados

**Escolha os recursos que melhor se adaptam ao seu estilo de aprendizagem.**

### Se você aprende melhor lendo

* 📄 [Pro Git (Capítulos 1 e 2)](https://git-scm.com/book/pt-br/v2)
* 📄 [Guia Rápido do Git](https://rogerdudler.github.io/git-guide/index.pt_BR.html)

### Se você aprende melhor com vídeos

* 🎥 [Entendendo GIT | (não é um tutorial!)](https://www.youtube.com/watch?v=6Czd1Yetaac)
* 🎥 [GIT: Minicurso para Você Sair do Zero! (Aprenda em 45 Minutos)](https://www.youtube.com/watch?v=ts-H3W1uLMM)
* 🎥 [Git e GitHub](https://www.youtube.com/playlist?list=PLhkO7OMKgT_rqwGYldqcFxyN4yjFgmDh8)
* 🎥 [Curso de Git e Github [Completo] - Aprenda o Essencial em 2 horas](https://www.youtube.com/watch?v=192HgwRgOYE)

---

# 📝 Checklist do módulo

> ⚠️ **Esse checklist não substitui o estudo dos materiais recomendados.**
> Ele serve apenas para verificar se você **praticou os conceitos do módulo**.

---

## 🛠 Instalar o Git

* [ ] Baixar e instalar o Git a partir do [site oficial](https://git-scm.com/)

    Verifique se a instalação foi concluída corretamente:

    ```bash
    git --version
    ```

---

## 🛠 Configurar seu usuário no Git

* [ ] Configurar nome e e-mail que aparecerão nos commits

    ```bash
    git config --global user.name "Seu Nome"
    git config --global user.email "seu@email.com"
    ```

> Essas informações serão registradas em cada commit.

---

## 🛠 Criar um repositório local

* [ ] Criar uma pasta para o projeto

    Exemplo no terminal:

    ```bash
    mkdir meu-projeto
    cd meu-projeto
    ```

* [ ] Agora inicialize o repositório Git:

    ```bash
    git init
    ```

> Isso cria a pasta `.git`, onde o histórico do projeto será armazenado.

⚠️ **Importante**

Execute `git init` **dentro da pasta do projeto**.

Se você executar esse comando na pasta do usuário (por exemplo `C:\Users\seu-nome`), o Git começará a rastrear **todos os arquivos dessa pasta**.

---

## 🧠 Entender o modelo mental do Git

* [ ] Ler o material abaixo antes de continuar

➡️ [Modelo Mental do Git](./git-mental-model.md)

Compreender esse modelo ajuda a entender **como o Git registra e organiza mudanças no projeto**.

---

## 🛠 Registrar mudanças com commits

* [ ] Adicionar arquivos ao controle de versão

    ```bash
    git add .
    ```

* [ ] Criar um commit:

    ```bash
    git commit -m "mensagem do commit"
    ```

### Boas práticas para commits

Commits representam **unidades de mudança no projeto**.

Para aprender como escrever boas mensagens de commit e utilizar o padrão **Conventional Commits**, consulte:

📄 [Boas práticas de commits](./conventional_commits.md)

---

## 🛠 Visualizar o histórico do projeto

* [ ] Inspecionar o estado e histórico do repositório

    ```bash
    git status
    git log
    ```

---

## 🛠 Criar um repositório remoto

* [ ] Criar uma conta em uma plataforma de hospedagem Git

    Exemplos de plataformas:

    * GitHub
    * GitLab

    Acesse:

    * [https://github.com](https://github.com)
    * [https://gitlab.com](https://gitlab.com)

    Crie um novo repositório na plataforma escolhida.

---

## 🔐 Configurar autenticação com SSH

* [ ] Configurar uma chave SSH para autenticação

    Para enviar código para plataformas como GitHub ou GitLab, é necessário configurar um método de autenticação.

    Uma das formas mais utilizadas é a **autenticação via SSH**, que permite conectar seu computador ao repositório remoto **sem precisar digitar usuário e senha a cada operação**.

    Consulte o guia oficial da plataforma que você estiver utilizando:

    * 🔐 [Configurar SSH no GitHub](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh)
    * 🔐 [Configurar SSH no GitLab](https://docs.gitlab.com/ee/user/ssh.html)

    Após configurar sua chave SSH, você poderá utilizar URLs como:

    ```
    git@github.com:usuario/repositorio.git
    ```

> Essa configuração precisa ser feita **apenas uma vez por computador**.

---

## 🛠 Conectar o repositório local ao remoto

* [ ] Conectar o repositório local ao remoto

    ```bash
    git remote add origin <URL_DO_REPOSITORIO>
    ```

---

## 🛠 Enviar seu código para o repositório remoto

* [ ] Enviar o primeiro commit

    ```bash
    git push -u origin main
    ```

> **Observação:** o parâmetro `-u` (`--set-upstream`) define a branch remota `origin/main` como referência para sua branch local `main`.
> Após executar esse comando pela primeira vez, você poderá utilizar apenas `git push` e `git pull`.

---

## 🛠 Atualizar seu repositório local

* [ ] Trazer mudanças do repositório remoto

    ```bash
    git pull
    ```

---

## 🛠 Clonar um repositório existente

* [ ] Clonar um repositório remoto

    ```bash
    git clone <URL_DO_REPOSITORIO>
    ```

Após clonar, faça uma alteração simples no `README.md`, crie um commit e envie a alteração.
