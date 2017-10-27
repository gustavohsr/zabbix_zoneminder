# zabbix
Configurações e Scripts para o Zabbix

editar /etc/zabbix/zabbix_agentd.conf
#### ZONEMINDER STATUS
UserParameter=zm.status,service zoneminder status | grep -i running | awk '{print $3}'| sed 's/[( )]//g'

Em seguida configurar no Zabbix Server o item a ser monitorando usando a chave 'zm.status' configurando posteriormente a trigger e ações de recuperação.
