# **Introdução ao uso pleno do `Git` pelo `Terminal do Ubuntu WSL`**

[![Ubuntu WSL](https://img.shields.io/badge/Ubuntu%20WSL-Download-orange?logo=ubuntu)](https://ubuntu.com/desktop/wsl)
[![Git](https://img.shields.io/badge/Git-Download-blue?logo=git)](https://git-scm.com/downloads)
[![gh](https://img.shields.io/badge/gh-Download-blue?logo=github)](https://cli.github.com)

## Criação de Repositório Inicial Padrão

### Observação: 

- Sempre que vir um bloco de código com `[]`, exemplo: `[nome-da-pasta]`, substitua pelo valor desejado, sem incluir os colchetes.  
Por exemplo: `[nome-da-pasta]` se tornaria `meu-repositorio`.

### Boas Práticas de Nomeação de Arquivos e Pastas:

- **Evite:** usar espaços, acentos ou caracteres especiais em nomes de arquivos e pastas, pois isso pode causar problemas de compatibilidade entre sistemas operacionais ou ferramentas.
    
- **Prefira:** utilizar letras minúsculas, separando palavras com hífens (`-`) ou underscores (`_`). Isso mantém os nomes legíveis e compatíveis com diferentes plataformas.

    **Exemplo de uma prática inadequada:**

    ```shell
    c/user/meu repositório/Relatório sobre a Cotação em R$.md
    ```

    - **Problemas:** contém espaços, acentuação e caracteres especiais (#), o que pode causar erros de acesso ou manipulação.

    **Exemplo de uma boa prática:**

    ```shell
    c/user/meu-repositorio/relatorio_sobre_a_cotacao_em_reais.md
    ```

    - **Vantagens:** usa hífens no lugar de espaços para pastas e usa underline para arquivos, sempre sem caracteres especiais ou acentuação. Tudo em minúsculas para maior compatibilidade e facilidade de uso.

### Passos:

1. **Criar nova pasta para o repositório:**

    ```shell
    sudo mkdir [nome-da-pasta]
    ```

2. **Entrar na pasta criada:**

    ```shell
    cd [nome-da-pasta]
    ```

3. **Inicializar o repositório local:**

    ```shell
    git init
    ```

4. **Renomear a branch local `master` para `main`:**

    ```shell
    git branch -m master main
    ```

5. **Criar o arquivo README:**

    ```shell
    sudo touch README.md
    ```

6. **Abrir o README com o editor de texto `vim`:**

    ```shell
    vim README.md
    ```

7. **Habilitar modo de inserção para editar o README:**

    - Ao abrir o `README.md`, a última linha mostrará algo como: `"README.md" 1L, 1B`  
    - Pressione a tecla `i` para entrar no modo INSERT. A última linha mudará para: `-- INSERT --`.

8. **Escrever texto inicial no README:**

    - Agora você pode escrever no seu README direto do terminal do Ubuntu podendo escrever algo por exemplo:

        ```markdown
        # Init repository
        ```
9. **Salvar e fechar o arquivo README:**

    - Após ter escrito o que desejou no modo de inserção para salvar o arquivo e fecha-lo:
        - Pressione a tecla `ESC`
        - Escreva `:wq` e pressione a tecla `ENTER`

10. **Verificar o status do repositório:**

    ```shell
    git status
    ```

    A saída esperada será:
    ```shell
    On branch main

    No commits yet

    Untracked files:
      (use "git add <file>..." to include in what will be committed)
            README.md

    nothing added to commit but untracked files present (use "git add" to track)
    ```
11. **Adicionar o README ao stage:**

    ```shell
    git add README.md
    ```

    A saída esperada será:
    ```shell
    On branch main

    No commits yet

    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
            new file:   README.md
    ```

12. **Realizar o primeiro commit com uma mensagem descritiva:**

    - Podemos utilizar algum padrão para os nossos commits, recomendação: [**Padrões de commits - @iuricode**](https://github.com/iuricode/padroes-de-commits)

    - Utilização:

        ```shell
        git commit -m ":emoji: tag: [descrição da ação do commit em inglês no infinitivo como se esse commit fosse fazer algo]"
        ```
    
    - Exemplo:

        ```shell
        git commit -m ":tada: init: start project"
        ```

    - Saída esperada:

        ```shell
        [main (root-commit) 353f129] :tada: init: start project
        1 file changed, 1 insertion(+)
        create mode 100644 README.md
        ```
13. **Verificar histórico de commits:**

    - Comando:

        ```shell
        git log
        ```

    - Saída esperada:

        ```shell
        commit 353f1298bd5577b52f2d3c941593a3c1c25f88ce (HEAD -> main)
        Author: scryng <scrynng@gmail.com>
        Date:   Wed Sep 18 16:45:25 2024 -0300

        :tada: init: start project
        ```

14. **Instalar o `gh` para poder criar repositório remoto direto do `Terminal do Ubuntu WSL`:**

    - [Github CLI (gh)](/docs/github_cli.md)

15. **Vincular repositório remoto do GitHub:**

    - Utilização:

        ```shell
        git remote add origin <url-do-seu-repositorio-no-github>
        ```

    - Exemplo:

        ```shell
        git remote add origin https://github.com/scryng/work-fastapi.git
        ```

16. **Subir os commits para o repositório remoto do GitHub:**

    ```shell
    git push -u origin main
    ```
