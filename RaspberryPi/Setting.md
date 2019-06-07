# 初期設定

## ネットワーク設定

~~~
vi /etc/dhcpcd.conf
以下を追加
interface wlan0
static ip_address 192.168.0.5/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
~~~

## 外部サイトに繋がらないとき

~~~
sudo dhclient wlan0
~~~
