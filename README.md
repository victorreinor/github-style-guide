# Guia de estilo git/github
Guia de estilo para git/github

1. [Branches](#branches "Branches")
2. [Commit](#commit "Commit")

# Branches
Escolha nomes *curtos* e *descritivos* para os brachs e cada um deverá começar com **feature/** ou **hotfix/**

## Master
Branch master é o default para desenvolvimento, sendo assim durante o ciclo de desenvolvimento de novas releases toda alteração deve partir(checkout) e retornar(merge) deste branch. Tornando este um branch atualizado.

## Features
Toda funcionalidade deve ser implementada em um branch próprio, ramificado a partir do master e integrado de volta quando concluída a funcionalidade. Uma vez que o pull request for aceito o branch será apagado.

**Exemplo**
  ```shell
  # bom
  $ git checkout -b feature/crud-cliente

  # ruim
  $ git checkout -b feature/cliente
  ```
  
## Hotfix
Correções que precisam ser aplicadas com urgência também devem ser criadas em um branch próprio a partir do master, entretanto será possível incorporar as modificações em quaisquer branches que forem necessários.

**Exemplo**
  ```shell
  # bom
  $ git checkout -b hotfix/inserir-pedido

  # ruim
  $ git checkout -b hotfix/erro-pedido
  ```
  
# Commit
Se duas correções distintas são realizadas, elas devem ser implementadas em dois commits diferentes. As mensagens de correção de issue devem descrever o que mudou e fazer referência ao número da issue associada à mudança. [Saiba mais sobre este tipo de commit](https://en.wikipedia.org/wiki/Atomic_commit#Atomic_commit_convention "Saiba mais sobre este tipo de commit")

**Titulo**
- Deve conter a descrição sucinta da alteração:
- No maximo 50 caracteres;
- Use sempre o imperativo: "Corrige" e não "corrigiu", "corrigindo" ou “correção”;
- Inicie a frase com letra maiúscula;
- Sem ponto (.) No final.
