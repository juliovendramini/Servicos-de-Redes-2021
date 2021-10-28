# Alterar porta SSH
Por padrão o serviço SSH utiliza a porta 22, caso queira utilizar uma outra porta deverá alterar seu arquivo de configuração


## Configurando porta 8080 para o SSH
Primeiro abra o arquivo de configuração SSH:
```
nano /etc/ssh/sshd_config
```
Você encontrará um arquivo praticamente todo comentado  logo no início também é possivel ver a configuração da porta comentada, o que segnifica que o SSH está utilizando a porta default 22, para alterar essa configuração você pode por exemplo incluir uma nova linha com o texto
```
Port 8080
```
Ou simplemesmente descomentar o que já existe e alterar por ali, após feitas alterações salve e feche o arquivo. Para que as alterações realizadas sejam aplicadas reinicie o serviço SSH com o comando: 
```
sudo systemctl restart sshd.service
```