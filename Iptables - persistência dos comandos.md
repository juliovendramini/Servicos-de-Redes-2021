Salvando as regras atuais:
sudo iptables-save > /etc/iptables/rules.v4

Ao reiniciar, para retornar as regras salvas (Este comando irá apagar as regras atuais e colocará as salvas):
sudo iptables-restore < /etc/iptables/rules.v4

Para que o restore não sobrescreva, o comando deve ser:
sudo iptables-restore -n < /etc/iptables/rules.v4

Para automatizar o processo de restore:
sudo aptitude install iptables-persistent
