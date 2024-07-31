# Como usar o Git

Este repositório contém um tutorial para dar os primeiros passos o git.

# O que é Git?

É uma ferramenta de gerenciamento e controle de versão de código.


# Requisitos para usar Git?

Ter um computador.

# Quando devemos usar Git?

Utilizamos o git para gerenciar as versões do nosso código, por exemplo, vamos supor que nós temos um arquivo chamado de **teste.py**

```teste.py
hello = 'Hello'
world = 'World'
```

Inicialmente, este arquivo possui 2 variaveis declaradas, vamos supor que essa seja a primeira versão do nosso arquivo. 
Mas e se eu quiser criar uma nova versão desse arquivo?

```teste.py
hello = 'Hello'
world = 'World'

resultado = hello + '' + world
```

No exemplo acima, criei uma nova versão do arquivo teste.py com um "conteúdo novo"

### Versão 1

```teste.py
hello = 'Hello'
world = 'World'
```

### Versão 2

```teste.py
hello = 'Hello'
world = 'World'

resultado = hello + '' + world
```

Logo, o arquivo **teste.py** tem 2 versões. Mas como eu controlo as versões desse código?

O git existe justamente para isso, para "monitorar" cada mudanca que você realizar no seu projeto.


Git é essencial para trabalhar com projetos grandes ou até mesmo projetos pessoais, versionamento de código te ajuda a ter controle do que está sendo criado no seu projeto.

# Lista de Conteúdo

- 1 - [Como baixar o git no Linux](./docs/como-baixar-git.md)

- 2 - [Como configurar o git](./docs/configurando-git.md)

- 3 - [Comandos do Git](./docs/comandos-git.md)
