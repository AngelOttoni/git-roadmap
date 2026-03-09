# 🤝 Como Contribuir

Obrigada por querer ajudar a melhorar este roadmap! 💜

> **As contribuições podem ser feitas utilizando GitHub ou GitLab, dependendo do ambiente em que você está utilizando o roadmap.**

## 🛠 **Passo a Passo**

### **1. Faça um fork do repositório**   
    → [GitHub](https://github.com/AngelOttoni/git-roadmap)   
    → [GitLab](https://gitlab.ppgmcs.com.br/lica-resources/best-practices/team/onboarding/git-workflow-roadmap.git)

**1.1 Depois clone o seu fork:**

    
    git clone <url-do-seu-fork>


**1.2 Entre na pasta do projeto:**

    
    cd git-workflow-roadmap
    

### **2. Crie uma branch para suas alterações:**

   ```bash
   git checkout -b minha-sugestao
   ```

- *Use nomes descritivos para a branch, por exemplo:*

        fix/erro-no-readme
        docs/novo-material
        feat/exercicio-adicional

### **3. Faça suas alterações**
- *Alguns exemplos de contribuições:* 

    - corrigir erros de documentação    
    - adicionar novos materiais ou links úteis  
    - melhorar explicações dos módulos  
    - sugerir novos exercícios  

### **4. Faça o commit**
- Utilize boas práticas de commit seguindo o padrão ([Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)):
    ```bash
    git commit -m "docs: melhora explicação sobre branching"
    ```

### **5. Envie suas alterações para o seu fork:**

   ```bash
   git push origin minha-sugestao
   ```
### **6. Abra uma contribuição 🚀**
> **Dependendo da plataforma utilizada:**

| Plataforma | Ação                           |
| ---------- | ------------------------------ |
| GitHub     | Abra um **Pull Request (PR)**  |
| GitLab     | Abra um **Merge Request (MR)** |

- Explique brevemente:

    - o que foi alterado
    - por que a alteração é útil
    - qual módulo foi afetado

## 🏷️ Labels usadas nas Issues

*As issues deste repositório utilizam algumas labels para facilitar a organização:*

- `iniciante` – tarefas para quem está começando
- `intermediário` – tarefas para quem já sabe o básico
- `avançado` – desafios mais complexos
- `docs` – melhorias na documentação
- `good first issue` – boas primeiras contribuições
- `projeto-final` – relacionado à entrega do projeto final

---
---

# 📦 Contribuições de Projetos Finais

Se você está entregando o projeto final do roadmap, siga os passos abaixo:

1. Faça um fork deste repositório   
    → [GitHub](https://github.com/AngelOttoni/git-roadmap)   
    → [GitLab](https://gitlab.ppgmcs.com.br/lica-resources/best-practices/team/onboarding/git-workflow-roadmap.git)
2. Clone o fork na sua máquina:

    ```bash
    git clone <url-do-seu-fork>
    ```

3. Crie uma nova branch para suas modificações *(substitua minha-entrega por um nome relevante)*:

    ```bash
    git checkout -b minha-entrega
    ```
4. Crie um arquivo `.md` com o nome da dupla na pasta `modules/05-project/submissions/`:    
    Exemplo:
    ```bash
    modules/05-project/submissions/nome1-e-nome2.md
    ```
5. Preencha o template
- Utilize o modelo disponível em: [`modules/05-project/templates/TEMPLATE_ENTREGA.md`](./modules/05-project/templates/TEMPLATE_ENTREGA.md).

6. Faça o commit com uma mensagem semântica:

    ```bash
    git add modules/05-project/submissions/nome-da-dupla.md
    git commit -m "feat(submission): adiciona entrega final da dupla Nome1 & Nome2"
    ```

7. Envie (push) a branch para seu fork:

    ```bash
    git push origin minha-entrega
    ```
8. Abra sua contribuição para o repositório original, selecionando sua branch recém enviada
    - **GitHub:** abra um **Pull Request**
    - **GitLab:** abra um **Merge Request**
9. Aguarde a revisão e sua entrada no Hall da Fama 🎉
