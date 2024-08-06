# Como configurar o git no seu computador

# Definindo o nome do usuário

```shell
git config --global user.name "Seu Nome"
```

# Definindo o email do usuário

```shell
git config --global user.email "seuemail@example.com"
```

# Verificando sua configuracão

```shell
git config --global --list
```

# Configurando um chave ssh para se conectar com o Github

```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

# Adicionando sua chave pública no Github

```shell
# Você deve encontrar um arquivo chamado de id_ed25519.pub na pasta ~/.ssh/
# Excute o comando abaixo para validar se este arquivo foi criado.

ls ~/.ssh/

# Se o arquivo existir, você deve visualizar o conteúdo dele e copiar.
cat id_ed25519.pub

# Copie este conteúdo e cole em seu github, clique em Profile -> Settings -> SSH and GPG keys -> New ssh key
# Cole o conteúdo do arquivo e salve.

```

# Validando se é possível se conectar ao github.

```shell
# Adicione a sua chave ssh ao gerenciador de chaves ssh
eval "$(ssh-agent -s)"
# > Agent pid 59566

# Adicionando a chave ssh ao gerenciador
ssh-add ~/.ssh/id_ed25519

# Execute o comando abaixo para validar a conexão.
ssh -T git@github.com

```


