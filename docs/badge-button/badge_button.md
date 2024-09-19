# Como criar `"Botão Badge"` personalizado utilizando o [Shields.io](https://shields.io) ou `svg`

## Exemplo de Botão Badge:

- Ícone padrão:

    [![Git](https://img.shields.io/badge/Git-2.39.1-yellow?logo=git)](https://git-scm.com)

    [![GitHub CLI (gh)](https://img.shields.io/badge/GitHub%20CLI%20(gh)-2.57.0-yellow?logo=github)](https://github.com/cli/cli)

- Ícone personalizado:

    [![Pub/Sub](https://img.shields.io/badge/Pub%2FSub-1.7.0-blue.svg?logo=data:image/svg%2bxml;base64,PHN2ZyBoZWlnaHQ9IjI1MDAiIHZpZXdCb3g9Ii0xLjYzMzIzNTQzIDcuMDMyNjA5MzMgMTMxLjI2NTc0NjgyIDExNC40MzkzOTA2NyIgd2lkdGg9IjI1MDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPjxsaW5lYXJHcmFkaWVudCBpZD0iYSIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiIHgxPSI2NCIgeDI9IjY0IiB5MT0iNy4wMzQiIHkyPSIxMjAuNzg5Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM0Mzg3ZmQiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiM0NjgzZWEiLz48L2xpbmVhckdyYWRpZW50PjxwYXRoIGQ9Im0yNy43OSAxMTUuMjE3LTI2LjI1LTQ1LjQ2OGExMS40OTkgMTEuNDk5IDAgMCAxIDAtMTEuNDk5bDI2LjI1LTQ1LjQ2N2ExMS41IDExLjUgMCAwIDEgOS45Ni01Ljc1aDUyLjVhMTEuNSAxMS41IDAgMCAxIDkuOTU5IDUuNzVsMjYuMjUgNDUuNDY3YTExLjQ5OSAxMS40OTkgMCAwIDEgMCAxMS41bC0yNi4yNSA0NS40NjdhMTEuNSAxMS41IDAgMCAxIC05Ljk1OSA1Ljc0OWgtNTIuNWExMS40OTkgMTEuNDk5IDAgMCAxIC05Ljk2LTUuNzV6IiBmaWxsPSJ1cmwoI2EpIi8+PHBhdGggZD0ibTEyMS4wNTQgNzkuNTgtMzEuODM2LTMxLjgzNC01Ljg1OCAxLjIxNC0xNC42MDMtMTQuNjAyLTQuNjczIDguNzM5LTIuNTM0IDEwLjEwOSA0LjI4OSA0LjI5LTguMjM4IDEuNjgyLTExLjI5Ni0xMS4yOTYtNy42NyA3LjM3MyAxNC4xMjMgMTQuMTI1LTE0Ljk3IDExLjkgNDAuMTkzIDQwLjE5MiAxOS41ODEtLjE5eiIgb3BhY2l0eT0iLjA3Ii8+PGcgZmlsbD0iI2ZmZiI+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjQyLjQ4IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iODguODQ5IiByPSI1LjMyNSIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iNjQiIHI9IjguNjAyIi8+PGNpcmNsZSBjeD0iNDIuNDgiIGN5PSI3Ni40MjQiIHI9IjYuNzU4Ii8+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNzYuNDI0IiByPSI2Ljc1OCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iMzkuMTUxIiByPSI2Ljc1OSIvPjwvZz48L3N2Zz4=)](https://cloud.google.com/pubsub)

---

## Criar Botão Badge com Ícones padrão do Shields.io:

- Estrutura do markdown:

    ```markdown
    [![Texto](https://img.shields.io/badge/Texto-SubTexto-color?logo=logoexistente)](https://seulink.com)
    ```

- Exemplo:

    ```markdown
    [![GitHub](https://img.shields.io/badge/GitHub-3.14.0-blue?logo=github)](https://github.com)
    ```

- Resultado:

    [![GitHub](https://img.shields.io/badge/GitHub-3.14.0-blue?logo=github)](https://github.com)

---

## Criar Botão Badge com Ícones personalizados:

Para utilizar imagens personalizadas `svg`, a imagem precisa ser codificada em `Base64`

Para isso iremos utilizar o `Ubuntu WSL Terminal`

1. **Abra o a pasta onde está a sua imagem svg via `Ubuntu WSL Terminal`:**

    ```shell
    cd /mnt/c/pasta
    ```

2. **Codifique a imagem com o `Base64`:**

    ```shell
    base64 -w 0 logo.svg > logo_base64.txt
    ```

3. **Será retornado no um `Código` dentro do arquivo `logo_base64.txt`, copie-o. Exemplo utilizado:**

    `logo_base64.txt`:
    ```shell
    PHN2ZyBoZWlnaHQ9IjI1MDAiIHZpZXdCb3g9Ii0xLjYzMzIzNTQzIDcuMDMyNjA5MzMgMTMxLjI2NTc0NjgyIDExNC40MzkzOTA2NyIgd2lkdGg9IjI1MDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPjxsaW5lYXJHcmFkaWVudCBpZD0iYSIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiIHgxPSI2NCIgeDI9IjY0IiB5MT0iNy4wMzQiIHkyPSIxMjAuNzg5Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM0Mzg3ZmQiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiM0NjgzZWEiLz48L2xpbmVhckdyYWRpZW50PjxwYXRoIGQ9Im0yNy43OSAxMTUuMjE3LTI2LjI1LTQ1LjQ2OGExMS40OTkgMTEuNDk5IDAgMCAxIDAtMTEuNDk5bDI2LjI1LTQ1LjQ2N2ExMS41IDExLjUgMCAwIDEgOS45Ni01Ljc1aDUyLjVhMTEuNSAxMS41IDAgMCAxIDkuOTU5IDUuNzVsMjYuMjUgNDUuNDY3YTExLjQ5OSAxMS40OTkgMCAwIDEgMCAxMS41bC0yNi4yNSA0NS40NjdhMTEuNSAxMS41IDAgMCAxIC05Ljk1OSA1Ljc0OWgtNTIuNWExMS40OTkgMTEuNDk5IDAgMCAxIC05Ljk2LTUuNzV6IiBmaWxsPSJ1cmwoI2EpIi8+PHBhdGggZD0ibTEyMS4wNTQgNzkuNTgtMzEuODM2LTMxLjgzNC01Ljg1OCAxLjIxNC0xNC42MDMtMTQuNjAyLTQuNjczIDguNzM5LTIuNTM0IDEwLjEwOSA0LjI4OSA0LjI5LTguMjM4IDEuNjgyLTExLjI5Ni0xMS4yOTYtNy42NyA3LjM3MyAxNC4xMjMgMTQuMTI1LTE0Ljk3IDExLjkgNDAuMTkzIDQwLjE5MiAxOS41ODEtLjE5eiIgb3BhY2l0eT0iLjA3Ii8+PGcgZmlsbD0iI2ZmZiI+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjQyLjQ4IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iODguODQ5IiByPSI1LjMyNSIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iNjQiIHI9IjguNjAyIi8+PGNpcmNsZSBjeD0iNDIuNDgiIGN5PSI3Ni40MjQiIHI9IjYuNzU4Ii8+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNzYuNDI0IiByPSI2Ljc1OCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iMzkuMTUxIiByPSI2Ljc1OSIvPjwvZz48L3N2Zz4=
    ```

4. **Copie o conteúdo do bloco de código "Exemplo" e cole o código retornado pelo `Base64`, onde está escrito `[COLE-O-CODIGO-AQUI]`:**

    - Estrutura do markdown:

        ```markdown
        [![Texto](https://img.shields.io/badge/Texto-SubTexto-color.svg?logo=data:image/svg%2bxml;base64,[COLE-O-CODIGO-AQUI])](https://seulink.com)
        ```

    - Exemplo:

        ```markdown
        [![Pub/Sub](https://img.shields.io/badge/Pub%2FSub-1.7.0-blue.svg?logo=data:image/svg%2bxml;base64,PHN2ZyBoZWlnaHQ9IjI1MDAiIHZpZXdCb3g9Ii0xLjYzMzIzNTQzIDcuMDMyNjA5MzMgMTMxLjI2NTc0NjgyIDExNC40MzkzOTA2NyIgd2lkdGg9IjI1MDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPjxsaW5lYXJHcmFkaWVudCBpZD0iYSIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiIHgxPSI2NCIgeDI9IjY0IiB5MT0iNy4wMzQiIHkyPSIxMjAuNzg5Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM0Mzg3ZmQiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiM0NjgzZWEiLz48L2xpbmVhckdyYWRpZW50PjxwYXRoIGQ9Im0yNy43OSAxMTUuMjE3LTI2LjI1LTQ1LjQ2OGExMS40OTkgMTEuNDk5IDAgMCAxIDAtMTEuNDk5bDI2LjI1LTQ1LjQ2N2ExMS41IDExLjUgMCAwIDEgOS45Ni01Ljc1aDUyLjVhMTEuNSAxMS41IDAgMCAxIDkuOTU5IDUuNzVsMjYuMjUgNDUuNDY3YTExLjQ5OSAxMS40OTkgMCAwIDEgMCAxMS41bC0yNi4yNSA0NS40NjdhMTEuNSAxMS41IDAgMCAxIC05Ljk1OSA1Ljc0OWgtNTIuNWExMS40OTkgMTEuNDk5IDAgMCAxIC05Ljk2LTUuNzV6IiBmaWxsPSJ1cmwoI2EpIi8+PHBhdGggZD0ibTEyMS4wNTQgNzkuNTgtMzEuODM2LTMxLjgzNC01Ljg1OCAxLjIxNC0xNC42MDMtMTQuNjAyLTQuNjczIDguNzM5LTIuNTM0IDEwLjEwOSA0LjI4OSA0LjI5LTguMjM4IDEuNjgyLTExLjI5Ni0xMS4yOTYtNy42NyA3LjM3MyAxNC4xMjMgMTQuMTI1LTE0Ljk3IDExLjkgNDAuMTkzIDQwLjE5MiAxOS41ODEtLjE5eiIgb3BhY2l0eT0iLjA3Ii8+PGcgZmlsbD0iI2ZmZiI+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjQyLjQ4IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iODguODQ5IiByPSI1LjMyNSIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iNjQiIHI9IjguNjAyIi8+PGNpcmNsZSBjeD0iNDIuNDgiIGN5PSI3Ni40MjQiIHI9IjYuNzU4Ii8+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNzYuNDI0IiByPSI2Ljc1OCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iMzkuMTUxIiByPSI2Ljc1OSIvPjwvZz48L3N2Zz4=)](https://cloud.google.com/pubsub)
        ```

    - Resultado:

        [![Pub/Sub](https://img.shields.io/badge/Pub%2FSub-1.7.0-blue.svg?logo=data:image/svg%2bxml;base64,PHN2ZyBoZWlnaHQ9IjI1MDAiIHZpZXdCb3g9Ii0xLjYzMzIzNTQzIDcuMDMyNjA5MzMgMTMxLjI2NTc0NjgyIDExNC40MzkzOTA2NyIgd2lkdGg9IjI1MDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPjxsaW5lYXJHcmFkaWVudCBpZD0iYSIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiIHgxPSI2NCIgeDI9IjY0IiB5MT0iNy4wMzQiIHkyPSIxMjAuNzg5Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM0Mzg3ZmQiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiM0NjgzZWEiLz48L2xpbmVhckdyYWRpZW50PjxwYXRoIGQ9Im0yNy43OSAxMTUuMjE3LTI2LjI1LTQ1LjQ2OGExMS40OTkgMTEuNDk5IDAgMCAxIDAtMTEuNDk5bDI2LjI1LTQ1LjQ2N2ExMS41IDExLjUgMCAwIDEgOS45Ni01Ljc1aDUyLjVhMTEuNSAxMS41IDAgMCAxIDkuOTU5IDUuNzVsMjYuMjUgNDUuNDY3YTExLjQ5OSAxMS40OTkgMCAwIDEgMCAxMS41bC0yNi4yNSA0NS40NjdhMTEuNSAxMS41IDAgMCAxIC05Ljk1OSA1Ljc0OWgtNTIuNWExMS40OTkgMTEuNDk5IDAgMCAxIC05Ljk2LTUuNzV6IiBmaWxsPSJ1cmwoI2EpIi8+PHBhdGggZD0ibTEyMS4wNTQgNzkuNTgtMzEuODM2LTMxLjgzNC01Ljg1OCAxLjIxNC0xNC42MDMtMTQuNjAyLTQuNjczIDguNzM5LTIuNTM0IDEwLjEwOSA0LjI4OSA0LjI5LTguMjM4IDEuNjgyLTExLjI5Ni0xMS4yOTYtNy42NyA3LjM3MyAxNC4xMjMgMTQuMTI1LTE0Ljk3IDExLjkgNDAuMTkzIDQwLjE5MiAxOS41ODEtLjE5eiIgb3BhY2l0eT0iLjA3Ii8+PGcgZmlsbD0iI2ZmZiI+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjQyLjQ4IiBjeT0iNTEuNTc2IiByPSI1LjMyNCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iODguODQ5IiByPSI1LjMyNSIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iNjQiIHI9IjguNjAyIi8+PGNpcmNsZSBjeD0iNDIuNDgiIGN5PSI3Ni40MjQiIHI9IjYuNzU4Ii8+PGNpcmNsZSBjeD0iODUuNTE5IiBjeT0iNzYuNDI0IiByPSI2Ljc1OCIvPjxjaXJjbGUgY3g9IjY0IiBjeT0iMzkuMTUxIiByPSI2Ljc1OSIvPjwvZz48L3N2Zz4=)](https://cloud.google.com/pubsub)