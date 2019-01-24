# Zabbix e Zoneminder
Configurações e Scripts para o monitoramento do daemon do Zoneminder através do Zabbix


# No servidor Zoneminder acesse:
vim /etc/zabbix/zabbix_agentd.conf

# acrescente...
#### ZONEMINDER STATUS
UserParameter=zm.status,service zoneminder status | grep -i running | awk '{print $3}'| sed 's/[( )]//g'

Habilitar “EnableRemoteCommands=1”.

Em seguida configurar no Zabbix Server o item a ser monitorando usando a chave 'zm.status' configurando posteriormente a trigger e ações de recuperação.
