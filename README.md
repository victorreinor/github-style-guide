# Guia de estilo git/github
Se você se sentir confortável para contribuir, por favor, o faça! Dê um fork no projeto e abra um pull request.

# Tabela de conteúdo
1. [Branch](#branch "Branch")
2. Em desenvolvimento
3. Em desenvolvimento
3. Em desenvolvimento
3. Em desenvolvimento

## Branch
Escolha nomes *curtos* e *descritivos* para os brachs e cada um deverá começar com **feature/** ou **hotfix/**

### Master
Branch master é o default para desenvolvimento, sendo assim durante o ciclo de desenvolvimento de novas releases toda alteração deve partir(checkout) e retornar(merge) deste branch. Tornando este um branch atualizado.

### Features
Toda funcionalidade deve ser implementada em um branch próprio, ramificado a partir do master e integrado de volta quando concluída a funcionalidade. Uma vez que o pull request for aceito o branch será apagado.

**Exemplo**
  ```shell
  # bom
  $ git checkout -b feature/crud-cliente

  # ruim
  $ git checkout -b feature/cliente
  ```
  
### Hotfix
Correções que precisam ser aplicadas com urgência também devem ser criadas em um branch próprio a partir do master, entretanto será possível incorporar as modificações em quaisquer branches que forem necessários.

**Exemplo**
  ```shell
  # bom
  $ git checkout -b hotfix/inserir-pedido

  # ruim
  $ git checkout -b hotfix/erro-pedido
  ```
