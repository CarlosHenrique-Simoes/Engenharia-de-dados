# Configuração do Ambiente de Trabalho

## PYENV - PYTHON ENVIRONMENT

### Instalar o PYENV no windows com o PYENV-WIN

Ativar as configurações do powershell com privilegios de administrador:

#### [Tutorial powershell unrestricted](https://www.top-password.com/blog/change-powershell-execution-policy-in-windows-10/)

![Imagem do powershell](https://www.top-password.com/blog/wp-content/uploads/2018/09/Set-ExecutionPolicy.png)

### Instalar o pyenv no windows

Rodar o código abaixo no powershell

`Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"`

#### [Documentação pyenv-win](https://github.com/pyenv-win/pyenv-win)

---


## Git Bash

### 1) Abrir o terminal de comando do Git:

![Imagem Git](https://media.geeksforgeeks.org/wp-content/uploads/20200421155539/git12.png)

---
### 2) Testar se o pyenv está conversando com o git bash

`pyenv --version`

![img git pyenv](https://user-images.githubusercontent.com/626824/118352193-54418500-b560-11eb-9f79-7e3132e0362e.png)

#### caso não esteja verificar a aula de boas vindas do pyenv terceira sessão informa como resolver o erro.

### 3) Rodar o codigo abaixo para excluir todas as bibliotecas

`pip freeze | grep -v "^-e" | xargs pip uninstall -y`

### 4) Instalar o pipx para controle de versão de instalação

`pip install pipx`

### 5) Instalar poetry para controle de ambiente virtual 

`pipx install poetry`

### 6) Instalar ipython para utilização do terminal como interpretador python

`pipx install ipython`

---
## VS Code
- Criar a pasta do projeto
- Entrar na pasta
- Abrir a pasta com o VS code


### 1) Configurar o pyenv para a pasta do projeto

`pyenv local 3.11.3`

### 2) Verificar se a versão está correta

`pyenv --version`

### 3) Verificar se o vs code aponta para o interpretador escolhido

### 4) Verificar se o poetry está funcionando na pasta do projeto 

`poetry --version`

### 5) Rodar o codigo abaixo caso o poetry não seja reconhecido

`export PATH="$HOME/.local/bin:$PATH"`

### 6) Configurando os ambientes virtuais do poetry

`poetry config virtualenvs.in-project true`

---
## Poetry

### 1) Inicializando o poetry

`poetry init`

### 2) Informar as configurações conforme formulário do poetry no terminal.

### 3) Incializar o shell do poetry

`poetry shell`

### 4) Adicionar bibliotecas com poetry

#### exemplo:

`poetry add pandas`

---

## Git no VS Code

### 1) Criar pasta .vs code:

### 2) Criar arquivo settings.json:

`{
    "files.exclude": {
        "**/.git": false
    }
}`

### 3) Criar arquivo .gitignore
Baixar o gitignore do site gitignoe.io

