# Como trabalhar em equipe com Git

O Git permite que você versione seu código, de forma com que você crie uma versão local com Git e uma outra versão na nuvem no Github

Quando estamos trabalhando em equipe, cada pessoa da equipe costuma ter seu próprio computador. 

Como fazemos para manter a mesma versão de código entre as pessoas da equipe?

Utilizando o Github.

Quando temos muitas pessoas na equipe, é normal criarmos um repositório na nuvem (Github) para criar uma versão única do seu projeto.

# Conceito de branch

Eu gosto de fazer uma analogia de que uma branch nada mais é do que uma area de trabalho, quando você está em um projeto, você pode criar várias branches.

Cada branch, possui uma versão do código com diferentes funcionalidades.

Branch é essencial quando você está trabalhando em equipe. 

Existe algumas abordagens ao trabalhar com branches "Feature flag" e "Trunk Based", neste momento, vou dar apenas o exemplo de Feature Flag.

Isso significa que toda funcionalidade nova que você for adicionar no seu projeto, você pode criar uma branch para essa funcionalidade e adicionar para a branch principal depois.

Todo projeto possui uma branch principal, essa branch contém a **última versão do projeto** (ao menos deveria), normalmente essa branch se chama **main ou master**

### Comandos para trabalhar com Branch

```sh
# Criar uma Nova Branch
git branch feature/nova-funcionalidade

# Mudar para uma Branch Existente
git checkout feature/nova-funcionalidade
# Poderia ser 
git checkout main

# Adicionando as alteracões de uma branch para outra
# Vamos supor que você codou algumas coisas na branch "feature/nova-funcionalidade" e quer adicionar elas para a branch principal
# Primeiro, mude para a branch principal
git checkout main
# Em seguinda, execute o comando "merge" para juntar essas alteracões
git merge feature/nova-funcionalidade

# Deletar uma branch
git branch -d feature/nova-funcionalidade
```


# Conceito de Clone

Quando você está trabalhando em um projeto de uma organizacão (empresa), provavelmente as pessoas vão te adicionar no repositório da empresa
com as permissões de escrita e leitura no repositório, dessa forma você consegue trabalhar normalmente.

Mas como eu faco para pegar uma cópia desse projeto da minha empresa para minha máquina?

Utilizando o git clone.

Essa funcionalidade permite que você crie uma cópia do projeto na sua máquina local, quando você executa um git clone, você baixa todas as branches, commits e histórico de alteracões daquele repositório.

Isso é muito importante quando vamos trabalhar em equipe, especialmente quando você se encontra com alguns problemas em producão e precisa "voltar" uma versão da sua aplicacão porque a nova estava com problema.

### Como clonar um repositório

```sh
git clone <link-do-repositorio>

# Exemplo real
git clone https://github.com/Early-Career-Automation-Community/learning-git.git

# Clonando via ssh
git clone git@github.com:Early-Career-Automation-Community/learning-git.git
```

# Conceito de Fork

Eu expliquei para vocês que quando você trabalha em uma empresa, normalmente o time te adiciona no repositório com as permissões de escrita e leitura.
Mas vamos supor que você queira contribuir para o Open Source (projetos abertos ao público). Neste caso, você não foi adicionado no projeto e não tem nenhuma permissão.

Nessa situacão, nós utilizamos o comando git fork para criar uma versão do projeto dentro do seu Github, ou seja, essa versão se torna sua e você tem total liberdade de fazer o que quiser.

Mas essa versão só existe na nuvem, ela não está disponível na sua máquina local. 
Por isso que após "forkar" um projeto, você deve clonar esse projeto para sua máquina local para conseguir adicionar suas mudancas no projeto.

Depois de ter feito esse fluxo, você tem uma versão só sua do projeto.

Mas como eu faco para adicionar minhas mudancas no projeto original?

É necessário abrir uma Pull Request (solicitacão de mudanca) para os donos do projeto.

Eles vão analisar suas alteracões e avaliar se deve adicionar ou não.

# Conceito de Issue

Todo repositório Open Source possui área só para registrar **bugs e sugestões de melhorias**, costumamos chamar essa área de Issue.

Então, todos os problemas ficam registrados nessa área onde você consegue visualizar os "tickets" que as pessoas abrem.

É possível linkar esseas issues com suas mudancas. Por exemplo, você encontrou um bug em um projeto Open Source e decide resolver isso.

Você abre uma issue no repositório, faz um fork do projeto e clona para sua máquina local.

Após isso, você cria uma branch para a sua alteracão e comeca a trabalhar nesse problema.

Em seguida, faz um push das suas alteracões para a branch que você criou.

Agora é o momento de abrir um Pull Request no repositório Original e linkar suas mudancas com o ID da Issue.

# Conceito de Pull Request

Nada mais é do que uma solicitacão de alteracão, em projetos grandes, costumamos abrir uma PR (Pull Request) para adicionar algo ao código do projeto.

Este momento de PR costuma ser avaliado pelos donos do repositório que verificam o seu código, podendo aprovar ou não essa sua requisicão de mudanca.
