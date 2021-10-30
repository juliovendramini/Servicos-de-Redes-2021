# Configurando o seu site para o Apache2
Primeiro crie o diretório do seu site:
```
sudo mkdir /var/www/alethalys/
```
Em seguida crie e edite o arquivo index.html:
```
cd /var/www/alethalys/
nano index.html
```
Inclua o html desejado acima.

Acesse o diretório que contém o arquivo de configuração default do Apache2:
```
cd /etc/apache2/sites-available/
```
Edite o arquivo padrão de configuração:
```
nano 000-default.conf
```
Altere o DocumentRoot para apontar para apontar pro seu diretório:
`
DocumentRoot /var/www/alethalys
`

Reinicie o apache:
```
service apache2 reload
```
### Pronto, agora basta acessar seu domínio e poderá ver seu site com a estrutura que você definiu =).
