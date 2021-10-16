## Primeiro deve-se instalar o sudo:

### Atualizar as listas de pacote para atualização:
> apt-get update -y

### Buscar por estas novas atualizações:
> apt-get upgrade -y

### Instalar:
> apt-get install sudo -y

## Após isto, deve-se atribuir os privilégios de sudo ao usuário:

### Atribuir usuário ao sudo
> adduser <seu usuário> sudo
