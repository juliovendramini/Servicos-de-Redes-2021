## IPTables é o nome da ferramenta da interface do usuário, que permite a criação de regras de firewall e Nat.

Principais comandos do IPTables
Substituindo uma regra:
iptables -R [regra] iptables –-replace [Regra]

Listando Regras:
iptables –L
iptables –-list
iptables –L OUTPUT
Criar regra:
iptables –A
iptables –-append

Criar uma regra em determinada “linha” de prioridade:
iptables –I [linha] iptables -–insert [linha]

Deletando uma regra:
iptables –D [Regra] iptables –-delete [Regra]

Removendo todas as regras:
iptables –F
iptables -–flush
iptables –F INPUT
iptables –t nat –F

Zerar contadores:
iptables –Z
iptables –-zero
iptables –Z INPUT
Criar nova CHAIN
iptables –N NOVACHAIN
iptables –-new-chain NOVACHAIN
iptables –t nat –N novachain

Renomeando CHAINS
iptables –E ANTIGACHAIN NOVACHAIN
iptables –-rename-chain ANTIGACHAIN NOVACHAIN
Deletando CHAINS
iptables –X NOMEDACHAIN
iptables -–delete-chain NOMEDACHAIN

Regras padrão:
iptables –P
iptables –-policy

Ajuda do Iptables
iptables –h
iptables –-help
