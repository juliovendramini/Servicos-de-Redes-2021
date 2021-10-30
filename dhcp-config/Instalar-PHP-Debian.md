# Instalar PHP 8 no Debian

## 0. Verificar versão do PHP atual (se tiver)
>php -V

## 1. Instalar os pacotes:
>sudo apt-get install lsb-release apt-transport-https ca-certificates
## 2. Adicionar chave GPG 
>sudo wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
## 3. Adicionar repositório para instalar o PHP
>echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/php.list
## 4. Atualizar o APT
>sudo apt update
## 5. Instalar o PHP + módulos
>sudo apt install php8.0 php8.0-intl php8.0-mysql php8.0-sqlite3 php8.0-gd
