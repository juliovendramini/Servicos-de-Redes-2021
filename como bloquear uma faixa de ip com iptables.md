## Comando para bloquear faixa de ip

Para bloquear uma faixa de ip com iptables utilizamos do comando sudo iptables -I INPUT -s 172.16.39.0/255.255.255.0 -j DROP

## Salvando regra
Para salvar as regras utiliza do comando iptables-save > /etc/iptables/rules.v4
