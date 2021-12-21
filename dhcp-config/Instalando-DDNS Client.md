# Instalando DDCliente
Se você possui acesso a uma máquina que hospeda seu serviço e esse acesso é feito unicamente por  ***IP da máquina*** você está correndo um risco muito de claro de:  ***perder o acesso a essa máquina cada o IP mude***, tendo que de alguma forma conseguir o IP novo para voltar a utilizar ela. Para resolver esse problema iremos configurar um utilitário do Linux que irá trabalhar com o ***DDNS (DynamicDNS)*** o  ***DDClient***, ele através de um domínio que vamos escolher fará o trabalho de  ***atualizar o IP para o domínio escolhido de forma automática caso ele mude***, sem que precisemos nos preocupar com isso.


## Registrando um domínio gratuito
Um dos possíveis sites que podemos registrar domínios gratuitos é o [FreeDNS - Afraid](https://freedns.afraid.org/)
Para criar um novo domínio nesse site você precisa estar previamente cadastrado nele, se registre e então crie seu domínio.

## Configurando DDClient

1 - Primeiro de tudo instale o aptitude:
```
sudo apt-get install aptitude
```
2 - Em seguida instale o DDClient:
```
aptitude install ddclient
```

`
A instalação do ddclient irá te questionar sobre algumas informações de seu domínio, preencha da exata forma a qual preencheu no ato de cadastramento feito anteriormente. Este preenchimento por interface é justamente para que seja feito o preenchimento do arquivo de configuração /etc/ddclient.conf
`
