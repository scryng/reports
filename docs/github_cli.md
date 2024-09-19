# **Instalar o `GitHub CLI (gh)` via `Terminal do Ubuntu WSL`**

[![gh](https://img.shields.io/badge/gh-Download-blue?logo=github)](https://cli.github.com)

## Referência: ["Installing gh on Linux and BSD"](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)

### Instalação:

```shell
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
&& sudo mkdir -p -m 755 /etc/apt/keyrings \
&& wget -qO- https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```

### Atualização:

```shell
sudo apt update
sudo apt install gh
```
### Autenticar o GitHub CLI com a sua conta do GitHub:

```shell
gh auth login
```

### Criar repositório vázio:

```shell
gh repo create
```

> ? What would you like to do?  
> Create a new repository on GitHub from scratch  
> 
> ? Repository name  
> meu-repositorio
> 
> ? Repository owner  
> scryng
> 
> ? Description  
> descrição do repositório
> 
> ? Visibility  
> Public
> 
> ? Would you like to add a README file?  
> No
> 
> ? Would you like to add a .gitignore?  
> No
> 
> ? Would you like to add a license?  
> No
> 
> ? This will create "meu-repositorio" as a public repository on GitHub. Continue?  
> Y
> 