# Erros php-mysql

### 1. Exibir erros na tela

Caso seu site apresente erros inesperados basta adicionar este comando em seu arquivo para exibir os erros na tela.

```php
ini_set('display_errors', '1');
ini_set('display_startup_errors', '1');
error_reporting(E_ALL);
```

Caso seu site apresente erro na conexão com o mariadb, existem alguns possiveis motivos para isso.

### 2. Erro mysqli_connect

Existem alguns possíveis motivos para este erro.

1. **Configuração do mariadb.**
    
    Para que a conexão seja feita corretamente é necessário criar um outro usuário no mariadb e garantir permições para que ele possa acessar os bancos, e com isso, utilizá-lo no seu arquivo de conexão.
    
    Para criar um novo usuário e definir suas permissões basta executar os seguintes comandos.
    
    ```sql
    mysql> CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'mypassword';
    mysql> GRANT ALL privileges ON *.* TO 'myuser'@localhost;
    mysql> FLUSH PRIVILEGES;
    ```
    
    Para visualizar os usuários basta digitar.
    
    ```sql
    mysql> select host, user, password from mysql.user
    ```
    
    Após isto, você deve editar o seu arquivo de configuração do php para estabelecer a conexão correta com o banco de dados, colocando as credenciais do seu usuário que acabou de criar.
    
    ```php
    <?php
    ini_set('display_errors', '1');
    ini_set('display_startup_errors', '1');
    error_reporting(E_ALL);
    $hostname = "localhost";
    $username = "myuser";
    $password = "mypassword";
    $database = "mydatabase";
    
    // connection
    $conn = mysqli_connect($hostname, $username, $password, $database);
    
    // check
    if (!$conn) {
        die("Error :" . mysqli_connect_error());
    }
    ```
    
    Com isso sua conexão está configurada.
    
    1. **Instalação do php-mysqli**
        
        É possível que o mysqli não esteja instalado em sua máquina, por isso execute o seguinte comando para realizar a instalação.
        
        ```powershell
        > sudo apt install php-mysqli
        ```
        

1. **Instalação de pacotes php**
    
    É possível que eteja faltando alguns pacotes php para serem instalados, para instalar todos os pacotes do php execute.
    
    ```powershell
    > sudo apt install -y php7.4-cli php7.4-dev php7.4-pgsql php7.4-sqlite3 php7.4-gd php7.4-curl php7.4-memcached php7.4-imap php7.4-mysql php7.4-mbstring php7.4-xml php7.4-imagick php7.4-zip php7.4-bcmath php7.4-soap php7.4-intl php7.4-readline php7.4-common php7.4-pspell php7.4-tidy php7.4-xmlrpc php7.4-xsl php7.4-opcache php7.4-apcu
    ```
    

### 3. Atualize o sistema

1. Após seguir esses passos atualize o sistema.
    
    ```powershell
    > sudo apt update
    > sudo apt upgrade
    ```
    
2. Após isto reinicie o apache.
    
    ```powershell
    > sudo systemctl restart apache2
    ```
    

Após isto o erro deverá ser corrigido.