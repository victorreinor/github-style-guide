# Guia de estilo git/github
Guia de estilo para git/github

1. [Branchs](#branchs "Branchs")
2. [Commit](#commit "Commit")

# Branchs
- Escolha nomes *curtos* e *descritivos* para os branchs e cada um deverá começar com **feature/** ou **hotfix/**
- Use traços para separar palavras.

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
Correções que precisam ser aplicadas com urgência também devem ser criadas em um branch próprio a partir do master, entretanto será possível incorporar as modificações em quaisquer branchs que forem necessários.

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

**Mensagens**
- Use o editor, não o terminal, quando estiver escrevendo a mensagem do commit:
	Committar do terminal encoraja uma ideia de ter que encaixar tudo em uma única linha, o que geralmente resulta em commits não informativos, mensagens ambíguas.

- O sumário (ie. a primeira linha da mensagem) deve ser descritivo ainda que sucinto. O ideal é que não seja maior que 50 caracteres. Deve ser escrito com letra maiúscula e no modo imperativo. Não deve terminar com um ponto, uma vez que é efetivamente o título do title: "Corrige" e não "corrigiu", "corrigindo" ou “correção”;

- Quando estiver escrevendo uma mensagem do commit, pense sobre o que você precisaria saber olhando para o commit daqui um ano.

# Organização de Projeto
1. Crie um **Project** no repositório no formato de kanban-automation
2. Crie isssues para cada necessidade do software;
	Cada issue aberta deverá ser vinculado ao **Project** criado e conter uma lista de checkbox com tudo que será necessario para desenvolver aquele módulo. **Segue abaixo o exemplo**
	
	![Exemplo Issue](https://raw.githubusercontent.com/victorreinor/github-style-guide/master/images/Issue%20de%20teste.PNG "Exemplo Issue")
	Conforme desenvolvido cada checkbox deverá ser marcado pois teremos uma barra de progresso que poderemos ver que estamos evoluindo perante aquela issue. 
	
	Na tela de projeto teremos o controle de como as coisas estão. Tudo que está listado (issues abertas vinculadas ao projeto), o andamento de cada uma issue e o que já foi finalizado
	![Tela de project](https://raw.githubusercontent.com/victorreinor/github-style-guide/master/images/Tela%20de%20project.PNG "Tela de project")
	
	O intuito desta organização e fazer as pessoas pensar no projeto antes de começar ou seja, listar tudo que precisa desde conversa com cliente até deploy do software, sendo assim teremos tudo que precisamos saber antes de começar desenvolver o software e quebrado em pequenas partes, assim facilitando o desenvolvimento. 
	Cada vez que tickamos o checkbox diminuimos um na nossa lista e podemos ver este progresso nas propria issues ou na aba de **Projects**(que dá uma visão geral), isso faz com que nosso cerebro libere doses de **dopamina** e sinta aquele sensação de prazer e recompensa por estar vendo o seu progresso.

###### [Fonte de ajuda 1](https://github.com/Openredu/Openredu/wiki/Guia-de-boas-práticas-de-desenvolvimento "Fonte de ajuda 1")
###### [Fonte de ajuda 2](https://github.com/guylhermetabosa/git-style-guide/blob/master/README.md "Fonte de ajuda 2")
