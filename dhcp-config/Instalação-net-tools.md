# Instalação do Net Tools

A instalação do net tools é bastante importante para o funcionamento dos serviços de redes, pois suas funções irão auxiliar na listagem das interfaces de rede, na consulta de IP(Internet Protocol), etc.

## Net Tools

O pacote net tools é um conjunto de ferramentas para controlar o sub-sistema de rede do kernel do Linux.

## Instalação

Passos para a intalação:

>**sudo apt-get install net-tools**

>Digite **"Y"** para confirmar que deseja continuar com a instalação.

Após esses passos, o net tools deve ter sido instalado. Para conferir, digite:

>**ifconfig**

Esse comando deve listar todas as interfaces de rede da máquina e suas informações.

## Comandos

- **arp**: Exibe e manipula o sistema do cache ARP.
- **ether-wake**: Permite enviar uma mensagem Wol (Wake-on-LAN) para “ligar” o servidor via mensagem de rede.
- **ifconfig**: Exibir/configurar uma interface de rede.
- **ipmaddr:** Adiciona, remove e exibe um endereço multicast.
- **iptunnel:** Cria, remove e exibe túneis configurados.
- **mii-diag:** Controle de adaptador de rede e monitoramento pconfig.
- **mii-tool:** Exibir o status de todas interfaces de rede.
- **nameif:** Nomear interfaces de rede de acordo com o endereço de MAC.
- **netstat: E**xibe conexões de rede, tabelas de roteamento, estatísticas de interfaces, masquerade…
- **plipconfig:** Melhorar parâmetros do PLIP.
- **route:** Exibir e manipular tabela de roteamento de IP.
- **slattach:** Conectar uma interface de rede a uma linha serial.