# docker-mysql
Repositório de estudo de MySQL com Docker no Windows.

## Instalando o docker

Escolha um dos métodos abaixo para instalar o docker no Windows.

### 1. Através do instalador do Docker Desktop

Baixe o instalador do Docker Desktop no link abaixo:
https://hub.docker.com/editions/community/docker-ce-desktop-windows/

Siga as instruções do instalador.

Ao terminar, siga para a seção [Subindo o MySQL através do Docker Compose](#subindo-o-mysql-através-do-docker-compose).

### 2. Através do Chocolatey

#### Instalar o Chocolatey

Para instalar o Chocolatey, abra o terminal como administrador apertando tecla Windows + X e selecione Terminal (Administrador) e execute o comando abaixo:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Siga as instruções do instalador.
Ao terminar verifique a versão instalada com o comando:

```powershell
choco
```

Mais informações na [página oficial do Chocolatey](https://chocolatey.org/install).

#### Instalando o Docker + Compose

Ainda no terminal como administrador execute o comando abaixo:
```powershell
choco install docker-desktop docker-compose
```

Siga as instruções do instalador.
O Docker deverá estar instalado, junto do compose.
Abra o atalho no desktop e aguarde a inicialização.

## Subindo o MySQL através do Docker Compose

Com o terminal no diretório do arquivo docker-compose.yml execute o comando abaixo:
```powershell
docker-compose up -d
```

Ao terminar o comando do compose, acesse http://localhost:8080/ e verifique se o MySQL está rodando.

Acesse com:

```
usuário: root
senha: example
```

## Encerrar o MySQL (isso apagará todos os dados do banco!)

Com o terminal no diretório do arquivo docker-compose.yml execute o comando abaixo:
```powershell
docker-compose down
```
