# 🤝 Colaboração com GitLab

Neste submódulo você aprenderá como colaborar utilizando o **GitLab**, plataforma que integra hospedagem de código, CI/CD, gerenciamento de tarefas e revisão de código.

No GitLab, o principal mecanismo de colaboração é o **Merge Request (MR)**.

---

## Tópicos abordados

- Fluxo GitLab Flow: uso de branches e Merge Requests (MRs)
- Criando e revisando Merge Requests
- Gerenciamento de issues e boards para organização
- Revisão de código e comentários inline
- Resolução de conflitos e rebase no GitLab
- ~~Pipelines básicos de CI/CD no GitLab~~ <!-- [WIP] Work in Progress -->

---

## Fluxo básico: GitLab Flow

O GitLab Flow combina o uso de branches, merge requests e integração contínua. Fluxo típico:

1. Criar uma branch para uma nova feature ou correção.
2. Enviar a branch para o repositório remoto.
3. Abrir um Merge Request para revisão e integração.
4. Utilize pipelines de CI/CD para validar o código automaticamente.
5. Realizar o merge após aprovação.

---

## Exemplo prático: Criando um Merge Request

```bash
git checkout -b feature/minha-feature
# faça suas alterações
git add .
git commit -m "feat: adiciona funcionalidade Y"
git push origin feature/minha-feature
```

Depois, abra um **Merge Request** na interface do **GitLab**.

---

## Boas práticas para Merge Requests

* Preencha título e descrição detalhados.
* Vincule issues relacionadas.
* Use labels para organizar.
* Comente diretamente no código para facilitar a comunicação.
* Aguarde a aprovação e execute o merge.

---

## Exercício prático

1. Crie uma `branch` nova e altere um arquivo (Ex.: `README.md`).
2. Faça commit com mensagem clara.
3. Suba a `branch` para o **GitLab**.
4. Abra um Merge Request.
5. Faça comentários simulando revisão.
6. Finalize o `merge` após revisão.

---

## Dicas para colaborar no GitLab

- Utilize templates de Merge Request para melhorar a padronização
- Comente de forma clara nas revisões para facilitar a comunicação
- Use labels, milestones e boards para acompanhar o progresso
- Aproveite a integração nativa do CI/CD para validar código automaticamente

---

## Recursos úteis

- [GitLab Docs - Merge Requests](https://docs.gitlab.com/ee/user/project/merge_requests/)
- [GitLab CI/CD Documentation](https://docs.gitlab.com/ee/ci/)
- [GitLab Flow Guide](https://docs.gitlab.com/ee/topics/gitlab_flow.html)
