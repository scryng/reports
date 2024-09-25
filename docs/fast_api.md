# **Introdução a projetos `Python` com `FastAPI` via `Terminal do Ubuntu WSL`:**

[![Fast API](https://img.shields.io/badge/Fast%20API-Version-009688?logo=fastapi)](https://fastapi.tiangolo.com)
[![Pyenv](https://img.shields.io/badge/Pyenv-2.4.13-blue.svg?logo=data:image/svg%2bxml;base64,PHN2ZyB3aWR0aD0iNDUzIiBoZWlnaHQ9IjQ1MyIgdmlld0JveD0iMCAwIDQ1MyA0NTMiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF83NV8zMCkiPgo8cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTExNy4wMzYgNTAuMTc3NEMxMTcuMDM2IDUwLjE3NzQgMTA5Ljc3MiAwLjE5NTM2NyAyMjQuNjM5IDAuMTk1MzY3TDIyNS4yMzggMEMzNDUuMTg2IDAgMzM1LjkzMiA2MC40MzQzIDMzNS45MzIgNjAuNDM0M1YxNTkuNjAxQzMzNS45MzIgMTc3Ljk4NyAzMzAuMjgzIDE5MC42OSAzMjIuNDIyIDE5OS40NjVDMzE4LjQ2OCAyMDAuMDM5IDMxNC45NzIgMjAxLjMyNiAzMTEuOTM3IDIwMy4zMjVDMzA4LjIyMiAyMDUuNzM5IDMwNS40MzggMjA4LjkwOSAzMDMuNTg1IDIxMi44MzVDMzAzLjAxMiAyMTMuMDg4IDMwMi40NCAyMTMuMzMgMzAxLjg2OSAyMTMuNTYzVjIwMC4xODJIMjgwLjI0M1YyMTguNzc4QzI3Ni45MzEgMjE5LjA5IDI3NC45MDYgMjE5LjA1OCAyNzQuOTA2IDIxOS4wNThIMjYxLjA2OEMyNTkuMjgyIDIxNS4zMjIgMjU3LjAyNiAyMTIuMTIgMjU0LjMwMiAyMDkuNDVDMjUwLjgyMiAyMDYuMDA2IDI0Ni43MzggMjAzLjQzMSAyNDIuMDUgMjAxLjcyN0MyMzcuMzk4IDE5OS45ODcgMjMyLjM3NCAxOTkuMTE2IDIyNi45NzYgMTk5LjExNkMyMTguOTUgMTk5LjExNiAyMTEuOTU1IDIwMC44OTIgMjA1Ljk4OSAyMDQuNDQzQzIwMC4xMzUgMjA3Ljk0OCAxOTUuNTc5IDIxMi44MiAxOTIuMzIgMjE5LjA1OEgxNzQuOTk4TDE4MS42MTkgMjAwLjE4MkgxNTcuNTk2TDE1MS45MjUgMjIwLjEwOEMxNDMuMzkyIDIyMS41MDQgMTM2LjMyOCAyMjQuMjE0IDEzMC40OCAyMjcuNzYxTDEyMi43MDYgMjAwLjE4Mkg5OC44NDJMMTE0LjAxMSAyNDMuNjc4QzEwMS42OTYgMjYyLjE5NiAxMDIuNDEgMjg0LjM5MyAxMDIuNDEgMjg0LjM5M1YzMzkuMTEySDY0LjkyNDZDNjQuOTI0NiAzMzkuMTEyIDM4LjkxNDUgMzQxLjAyMyAxOS44MjAzIDMxMi42ODJIMzUuNzQ3MlYyNjguODk2SDM2LjQzOTZDMzcuNDY5NSAyNzEuMTY5IDM4Ljk2MDkgMjczLjQyNCA0MC45MTQxIDI3NS42NjFDNDIuODY3MiAyNzcuODYzIDQ1LjM3MDcgMjc5LjY5MiA0OC40MjQ3IDI4MS4xNDhDNTEuNTE0MiAyODIuNjA0IDU1LjI2MDcgMjgzLjMzMiA1OS42NjQxIDI4My4zMzJDNjUuODc4NiAyODMuMzMyIDcxLjQ4OTMgMjgxLjczNCA3Ni40OTY1IDI3OC41MzhDODEuNTM5MSAyNzUuMzA2IDg1LjUxNjMgMjcwLjU2NSA4OC40MjgzIDI2NC4zMTVDOTEuMzc1NyAyNTguMDMgOTIuODQ5NCAyNTAuMzI0IDkyLjg0OTQgMjQxLjE5N0M5Mi44NDk0IDIzMS44MjIgOTEuMzQwMiAyMjQuMDI4IDg4LjMyMTcgMjE3LjgxM0M4NS4zMDMzIDIxMS41NjMgODEuMjcyNyAyMDYuODkzIDc2LjIzMDEgMjAzLjgwNEM3MS4xODc1IDIwMC42NzkgNjUuNjgzMiAxOTkuMTE2IDU5LjcxNzMgMTk5LjExNkM1NS4xMzY0IDE5OS4xMTYgNTEuMzAxMSAxOTkuODk4IDQ4LjIxMTYgMjAxLjQ2QzQ1LjE1NzcgMjAyLjk4NyA0Mi42NzE5IDIwNC45MDUgNDAuNzU0MyAyMDcuMjEzQzM4Ljg3MjIgMjA5LjQ4NiAzNy40MzM5IDIxMS43MjMgMzYuNDM5NiAyMTMuOTI1SDM1LjQyNzZWMjAwLjE4MkgxMy4wNTU0VjMwMC41ODhDNS4zODYgMjg0LjAyNSAwIDI2MC4zNjYgMCAyMjYuNThDMCAxMDkuMjc3IDczLjUzMTYgMTE4LjM5NCA3My41MzE2IDExOC4zOTRIMjI2LjI3M1YxMDIuMTEzSDExNy4wMzZWNTAuMTc3NFpNMjM3LjMzNiAyMTkuMDU4SDIxNy4yMzdDMjE3LjU0NSAyMTguODQ4IDIxNy44NjIgMjE4LjY0NiAyMTguMTg3IDIxOC40NTJDMjIwLjg1IDIxNi44NTQgMjIzLjkwNCAyMTYuMDU1IDIyNy4zNDkgMjE2LjA1NUMyMzAuNjUxIDIxNi4wNTUgMjMzLjU0NSAyMTYuNzgzIDIzNi4wMzEgMjE4LjIzOUMyMzYuNDg0IDIxOC40OTQgMjM2LjkxOSAyMTguNzY3IDIzNy4zMzYgMjE5LjA1OFpNMTc1LjI1MyAzOC4wNDA2QzE3MS45NyAzNS45NTEzIDE2OC4xNDUgMzQuODg4OCAxNjQuMjYxIDM0Ljk4NzRMMTY0Ljc2MyAzNS4xNTAyQzE1OS41NTQgMzUuMTUwMiAxNTQuNTU4IDM3LjIzMjYgMTUwLjg3NCA0MC45MzkyQzE0Ny4xOTEgNDQuNjQ1OCAxNDUuMTIyIDQ5LjY3MzEgMTQ1LjEyMiA1NC45MTUxVjU1LjI0MDdDMTQ1LjIxOSA1OS4xNDg4IDE0Ni40NjYgNjIuOTQgMTQ4LjcwNCA2Ni4xMzVDMTUwLjk0MyA2OS4zMzAxIDE1NC4wNzIgNzEuNzg1MyAxNTcuNjk4IDczLjE5MDNDMTYxLjMyMyA3NC41OTUzIDE2NS4yODEgNzQuODg2OCAxNjkuMDcgNzQuMDI4MkMxNzIuODYgNzMuMTY5NSAxNzYuMzEyIDcxLjE5OTIgMTc4Ljk4OSA2OC4zNjYzQzE4MS42NjYgNjUuNTMzNCAxODMuNDQ4IDYxLjk2NTMgMTg0LjExIDU4LjExMzJDMTg0Ljc3MiA1NC4yNjEgMTg0LjI4NCA1MC4yOTc5IDE4Mi43MDcgNDYuNzI1QzE4MS4xMzEgNDMuMTUyMSAxNzguNTM3IDQwLjEyOTkgMTc1LjI1MyAzOC4wNDA2Wk0zNy4yOTE5IDI1My44MjJDMzUuOTQyNSAyNTAuMiAzNS4yNjc4IDI0NS45NTYgMzUuMjY3OCAyNDEuMDkxQzM1LjI2NzggMjM2LjIyNiAzNS45NDI1IDIzMiAzNy4yOTE5IDIyOC40MTNDMzguNjQxMyAyMjQuODI3IDQwLjU3NjcgMjIyLjA1NyA0My4wOTggMjIwLjEwNEM0NS42NTQ4IDIxOC4xNTEgNDguNzc5OCAyMTcuMTc0IDUyLjQ3MyAyMTcuMTc0QzU2LjIwMTcgMjE3LjE3NCA1OS4zNDQ1IDIxOC4xODYgNjEuOTAxMyAyMjAuMjFDNjQuNDU4MSAyMjIuMjM0IDY2LjM5MzUgMjI1LjA0IDY3LjcwNzQgMjI4LjYyNkM2OS4wMjEzIDIzMi4yMTMgNjkuNjc4MyAyMzYuMzY4IDY5LjY3ODMgMjQxLjA5MUM2OS42NzgzIDI0NS44NDkgNjkuMDAzNiAyNTAuMDU4IDY3LjY1NDEgMjUzLjcxNUM2Ni4zNDAyIDI1Ny4zMzcgNjQuNDA0OCAyNjAuMTc4IDYxLjg0OCAyNjIuMjM4QzU5LjI5MTIgMjY0LjI2MiA1Ni4xNjYyIDI2NS4yNzQgNTIuNDczIDI2NS4yNzRDNDguODE1MyAyNjUuMjc0IDQ1LjcwODEgMjY0LjI4IDQzLjE1MTMgMjYyLjI5MUM0MC41OTQ1IDI2MC4yNjcgMzguNjQxMyAyNTcuNDQ0IDM3LjI5MTkgMjUzLjgyMloiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMzM1LjQ3OSA0MDIuODIzQzMzNS40NzkgNDAyLjgyMyAzNDIuNzQzIDQ1Mi45NjggMjI3Ljg3NSA0NTIuOTY4TDIyNy44MjcgNDUzLjAwMUgyMjcuMThDMTA3LjIzMiA0NTMuMDAxIDExNi40ODYgMzkyLjU2NiAxMTYuNDg2IDM5Mi41NjZWMzEyLjYwMkMxMTcuNDIgMzEyLjY1NSAxMTguMzc1IDMxMi42ODIgMTE5LjM1IDMxMi42ODJDMTI0Ljk2MSAzMTIuNjgyIDEyOS43NTUgMzExLjc3NiAxMzMuNzMyIDMwOS45NjVDMTM3LjcwOSAzMDguMTkgMTQwLjk5NCAzMDUuNjUxIDE0My41ODYgMzAyLjM0OEMxNDYuMjE0IDI5OS4wODEgMTQ4LjI5MiAyOTUuMjQ2IDE0OS44MTkgMjkwLjg0MkwxNjkuODM2IDIzMy43NzRDMTc0LjUzNyAyMzMuMTggMTc3LjU2IDIzMy4yMjYgMTc3LjU2IDIzMy4yMjZIMTg3Ljg2QzE4Ny40ODEgMjM1Ljg1MyAxODcuMjkyIDIzOC41OTkgMTg3LjI5MiAyNDEuNDY0QzE4Ny4yOTIgMjUwLjA5MyAxODguOTI1IDI1Ny41NjggMTkyLjE5MiAyNjMuODg5QzE5NS40NiAyNzAuMTc1IDIwMC4xMTIgMjc1LjA0IDIwNi4xNDggMjc4LjQ4NEMyMTIuMjIxIDI4MS44OTMgMjE5LjQ2NSAyODMuNTk4IDIyNy44ODEgMjgzLjU5OEMyMzQuNjI5IDI4My41OTggMjQwLjU3NyAyODIuNTY4IDI0NS43MjYgMjgwLjUwOUMyNTAuOTExIDI3OC40MTMgMjU1LjEzNiAyNzUuNTAxIDI1OC40MDMgMjcxLjc3M0MyNjEuNzA2IDI2OC4wMDkgMjYzLjg5IDI2My42MDUgMjY0Ljk1NSAyNTguNTYyTDI0My45NjggMjU3LjE3OEMyNDMuMTg3IDI1OS4yMzcgMjQyLjA1IDI2MC45NzcgMjQwLjU1OSAyNjIuMzk4QzIzOS4wNjcgMjYzLjgxOCAyMzcuMjc0IDI2NC44ODQgMjM1LjE3OSAyNjUuNTk0QzIzMy4wODQgMjY2LjMwNCAyMzAuNzc2IDI2Ni42NTkgMjI4LjI1NCAyNjYuNjU5QzIyNC40NTUgMjY2LjY1OSAyMjEuMTcgMjY1Ljg2IDIxOC40IDI2NC4yNjJDMjE1LjYzIDI2Mi42NjQgMjEzLjQ4MiAyNjAuMzkxIDIxMS45NTUgMjU3LjQ0NEMyMTAuNDYzIDI1NC40OTYgMjA5LjcxNyAyNTAuOTk5IDIwOS43MTcgMjQ2Ljk1VjI0Ni44OTdIMjY1LjQzNVYyNDAuNjY1QzI2NS40MzUgMjM4LjA2MSAyNjUuMjk4IDIzNS41ODIgMjY1LjAyNSAyMzMuMjI2SDI4MC4yNDNWMjgySDMwMi45MzVWMjM0LjY5OUMzMDIuOTQ1IDIzMy42NTkgMzAzLjAxIDIzMi42NjMgMzAzLjEyOSAyMzEuNzEzQzMxMy4yODMgMjI5LjY3MiAzMjEuMjQ1IDIyNS43MDkgMzI3LjQ4NyAyMjAuNzE0QzMyOC4wNzcgMjIxLjE2NSAzMjguNjI5IDIyMS42NzIgMzI5LjE0MiAyMjIuMjM0QzMzMS43MzQgMjI1LjA0IDMzMy4wMTMgMjI4Ljk0NiAzMzIuOTc3IDIzMy45NTNWMjgySDM1NS42NjlWMjI5LjkwNUMzNTUuNjY5IDIyMy41NDggMzU0LjQ5NyAyMTguMDggMzUyLjE1MyAyMTMuNDk5QzM0OS44MSAyMDguODgyIDM0Ni41MjUgMjA1LjMzMSAzNDIuMjk5IDIwMi44NDVDMzQyLjE5MyAyMDIuNzgzIDM0Mi4wODYgMjAyLjcyMSAzNDEuOTc5IDIwMi42NkMzNTAuNjc2IDE4NS42NTcgMzUwLjEwNCAxNjcuODkxIDM1MC4xMDQgMTY3Ljg5MVYxMTMuODg4SDM4OC4wNzVDMzg4LjA3NSAxMTMuODg4IDQ1MyAxMDkuODAyIDQ1MyAyMjYuNDIxQzQ1MyAzNDMuMDQgMzc5LjQ2OCAzMzQuNzY5IDM3OS40NjggMzM0Ljc2OUgyMjYuMjU3VjM1MS4wNUgzMzUuNDc5VjQwMi44MjNaTTE0Ni4wMzcgMjQwLjhDMTQyLjYwNSAyNDIuNTIgMTM5LjE5MSAyNDQuNjMxIDEzNS45NjYgMjQ3LjIyTDEzOS42NDUgMjYwLjI2N0gxNDAuNDk3TDE0Ni4wMzcgMjQwLjhaTTEyMS42OTkgMjY1LjcyNEMxMTguNDYgMjcyLjk4NCAxMTYuNDg2IDI4MS44NjcgMTE2LjQ4NiAyOTIuNzMzVjI5NC42OEMxMTYuNzg4IDI5NC43MDQgMTE3LjA4NiAyOTQuNzIxIDExNy4zNzkgMjk0LjczMUMxMTkuNTQ1IDI5NC44MDIgMTIxLjQwOSAyOTQuMzA1IDEyMi45NzIgMjkzLjIzOUMxMjQuNTcgMjkyLjE3NCAxMjUuODY2IDI5MC4zNjMgMTI2Ljg2IDI4Ny44MDZMMTI4LjE5MiAyODQuMzQ0TDEyMS42OTkgMjY1LjcyNFpNMjc3LjI2MSA0MTQuOTZDMjgwLjU0NSA0MTcuMDQ5IDI4NC4zNyA0MTguMTEyIDI4OC4yNTQgNDE4LjAxM0gyODcuNzUyQzI5Mi45NjEgNDE4LjAxMyAyOTcuOTU3IDQxNS45MzEgMzAxLjY0IDQxMi4yMjRDMzA1LjMyNCA0MDguNTE3IDMwNy4zOTMgNDAzLjQ5IDMwNy4zOTMgMzk4LjI0OFYzOTcuNzZDMzA3LjI5NiAzOTMuODUyIDMwNi4wNDkgMzkwLjA2IDMwMy44MSAzODYuODY1QzMwMS41NzIgMzgzLjY3IDI5OC40NDIgMzgxLjIxNSAyOTQuODE3IDM3OS44MUMyOTEuMTkyIDM3OC40MDUgMjg3LjIzNCAzNzguMTE0IDI4My40NDQgMzc4Ljk3MkMyNzkuNjU0IDM3OS44MzEgMjc2LjIwMyAzODEuODAxIDI3My41MjYgMzg0LjYzNEMyNzAuODQ5IDM4Ny40NjcgMjY5LjA2NiAzOTEuMDM1IDI2OC40MDUgMzk0Ljg4N0MyNjcuNzQzIDM5OC43NCAyNjguMjMxIDQwMi43MDMgMjY5LjgwOCA0MDYuMjc2QzI3MS4zODQgNDA5Ljg0OCAyNzMuOTc4IDQxMi44NzEgMjc3LjI2MSA0MTQuOTZaTTM5Mi43MyAyODJINDE4LjI5OEw0NDYuOTAyIDIwMC4xODJINDIyLjg3OUw0MDUuOTQgMjU4LjcyMkg0MDUuMDg4TDM4OC4wOTUgMjAwLjE4MkgzNjQuMTI1TDM5Mi43MyAyODJaIiBmaWxsPSIjMEY4MUMyIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfNzVfMzAiPgo8cmVjdCB3aWR0aD0iNDUzIiBoZWlnaHQ9IjQ1MyIgZmlsbD0id2hpdGUiLz4KPC9jbGlwUGF0aD4KPC9kZWZzPgo8L3N2Zz4K)](https://github.com/pyenv/pyenv)
[![Poetry](https://img.shields.io/badge/Poetry-1.8.3-60a5fa?logo=poetry)](https://python-poetry.org)

Este guia tem como objetivo auxiliar no processo de criação de projetos `FastAPI` utilizando o terminal do `Ubuntu WSL`. Abaixo está uma lista de comandos e etapas úteis para criar e configurar seu projeto.

## **1. Instalação do `pyenv`, `pipx` e `poetry`**
Antes de criar um projeto com `FastAPI`, você pode utilizar o `pyenv` para gerenciar versões de `Python`. Siga os passos abaixo para instalar o `pyenv`:

- Atualize os pacotes do sistema:
    ```shell
    sudo apt update && sudo apt upgrade
    ```

- Instale dependências necessárias para o pyenv
    ```shell
    sudo apt install -y make build-essential libssl-dev zlib1g-dev \
    libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
    libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
    ```

- Clone o repositório pyenv
    ```shell
    curl https://pyenv.run | bash
    ```

- Adicione o pyenv ao PATH
    ```shell
    echo -e '\n# Pyenv Configuration\nexport PYTHON_BUILD_ARIA2_OPTS="-x 10 -k 1M"\nexport PATH="${HOME}/.pyenv/bin:$PATH"\neval "$(pyenv init --path)"\neval "$(pyenv init -)"\neval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
    ```

- Reinicie o terminal

- Atualize e verifique se o `pyenv` foi instalado, o comando abaixo deverá listar a versão do pyenv e os seus comandos
    ```shell
    pyenv update
    pyenv
    ```

- Instale a versão do python desejada

    ```shell
    pyenv install 3.12:latest
    ```

- Instale o `pipx` e o `poetry` para gerenciar pacotes

    ```shell
    pip install pipx && pipx install poetry
    ```

## 2. Criando projeto com `poetry`:

- Entre na raiz onde você deseja criar o projeto como por exemplo o disco C:

    ```shell
    cd /mnt/c
    ```
- Crie o projeto

    Utilize nomes como "meu_projeto", não utilize caractéres especiais ou acentuação, e use _ (underline) no lugar dos espaços.

    ```shell
    poetry new [project_name]
    ```

- A estrutura do projeto estará assim:

    ```shell
    C:
    └── project_name
        ├── README.md
        ├── project_name
        │   └── __init__.py
        ├── pyproject.toml
        └── tests
            ├── __init__.py
            └── test_project_name.py
    ```

- Entre no projeto

    ```shell
    cd project_name
    ```

- Renomeie a pasta do projeto para src

    ```shell
    sudo mv project_name src
    sudo mv tests/test_project_name.py tests/test_src.py
    ```

- Sete a versão do python do projeto local

    ```shell
    pyenv local 3.12.6
    ```
- Instale as dependências do poetry

    ```shell
    poetry install
    ```

- Adicione FastAPI ao projeto e crie o ambiente de desenvolvimento

    ```shell
    poetry add 'fastapi[standard]'
    ```

- Inicie o ambiente

    ```shell
    poetry shell
    source $(poetry env info --path)/bin/activate
    ```

- Adicione `ruff`, `pytest`, `taskipy` ao projeto

    ```shell
    poetry add --group dev ruff pytest pytest-cov taskipy
    ```

- Adicione as configurações ao `pyproject.toml`

    ```shell
    [tool.ruff]
    line-length = 79
    extend-exclude = ['migrations']

    [tool.ruff.lint]
    preview = true
    select = ['I', 'F', 'E', 'W', 'PL', 'PT']

    [tool.pytest.ini_options]
    pythonpath = "."
    addopts = '-p no:warnings'

    [tool.taskipy.tasks]
    lint = 'ruff check .; ruff check . --diff'
    format = 'ruff check . --fix; ruff format .'
    run = 'fastapi dev fast_zero/app.py'
    pre_test = 'task lint'
    test = 'pytest -s -x --cov=fast_zero -vv'
    post_test = 'coverage html'
    ```

- Instale o `ignr`

    ```shell
    pipx install ignr
    ```

- Crie `.gitignore` utilizando o `ignr`

    ```shell
    ignr -p python > .gitignore
    ```

- Criar arquivos básicos de estrutura do projeto:

    ```shell
    sudo touch .env src/app.py src/routes.py src/config.py src/models.py src/schemas.py
    ```

- Instale o `alembic`

    ```shell
    poetry add alembic
    ```

- Outros comandos (não executar)

    ```shell
    alembic init migrations
    alembic revision --autogenerate -m "create users table"
    alembic upgrade head

    sudo apt install sqlite3
    sqlite3 database.db
    .schema
    SELECT * FROM alembic_version;
    echo 'database.db' >> .gitignore
    echo 'log.txt' >> .gitignore
    ```