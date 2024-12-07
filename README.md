# Criando Ambientes Virtuais em Python

Saudações pessoal, este repositório se destina a criação de ambientes virtuais, tanto para gerênciar pacotes quanto versões do proprio python.

## Usando Poetry Para Gerência a Versão

Instale o poetry usando meu tutorial [aqui](https://github.com/mauriciobenjamin700/Poetry-Learning)

Primeiro instale as dependências:

Linux (Ubuntu):

Abra um terminal, apertando o atalho CRTL + ALT + T ou digite aperte a tecla do windows e digite terminal, ou clique com o botão direito na tela, e escolha a opção "Abrir Terminal" (somente para Ubuntu 15.10 ou superior, para 14.04 é necessário instalar o pacote nautilus-open-terminal e reiniciar)

Primeiro, atualize a lista de pacotes:

```bash
sudo apt-get update
```
Instale os pacotes básicos

```bash
sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm gettext libncurses5-dev tk-dev tcl-dev blt-dev libgdbm-dev git python2-dev python3-dev aria2 lzma liblzma-dev

```

depois:

```bash
curl -L https://raw.githubusercontent.com/pyenv/pyenv-installer/master/bin/pyenv-installer | bash
```

logo após, edite o arquivo .bashrc localizado na "Pasta Pessoal" ou Home do seu usuário, com o comando:

```bash
gedit ~/.bashrc
```

adicione esses comandos ao final do arquivo:

```bash
export PYTHON_BUILD_ARIA2_OPTS="-x 10 -k 1M"

export PATH="${HOME}/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

feito isso, salve o arquivo, feche o gedit e feche TODOS os terminais para poder aplicar a configuração.



Abra novamente um terminal, apertando o atalho CRTL + SHIFT + T .



Você pode ver as versões do interpretador Python que podem ser instalados com o comando:

```bash
pyenv install -l
```

Se a versão do interpretador Python que você quer instalar não aparecer na lista, tente atualizar da base de dados de versões do interpretadores rodando pyenv

```bash
pyenv update
```

Instale o pyenv (vou usar a versão 3.5.1 nos exemplos a seguir, mas você pode usar qualquer uma das versões listadas ao executar pyenv install -l )

```bash
pyenv install 3.5.1
```

logo após, defina o Python 3.5.1 como o python padrão do seu usuário:

```bash
pyenv global 3.5.1
```

ps: Se você instalou múltiplas versões do interpretador python e quer deixa-las disponíveis para uso execute

```bash
pyenv global versao_principal segunda_versao terceira_versao
```
exemplo, vamos supor que você instalou o Python 3.5.1, 3.6.2, 2.7.13 , então o comando seria:

```bash
pyenv global 3.5.1 3.6.2 2.7.13
```
Verifique a versão instalada com:

```bash
python -V
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
