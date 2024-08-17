# Subindo ambiente Ubuntu 24.04

## Faça o download da imagem do Ubuntu 24.04

<img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu">

[Download Ubuntu 24.04](https://ubuntu.com/download/desktop)

## Instale o Ubuntu 24.04

Crie um pendrive bootável com a imagem do Ubuntu 24.04 e instale o sistema operacional. Configure, usuário e
senha.

## Atualizando a loja e aplicativos

```shell
snap refresh
```

## Atualizar os pacotes e o sistema

```shell
sudo apt update && sudo apt upgrade -y
```

## Instalar o git

```shell
sudo apt install git
```

## Instalar o PHP8.3 e extenções

```shell
sudo apt install software-properties-common -y
```

```shell
sudo add-apt-repository ppa:ondrej/php -y
```

```shell
sudo apt update
```

```shell
sudo apt install php8.3
```

## Instalar o PHP-CGI

```shell
sudo apt install php-cgi
```

## Instalar o XDEBUG

```shell
sudo apt install php8.3-xdebug
```

## Instalar o Composer

```shell
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
```

## Verificar a instalação do composer e instalar os demais requisitos

```shell
composer diagnose
```

```shell
sudo apt install php8.3-zip php8.3-curl
```

## Instalar o curl

```shell
sudo apt install curl
```

## Instalar o nodejs

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
```

```shell
source ~/.bashrc
```

```shell
nvm install 20
```

## Instalar o PHPStorm, PYCharm e DataGrip pela loja do Ubuntu

## Instalar o VScode pela loja do Ubuntu

## Instalar o MYSQL

```shell
sudo apt install mysql-server
```

```shell
sudo mysql
```

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'defina_aqui_senha_root';

flush privileges;

exit;

```shell
sudo mysql_secure_installation
```

## Seguir os passos de configuração

```shell
sudo mysql -u root -p
```

show databases;

## Instalar o postman pela loja de aplicativos

## Instalar o Docker

## Adicionar a chave GPG oficial do Docker

```shell
# Add Docker's official GPG key:
sudo apt get update
sudo apt get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

## Instalar o Docker

```shell  
sudo apt get update
```

## Para instalar a versão mais recente do Docker, execute o comando abaixo:

```shell
sudo apt get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Verificar a instalação do Docker

```shell
sudo docker run hello-world
```

## Para permitir que seu usuário atual use o Docker, adicione-o ao grupo docker com o comando abaixo:

```shell
sudo groupadd docker
```

## Adicione seu usuário ao grupo docker com o comando abaixo:

```shell
sudo usermod -aG docker $USER
```

## Para aplicar as alterações, faça logout e login novamente ou execute o comando abaixo:

```shell
newgrp docker
```

## Para verificar se o Docker foi instalado corretamente e se o daemon do Docker está em execução, execute o comando abaixo:

```shell
docker run hello-world
```

## Instalar o Kubernetes(Kubectl) e Minikube

### Instalar o Kubectl

```shell
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```

```shell
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
```

```shell
echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check
```

```shell
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

```shell
kubectl version --client
```

## Instalar o Minikube

```shell
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```

```shell
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
```

## Configurar o git

Configurar o nome de usuário

```shell
git config --global user.name "Seu Nome de Seu Usuário do Github"
```

Configurar o email de usuário

```shell
git config --global user.email "Seu Email de Seu Usuário do Github"
```

Configurar o editor de texto

```shell
git config --global color.ui auto
```

Gerar a chave SSH

```shell
ssh-keygen -t ed25519 -C "Seu Email de Seu Usuário do Github"
```

Copiar a chave SSH

```shell
cat ~/.ssh/id_ed25519.pub
```

[Adicionar a chave SSH no Github](https://github.com/settings/keys)

### Autor: Paulo Coelho

- [Dev Paulo Coelho](https://devpaulocoelho.com/)
- [Credly](https://www.credly.com/users/paulo-henrique-medina-coelho)
- [Microsoft Learn](https://learn.microsoft.com/pt-br/users/paulohenriquemedinacoelho/transcript/d9w2s0gyqmz2z87?tab=credentials-tab)

### Contato:

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:paulomedinabr01@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/paulohcoelho/)
