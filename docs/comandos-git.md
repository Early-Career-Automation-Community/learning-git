# Comandos do git

O git possui diversos comandos para diversas funcionalidades, mas inicialmente, nós vamos cobrir só algumas funcionalidades.

# Comandos e suas funcionalidades

```shell
# Utilizado para inicializar o seu repositório
git init

# Utilizado para adicionar suas mudancas
git add

# Utilizado para salvar suas mudancas
git commit

# Utilizado para exibir o histórico de commits
git log

# Utilizado para verificar as mudancas feitas nos arquivos/diretório do projeto
git status

# Utilizado para se conectar a um repositório na nuvem
git remote add origin https://github.com/seuusuario/meu_projeto.git

# Utilizado para enviar seus commits locais para a nuvem
git push
```

# Criando um repositório Local

```shell
# Criando uma pasta chamada de ecac-git
mkdir ecac-git

# Entrando dentro da pasta
cd ecac-git

# Verificando o caminho da sua pasta
pwd

# Inicializando seu repositório Local
git init
```

# Criando um arquivo no seu repositório Local

```shell
echo "# Olá mundo" > README.md
```

# Adicionando o arquivo ao repositório

```shell
git add README.md
```

# Salvando o arquivo no repositório local

```shell
# -m adiciona uma mensagem ao seu commit
git commit -m "Meu primeiro commit no ECAC"
```

# TO-DO: Criar um repositório na nuvem e subir o seu arquivo para o GitHub




