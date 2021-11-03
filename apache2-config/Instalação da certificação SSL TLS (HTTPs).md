# Instalação da certificação SSL/TLS (HTTPs)

Nessa instalação, usaremos o certbot, que é um bot construido com python pela empresa Let's Encrypt

### Pré-requisitos

- Ubuntu 18.04
- Instalação do apache2
- Configuração de domínio do apache2

## Passos

*Observação: Os comandos devem ser executados como root, ou seja sudo.*

1. Instalar o certbot:

**apt-get install certbot python3-certbot-apache**

1. Inserir um email para a chegada dos logs e erros.

![Untitled](assets/Untitled.png)

1. Concordar com os passos, digitando "**a**" e, logo em seguida, "**y**".

![Untitled](assets/Untitled%201.png)

1. Nesse passo, o certbot deve listar todos os domínios configurados no servidor, perguntando quais o usuário deseja instalar as certificações.
    
    Para instalar em todos os domínios, é só deixar em branco.
    
    ![Untitled](assets/Untitled%202.png)
    

1. O Último passo é somente forcar o uso do HTTPs, digitando "**2**".

![Untitled](assets/Untitled%203.png)

1. Pronto, certificações instaladas e HTTPs funcionando

![Untitled](assets/Untitled%204.png)

![Untitled](assets/Untitled%205.png)

1. Para renovar a certificação automaticamente a cada 3 meses, digite o seguinte comando

**echo "0 0,12 * * * root python -c 'import random; import time; time.sleep(random.random() * 3600)' && certbot renew" | sudo tee -a /etc/crontab > /dev/null**
