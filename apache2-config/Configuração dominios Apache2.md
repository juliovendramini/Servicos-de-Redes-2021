# Configuração do Apache 2

Para a servir a aplicação Angular, um servidor web é necessário.

O Apache 2 é o mais indicado, por possuir um sistema de configuração simples e eficaz, além de ser ótimo para ambientes linux.

## Passos

*Observação: Os comandos devem ser executados como root, ou seja, sudo*.

1. Instalar o apache.
    
    **apt install apache2**
    

1. Criar a pasta em que ficará hospedado os arquivos de sua aplicação WEB.
    
    **mkdir -p /var/www/seudominio.com/public_html**
    
2. Garantir as permissões de leitura da pasta do apache.
    
    **chmod -R 755 /var/www**
    

1. Copiar todo o conteúdo de sua aplicação para a pasta.
    
    **/var/www/seudominio.com/public_html**
    
2. Criação dos arquivos de host virtual.
    
    Primeiramente, o apache já vem com um arquivo de configuração padrão, denomidado 000-default.conf.
    
    Nós deveremos fazer uma cópia desse arquivo para servir de base para a nossa aplicação.
    
    **cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/seudominio.com.conf**
    
    Após isso, abra o arquivo de configuração criado "**seudominio.com.conf**" com qualquer editor de texto, e edite para ficar semelhante ao arquivo a seguir:
    
    ```
    <VirtualHost *:80>
        ServerAdmin admin@example.com
        ServerName seudominio.com
        ServerAlias www.seudominio.com
        DocumentRoot /var/www/seudominio.com/public_html
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>
    ```
    

1. Habilitar o arquivo de configuração criado.
    
    **a2ensite seudominio.com.conf**
    
2. Desabilitar o arquivo de configuração de padrão.
    
    **a2dissite 000-default.conf**
    
3. Restartar o serviço do apache.
    
    **systemctl restart apache2**
