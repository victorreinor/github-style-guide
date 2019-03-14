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

Cada commit deve ser uma mudança lógica simples. Não faça várias mudanças lógicas em um commit. Por exemplo, se uma alteração corrige um bug e otimiza a performance de uma funcionalidade, o divida em dois commits separados.

Não divida uma mudança lógica simples em vários commits. Por exemplo, a implementação de uma funcionalidade e os testes correspondentes à ela devem estar no mesmo commit.

Commit cedo e frequentemente. Commits pequenos e autônomos são mais fáceis de entender e reverter quando algo dá errado.

Commits devem ser ordenados logicamente. Por exemplo, se commit X depende de uma mudança feita no commit Y, então commit Y deve vir antes do commit X.

[Commits Atomicos](https://en.wikipedia.org/wiki/Atomic_commit#Atomic_commit_convention "Commits Atomicos")

**Titulo**
- Deve conter a descrição sucinta da alteração:
- No maximo 50 caracteres;
- Use sempre o imperativo: "Corrige" e não "corrigiu", "corrigindo" ou “correção”;
- Inicie a frase com letra maiúscula;
- Sem ponto (.) No final.
