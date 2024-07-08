# Criando Ambientes Virtuais em Python

Saudações pessoal, este repositório se destina a criação de ambientes virtuais, tanto para gerênciar pacotes quanto versões do proprio python.

## Usando Poetry Para Gerência a Versão

Instale o poetry usando meu tutorial [aqui](https://github.com/mauriciobenjamin700/Poetry-Learning)

### Instale o pyenv agora com Linux

```bash
# Instalar dependências necessárias
sudo apt update
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev \
python3-openssl git

# Baixar e instalar o `pyenv`
curl https://pyenv.run | bash

```

```bash
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

```bash
source ~/.bashrc
```

### Instalando Pyenv no windows

[Oficinal](https://github.com/pyenv-win/pyenv-win)

Passo a passo que usei caso o oficial não seja do seu agrado

```bash
Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
```

Quando terminar de instalar basta configurar usando `pyenv install "sua versão aqui sem as aspas"`

Reinicie o terminal

Definindo a versão local usando o comando `pyenv local 3.9.2`

## Ativando a env com Poetry

Inicie o Projeto com ``poetry init`

Use o comando `poetry env use 3.9.2` para criar a env com a versão específica

Instale os pacotes com  `poetry install`
