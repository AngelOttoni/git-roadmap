# 📘 Módulo 01 – Git Fundamentals

Neste módulo você aprenderá os **conceitos fundamentais do Git** e os comandos básicos utilizados no dia a dia.

Ao final deste módulo você será capaz de:

* criar um repositório Git
* registrar alterações com commits
* visualizar o histórico de mudanças
* conectar um repositório local a um repositório remoto

Este é o primeiro passo para trabalhar com **versionamento de código em projetos reais**.

---

# 🎯 Objetivos

Ao concluir este módulo você deverá ser capaz de:

* entender o que é **controle de versão**
* instalar e configurar o **Git**
* utilizar comandos essenciais:

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

> Antes de começar a usar comandos, é importante entender como o **Git** organiza as mudanças no projeto.

---

## 📖 Materiais Recomendados

*Escolha os recursos que melhor se adaptam ao seu estilo de aprendizagem:*

**Se você aprende melhor lendo**
- 📄 [Pro Git (Capítulos 1 e 2)](https://git-scm.com/book/pt-br/v2)
- 📄 [Guia Rápido do Git](https://rogerdudler.github.io/git-guide/index.pt_BR.html)

**Se você aprende melhor com vídeos**
- 🎥 [Entendendo GIT | (não é um tutorial!)](https://www.youtube.com/watch?v=6Czd1Yetaac)
- 🎥 [GIT: Minicurso para Você Sair do Zero! (Aprenda em 45 Minutos)](https://www.youtube.com/watch?v=ts-H3W1uLMM)
- 🎥 [Git e GitHub](https://www.youtube.com/playlist?list=PLhkO7OMKgT_rqwGYldqcFxyN4yjFgmDh8)
- 🎥 [Curso de Git e Github [Completo] - Aprenda o Essencial em 2 horas](https://www.youtube.com/watch?v=192HgwRgOYE)


---

## 📝 Checklist do módulo:

### **1. Instalar o Git**

- Baixe e instale o Git a partir do [site oficial](https://git-scm.com/).

- Verifique a instalação:

    ```bash
    git --version
    ```

---

### **2. Configurar seu usuário no Git**

- Configure seu nome e e-mail para que seus commits sejam identificados corretamente.

    ```bash
    git config --global user.name "Seu Nome"
    git config --global user.email "seu@email.com"
    ```

    > Essas informações serão registradas em cada commit.

---

### **3. Criar um repositório local**

- Crie uma pasta para o projeto e inicialize um repositório Git:

    ```bash
    git init
    ```

    > Isso cria a pasta `.git`, onde o histórico do projeto será armazenado.

---

### 🧠 **4. Entendendo o modelo mental do Git**

Antes de continuar, é importante compreender como o Git organiza as mudanças no projeto.

Leia:

➡️ [Modelo Mental do Git](./git-mental-model.md)

---

### **5. Registrar mudanças com commits**

- Adicione arquivos ao controle de versão:

    ```bash
    git add .
    ```

    Crie um commit:

    ```bash
    git commit -m "<tipo>: mensagem do commit"
    ```
---

#### 📝 Boas práticas para commits

Commits representam **unidades de mudança no projeto**.

Cada commit deve representar **uma alteração lógica e coesa**.

Evite mensagens genéricas como:

```
update
ajustes
mudanças
```

*Prefira mensagens claras e descritivas.*

**Conventional Commits**

Um padrão muito utilizado em projetos profissionais é o [**Conventional Commits**](https://www.conventionalcommits.org/pt-br/v1.0.0/).

Formato:

```bash
<tipo>: descrição curta
```

Exemplos:

```
feat: adicionar função de busca de usuários
fix: corrigir bug na função de login
docs: atualizar README
```

Tipos comuns:

* `feat` → nova funcionalidade
* `fix` → correção de bug
* `docs` → documentação
* `refactor` → melhoria interna no código
* `test` → testes
* `style` → ajustes de formatação (espaços, quebras de linha etc.)

---


## 6. Visualizar o histórico do projeto

- Use os comandos abaixo para inspecionar o repositório:

    ```bash
    git status
    git log
    ```

---

## 7. Criar um repositório remoto

- Para compartilhar seu código, você pode utilizar uma plataforma de hospedagem Git, como:

    - GitHub
    - GitLab

- Acesse [github.com](https://github.com/) ou [gitlab.com](https://gitlab.com/) e registre-se para obter uma conta gratuita, que será usada para hospedar seus repositórios remotos.

> Após fazer sua conta, crie um novo repositório na plataforma escolhida.

---

## 8. Configurar autenticação com SSH

Para enviar código para plataformas como GitHub ou GitLab, é necessário configurar um método de autenticação.

Uma das formas mais utilizadas é a **autenticação via SSH**, que permite conectar seu computador ao repositório remoto de forma segura, sem precisar digitar usuário e senha a cada operação.

Consulte o guia oficial da plataforma que você estiver utilizando:

- 🔐 [Configurar SSH no GitHub](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh)
- 🔐 [Configurar SSH no GitLab](https://docs.gitlab.com/ee/user/ssh.html)

> Após configurar sua chave SSH, você poderá utilizar URLs do tipo:
>
> ```
> git@github.com:usuario/repositorio.git
> ```

## 9. Conectar o repositório local ao remoto

Após criar o repositório remoto, conecte-o ao repositório local:

```bash
git remote add origin <URL_DO_REPOSITORIO>
```

---

## 10. Enviar seu código para o repositório remoto

Envie seu primeiro commit:

```bash
git push -u origin main
```

> **📝Observação:** o parâmetro `-u` (abreviação de `--set-upstream`) define a branch remota `origin/main` como referência de rastreamento da sua branch local `main`. Após executar esse comando pela primeira vez, nos próximos envios você poderá utilizar apenas `git push` (e `git pull`), pois o Git já saberá para qual branch remota enviar ou buscar atualizações.

---

## 11. Atualizar seu repositório local

Para trazer mudanças do repositório remoto:

```bash
git pull
```

---

## 12. Clonar um repositório existente

Você também pode baixar um repositório existente utilizando:

```bash
git clone <URL_DO_REPOSITORIO>
```

Após clonar, faça uma alteração simples no `README.md`, crie um commit e envie a alteração.