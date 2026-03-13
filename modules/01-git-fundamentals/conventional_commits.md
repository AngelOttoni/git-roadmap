## 📝 Boas práticas para escrever commits

Commits representam **unidades de mudança no projeto**.

Cada commit deve representar **uma alteração lógica e coesa**.

Evite mensagens genéricas como:

```
update
ajustes
mudanças
```

*Prefira mensagens claras e descritivas.*

## **Conventional Commits**

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
