# IP Estático para uma interface de rede
Na criação e configuração de um servidor DHCP você irá perceber que as configurações realizadas podem estar atribuindo um IP para o servidor que irá perdurar apenas durante a sessão, para configurar o IP do servidor de maneira permanente e de forma estática siga esse tutorial.


## Liste suas interfaces de rede disponíveis
Para listar as interfaces de redes disponíveis e resgatar a que será o seu servidor dependerá se se ela já está ativa:
```
sudo ifconfig
```
Ou se encontra inativa:
```
ip a
```

Após listadas você já pode visualizar o nome da interface que está atribuída ao servidor.

## IP Estático
Primeiramente abra o arquivo de configuração:
```
sudo nano /etc/network/interfaces
```
Em seguida adicione o seguinte trecho ao arquivo:
````
auto enps011
iface enps011 inet static
  address 192.168.0.2
  netmask 255.255.255.0
````


`
Para o exemplo acima a interface de rede a qual atribuímos um IP Estático foi a enps011, você deverá adaptar esse trecho conforme sua interface,
`