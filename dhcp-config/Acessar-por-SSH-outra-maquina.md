# Método 01 - Terminal 
## 1. Acessar terminal da sua máquina 
Configura se sua máquina já possui o serviço SSH habilitado, caso não possua você deverá instalar antes de executar esses passos.
Aqui está um tutorial para Linux: [Instalando SSH](https://github.com/juliovendramini/Servicos-de-Redes-2021/blob/main/dhcp-config/Instalando-SSH.md)
## 2. Digitar o comando:
>ssh [usuário da máquina DE LÁ]@[IP/DNS] -p [Porta]
### Caso o (-p [porta]) não for preenchida e você não tiver alterado as predefinições do serviço SSH ele por padrão irá utilizar a porta 22
O acesso em alguns lugares por essa porta (22) pode resultar em um acesso negado.
# Método 02 - Putty
## 1. Instalar o Putty
>https://www.putty.org/
## 2. Ao abrir o Putty, marcar 'connection type' como SSH
## 3. Em Host Name, digitar o comando:
>[usuário da máquina DE LÁ]@[IP/DNS]
## 4. Se necessário, mudar a porta no campo 'Port' (ao lado)
## 5. Clicar em 'open'
