# TP5 : Un ptit LAN à nous

# I. Setup

**client1**
``````
[root@client1 ~]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:e7:b9:f4 brd ff:ff:ff:ff:ff:ff
    inet 10.5.1.11/24 brd 10.5.1.255 scope global noprefixroute enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fee7:b9f4/64 scope link
       valid_lft forever preferred_lft forever
``````

**client2**

``````
[root@Client2 ~]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:a0:0f:b0 brd ff:ff:ff:ff:ff:ff
    inet 10.5.1.12/24 brd 10.5.1.255 scope global noprefixroute enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fea0:fb0/64 scope link
       valid_lft forever preferred_lft forever
``````

**routeur**
`````
[root@routeur ~]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:a0:0f:b0 brd ff:ff:ff:ff:ff:ff
    inet 10.5.1.254/24 brd 10.5.1.255 scope global noprefixroute enp0s3
       valid_lft forever preferred_lft forever
    inet6 fe80::a00:27ff:fea0:fb0/64 scope link dadfailed tentative
       valid_lft forever preferred_lft forever
3: enp0s8: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:58:3b:49 brd ff:ff:ff:ff:ff:ff
    inet 10.0.3.15/24 brd 10.0.3.255 scope global dynamic noprefixroute enp0s8
       valid_lft 85541sec preferred_lft 85541sec
    inet6 fe80::fddc:473b:cf18:2bfc/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
``````

**Tout les pings de mon pc vers mes Vms**

````
PS C:\Users\dylan> ping 10.5.1.11

Envoi d’une requête 'Ping'  10.5.1.11 avec 32 octets de données :
Réponse de 10.5.1.11 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.11 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.11 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.11 : octets=32 temps<1ms TTL=64

Statistiques Ping pour 10.5.1.11:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
PS C:\Users\dylan> ping 10.5.1.12

Envoi d’une requête 'Ping'  10.5.1.12 avec 32 octets de données :
Réponse de 10.5.1.12 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.12 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.12 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.12 : octets=32 temps<1ms TTL=64

Statistiques Ping pour 10.5.1.12:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
PS C:\Users\dylan> 10.5.1.254
PS C:\Users\dylan> ping 10.5.1.254

Envoi d’une requête 'Ping'  10.5.1.254 avec 32 octets de données :
Réponse de 10.5.1.254 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.254 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.254 : octets=32 temps<1ms TTL=64
Réponse de 10.5.1.254 : octets=32 temps<1ms TTL=64

Statistiques Ping pour 10.5.1.254:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
````
# Accès Internet pour tous

# 1. Accès internet routeur
* ☀️ Déjà, prouvez que le routeur a un accès internet
````
[root@routeur ~]# ping www.ynov.com
PING www.ynov.com (172.67.74.226) 56(84) bytes of data.
64 bytes from 172.67.74.226 (172.67.74.226): icmp_seq=1 ttl=47 time=79.4 ms
64 bytes from 172.67.74.226 (172.67.74.226): icmp_seq=2 ttl=47 time=47.1 ms
64 bytes from 172.67.74.226 (172.67.74.226): icmp_seq=3 ttl=47 time=79.9 ms
``````
* ☀️ Activez le routage
`````
[root@routeur ~]# sudo firewall-cmd --add-masquerade --permanent
success
[root@routeur ~]# sudo firewall-cmd --reload
success
``````

# 2. Accès internet clients

* ☀️ Prouvez que les clients ont un accès internet
`````
[root@client1 ~]# ping www.ynov.com
PING www.ynov.com (104.26.10.233) 56(84) bytes of data.
64 bytes from 104.26.10.233 (104.26.10.233): icmp_seq=1 ttl=46 time=35.8 ms
64 bytes from 104.26.10.233 (104.26.10.233): icmp_seq=2 ttl=46 time=42.4 ms
``````

````
[root@Client2 ~]# ping 1.1.1.1
PING 1.1.1.1 (1.1.1.1) 56(84) bytes of data.
64 bytes from 1.1.1.1: icmp_seq=1 ttl=46 time=714 ms
64 bytes from 1.1.1.1: icmp_seq=2 ttl=46 time=51.5 ms
````
☀️ Montrez-moi le contenu final du fichier de configuration de l'interface réseau
````
[root@Client2 ~]# cat /etc/sysconfig/network-scripts/ifcfg-enp0s3
DEVICE=enp0s3
NAME=lan1

ONBOOT=yes
BOOTPROTO=static

IPADDR=10.5.1.12
NETMASK=255.255.255.0
GATEWAY=10.5.1.254
DNS1=1.1.1.1
````
# III. Serveur SSH
* ☀️ Sur routeur.tp5.b1, déterminer sur quel port écoute le serveur SSH
````
[root@routeur ~]# sudo ss -lnpt | grep 22
LISTEN 0      128          0.0.0.0:22        0.0.0.0:*    users:(("sshd",pid=710,fd=3))
LISTEN 0      128             [::]:22           [::]:*    users:(("sshd",pid=710,fd=4))
``````
* ☀️ Sur routeur.tp5.b1, vérifier que ce port est bien ouvert

````
[root@routeur ~]# sudo ss -npt
State        Recv-Q        Send-Q               Local Address:Port               Peer Address:Port        Process
ESTAB        0             76                      10.5.1.254:22                     10.5.1.1:30329        users:(("sshd",pid=1286,fd=4),("sshd",pid=1272,fd=4))
`````
# IV. Serveur DHCP

# A. Installation et configuration du serveur DHCP

* ☀️ Installez et configurez un serveur DHCP sur la machine routeur.tp5.b1

J'ai d'abord installer le package dhcp
````
[root@routeur ~]# dnf -y install dhcp-server
````

Je vais modifier la conf 
````
[root@routeur ~]# nano /etc/dhcp/dhcpd.conf
````
````
[root@routeur ~]# cat /etc/dhcp/dhcpd.conf
# DHCP Server Configuration 10.5.1.0

# specify DNS server's hostname or IP address
option domain-name-servers     1.1.1.1;

# this DHCP server to be declared valid
authoritative;

# specify network address and subnetmask
subnet 10.5.1.0 netmask 255.255.255.0 {
    # specify the range of lease IP address
    range dynamic-bootp 10.5.1.137 10.5.1.237;
    # specify broadcast address
    option broadcast-address 10.5.0.255;
    # specify gateway
    option routers 10.5.1.254;
}
`````
# B. Test avec un nouveau client

* ☀️ Créez une nouvelle machine client client3.tp5.b1

* Sélection d'addresse ip par le serveur dhcp 
`````
[root@client3 ~]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:22:3b:2f brd ff:ff:ff:ff:ff:ff
    inet ☀️10.5.1.138/24 brd 10.5.1.255 scope global dynamic noprefixroute enp0s3
       valid_lft 38147sec preferred_lft 38147sec
    inet6 fe80::a00:27ff:fe22:3b2f/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
``````
* Acces a internet

`````
[root@client3 ~]# ping 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=113 time=17.9 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=113 time=17.0 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=113 time=17.0 ms
^C
--- 8.8.8.8 ping statistics ---
3 packets transmitted, 3 received, 0% packet loss, time 2005ms
rtt min/avg/max/mdev = 17.008/17.320/17.933/0.433 ms
```````
* Puis on active pour qu'il se lance au démarrage et on le démarre
````
[root@client3 ~]# systemctl enable --now dhcpd
````
# C. Consulter le bail DHCP

* ☀️ Consultez le bail DHCP qui a été créé pour notre client
````
[root@routeur ~]# cat /var/lib/dhcpd/dhcpd.leases
# The format of this file is documented in the dhcpd.leases(5) manual page.
# This lease file was written by isc-dhcp-4.4.2b1

# authoring-byte-order entry is generated, DO NOT DELETE
authoring-byte-order little-endian;

lease 10.5.1.137 {
  starts 2 2024/10/15 15:32:21;
  ends 3 2024/10/16 03:32:21;
  tstp 3 2024/10/16 03:32:21;
  cltt 2 2024/10/15 15:32:21;
  binding state active;
  next binding state free;
  rewind binding state free;
  hardware ethernet 08:00:27:a0:0f:b0;
  uid "\001\010\000'\240\017\260";
}
lease ☀️10.5.1.138 {
  starts 2 2024/10/15 15:53:53;
  ends 3 2024/10/16 03:53:53;
  tstp 3 2024/10/16 03:53:53;
  cltt 2 2024/10/15 15:53:53;
  binding state active;
  next binding state free;
  rewind binding state free;
  hardware ethernet ☀️08:00:27:22:3b:2f;
  uid "\001\010\000'\";/";
}
server-duid "\000\001\000\001.\241D7\010\000'X;I";
````
☀️ Confirmez qu'il s'agit bien de la bonne adresse MAC
`````
[root@client3 ~]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether ☀️08:00:27:22:3b:2f brd ff:ff:ff:ff:ff:ff
    inet 10.5.1.138/24 brd 10.5.1.255 scope global dynamic noprefixroute enp0s3
       valid_lft 37853sec preferred_lft 37853sec
    inet6 fe80::a00:27ff:fe22:3b2f/64 scope link noprefixroute
       valid_lft forever preferred_lft forever
``````