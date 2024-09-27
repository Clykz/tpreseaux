# TP RESEAU 1

# I. Récolte d'informations

🌞 **Adresses IP de ta machine**



**affiche l'adresse IP que ta machine a sur sa carte réseau WiFi :**

```
- PS C:\Users\dylan> ipconfig

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::ef26:7c2d:9d91:7d2b%18
   🌞Adresse IPv4. . . . . . . . . . . . . .: 10.33.77.151
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254

```

**affiche l'adresse IP que ta machine a sur sa carte réseau ethernet**
```
PS C:\Users\dylan> ipconfig

Carte Ethernet Ethernet 2 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::bcd7:69a0:84ef:7c59%21
   🌞Adresse IPv4. . . . . . . . . . . . . .: 192.168.56.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :
````

**affiche l'adresse IP de la passerelle du réseau local**

```
PS C:\Users\dylan> ipconfig /all

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Killer(R) Wi-Fi 6E AX1690i 160MHz Wireless Network Adapter (411NGW)
   Adresse physique . . . . . . . . . . . : D4-D8-53-78-45-B0
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::ef26:7c2d:9d91:7d2b%18(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.77.151(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Bail obtenu. . . . . . . . . . . . . . : vendredi 27 septembre 2024 13:38:21
   Bail expirant. . . . . . . . . . . . . : samedi 28 septembre 2024 13:38:21
   🌞 Passerelle par défaut. . . . . . . . . : 10.33.79.254
   Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
   IAID DHCPv6 . . . . . . . . . . . : 433379411
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-2C-F9-2E-BE-98-BB-1E-1F-74-5B
   Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                       1.1.1.1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé

```

**affiche l'adresse IP du serveur DNS que connaît ton PC**

```
PS C:\Users\dylan> ipconfig /all

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Killer(R) Wi-Fi 6E AX1690i 160MHz Wireless Network Adapter (411NGW)
   Adresse physique . . . . . . . . . . . : D4-D8-53-78-45-B0
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::ef26:7c2d:9d91:7d2b%18(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.77.151(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Bail obtenu. . . . . . . . . . . . . . : vendredi 27 septembre 2024 13:38:21
   Bail expirant. . . . . . . . . . . . . : samedi 28 septembre 2024 13:38:20
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
   Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
   IAID DHCPv6 . . . . . . . . . . . : 433379411
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-2C-F9-2E-BE-98-BB-1E-1F-74-5B
   🌞Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                       1.1.1.1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé


````

**affiche l'adresse IP du serveur DHCP que connaît ton PC**

```
PS C:\Users\dylan> ipconfig /all

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Killer(R) Wi-Fi 6E AX1690i 160MHz Wireless Network Adapter (411NGW)
   Adresse physique . . . . . . . . . . . : D4-D8-53-78-45-B0
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::ef26:7c2d:9d91:7d2b%18(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.77.151(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Bail obtenu. . . . . . . . . . . . . . : vendredi 27 septembre 2024 13:38:21
   Bail expirant. . . . . . . . . . . . . : samedi 28 septembre 2024 13:38:20
   Passerelle par défaut. . . . . . . . . : 10.33.79.254
   🌞Serveur DHCP . . . . . . . . . . . . . : 10.33.79.254
   IAID DHCPv6 . . . . . . . . . . . : 433379411
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-2C-F9-2E-BE-98-BB-1E-1F-74-5B
   Serveurs DNS. . .  . . . . . . . . . . : 8.8.8.8
                                       1.1.1.1
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé


````

**BONUS : Détermine s'il y a un pare-feu actif sur ta machine**

```
PS C:\Users\dylan> Get-NetFirewallProfile | ft Name,Enabled

Name    Enabled
----    -------
Domain     True
Private    True
Public     True
````


```
Get-NetFirewallRule
```

# II. Utiliser le réseau

**🌞 Envoie un ping vers...***

**toi-même !**

```
PS C:\Users\dylan> ping 10.33.77.151

Envoi d’une requête 'Ping'  10.33.77.151 avec 32 octets de données :
Réponse de 10.33.77.151 : octets=32 temps<1ms TTL=128
Réponse de 10.33.77.151 : octets=32 temps<1ms TTL=128
Réponse de 10.33.77.151 : octets=32 temps<1ms TTL=128
Réponse de 10.33.77.151 : octets=32 temps<1ms TTL=128

Statistiques Ping pour 10.33.77.151:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    🌞Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
```
**vers l'adresse IP 127.0.0.1**

```
PS C:\Users\dylan> ping 127.0.0.1

Envoi d’une requête 'Ping'  127.0.0.1 avec 32 octets de données :
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 🌞temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128
Réponse de 127.0.0.1 : octets=32 temps<1ms TTL=128

Statistiques Ping pour 127.0.0.1:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
   🌞 Minimum = 0ms, Maximum = 0ms, Moyenne = 0ms
```
**ta passerelle**
```
PS C:\Users\dylan> ping 10.33.79.254

Envoi d’une requête 'Ping'  10.33.79.254 avec 32 octets de données :
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.
Délai d’attente de la demande dépassé.

Statistiques Ping pour 10.33.79.254:
    Paquets : envoyés = 4, reçus = 0, perdus = 4 (perte 100%)

```

**un(e) pote sur le réseau**

```
PS C:\Users\dylan> ping 10.33.66.78

Envoi d’une requête 'Ping'  10.33.66.78 avec 32 octets de données :
Réponse de 10.33.66.78 : octets=32 🌞temps=28 ms TTL=64
Réponse de 10.33.66.78 : octets=32 🌞temps=4 ms TTL=64
Réponse de 10.33.66.78 : octets=32 temps=48 ms TTL=64
Réponse de 10.33.66.78 : octets=32 temps=61 ms TTL=64

Statistiques Ping pour 10.33.66.78:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    🌞Minimum = 4ms, Maximum = 61ms, Moyenne = 35ms
```

**un site internet**

```
PS C:\Users\dylan> ping www.thinkerview.com

Envoi d’une requête 'ping' sur www.thinkerview.com [188.114.96.7] avec 32 octets de données :
Réponse de 188.114.96.7 : octets=32 temps=16 ms TTL=55
Réponse de 188.114.96.7 : octets=32 temps=16 ms TTL=55
Réponse de 188.114.96.7 : octets=32 temps=16 ms TTL=55
Réponse de 188.114.96.7 : octets=32 temps=18 ms TTL=55

Statistiques Ping pour 188.114.96.7:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    🌞Minimum = 16ms, Maximum = 18ms, Moyenne = 16ms
```

**🌞 Faire une requête DNS à la main**

```
PS C:\Users\dylan> Resolve-DnsName -Name www.wikileaks.org -Type A

Name                           Type   TTL   Section    NameHost
----                           ----   ---   -------    --------
www.wikileaks.org              CNAME  1800  Answer     wikileaks.org

Name       : wikileaks.org
QueryType  : A
TTL        : 1800
Section    : Answer
IP4Address : 80.81.248.21


Name       : wikileaks.org
QueryType  : A
TTL        : 1800
Section    : Answer
IP4Address : 51.159.197.136
```

```
PS C:\Users\dylan> Resolve-DnsName -Name www.torproject.org -Type A

Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
www.torproject.org                             A      75    Answer     204.8.99.146
www.torproject.org                             A      75    Answer     204.8.99.144
www.torproject.org                             A      75    Answer     116.202.120.166
www.torproject.org                             A      75    Answer     116.202.120.165
www.torproject.org                             A      75    Answer     95.216.163.36
```

```
PS C:\Users\dylan> Resolve-DnsName -Name www.thinkerview.com -Type A

Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
www.thinkerview.com                            A      300   Answer     172.67.189.166
www.thinkerview.com                            A      300   Answer     104.21.73.104
```

# IV. Network scanning et adresses IP

**🌞 Effectue un scan du réseau auquel tu es connecté**
```
PS C:\Users\dylan> nmap -sn -PR 10.33.64.0/20
MAC Address: 72:90:60:02:33:B5 (Unknown)
Nmap scan report for 10.33.79.254
Host is up (0.0020s latency).
MAC Address: 7C:5A:1C:D3:D8:76 (Sophos)
Nmap scan report for 10.33.77.151
Host is up.
Nmap scan report for 10.33.77.152
Host is up.
Nmap done: 4096 IP addresses (165 hosts up) scanned in 137.84 seconds
```

**🌞 Changer d'adresse IP**
```
PS C:\Users\dylan> ipconfig

Configuration IP de Windows


Carte Ethernet Ethernet 2 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::bcd7:69a0:84ef:7c59%21
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.56.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte réseau sans fil Wi-Fi 2 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi 5 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::ef26:7c2d:9d91:7d2b%18
   Adresse IPv4. . . . . . . . . . . . . .: 🌞10.33.77.151
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254

Carte réseau sans fil Wi-Fi 4 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::e4a9:7de3:38fc:b1bc%4
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.77.152
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :
```
```
PS C:\Users\dylan> ipconfig

Configuration IP de Windows


Carte Ethernet Ethernet 2 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::bcd7:69a0:84ef:7c59%21
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.56.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte réseau sans fil Wi-Fi 2 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi 5 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::ef26:7c2d:9d91:7d2b%18
   Adresse IPv4. . . . . . . . . . . . . .: 🌞10.33.79.14
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254

Carte réseau sans fil Wi-Fi 4 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::e4a9:7de3:38fc:b1bc%4
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.77.152
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :
```