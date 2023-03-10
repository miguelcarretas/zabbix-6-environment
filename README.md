# zabbix-6-environment

:information_source: This proyect allow to run zabbix-server, mysql-server (two instances), zabbix-nginx-web, zabbix-java-gateway, zabbix-proxy, inlfuxdb and telegraf containers

:fire: If not exists, create the following directories, become `root`:

```bash
mkdir -p /etc/localtime
mkdir -p /etc/timezone
mkdir -p /usr/share/zabbix/modules
mkdir -p /opt/etc/ssl/nginx
mkdir -p /usr/lib/zabbix/alertscripts
mkdir -p /usr/lib/zabbix/externalscripts
mkdir -p /var/lib/zabbix/export
mkdir -p /var/lib/zabbix/modules
mkdir -p /var/lib/zabbix/enc
mkdir -p /var/lib/zabbix/ssh_keys
mkdir -p /var/lib/zabbix/mibs
mkdir -p /var/lib/zabbix/snmptraps
mkdir -p /opt/mysql2/lib
mkdir -p /opt/mysql2/conf
mkdir -p /var/lib/mysql
mkdir -p /opt/mysql/conf
mkdir -p /etc/ssl/certs
mkdir -p /opt/grafana/var/lib/
mkdir -p /opt/grafana/var/log
mkdir -p /opt/grafana/etc/grafana
mkdir -p /opt/influxdb/var
mkdir -p /opt/influxdb/etc
mkdir -p /opt/telegraf/etc/
mkdir -p /opt/telegraf/etc/hosts
mkdir -p /opt/nginx/ssl
mkdir -p /opt/nginx/http.d/
```

Download `telegraf.conf` file and replace with your vCenter's values and connections string.

Add your own SSL certifacates into `/opt/nginx/ssl/` path (.crt and .key files):

```
lab.local.crt
lab.local.key
```

After create these directories, run docker compose:

```bash
docker compose -f docker-compose.yml up -d
```


