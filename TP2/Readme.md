# TP2 RESEAU

# I. Quelques pings

🌞 **Prouvez que votre configuration est effective**

````
Get-NetIPAddress -InterfaceAlias "Ethernet"


IPAddress         : fe80::bcd7:69a0:84ef:7c59%21
InterfaceIndex    : 21
InterfaceAlias    : Ethernet
AddressFamily     : IPv6
Type              : Unicast
PrefixLength      : 64
PrefixOrigin      : WellKnown
SuffixOrigin      : Link
AddressState      : Preferred
ValidLifetime     :
PreferredLifetime :
SkipAsSource      : False
PolicyStore       : ActiveStore

IPAddress         : 10.1.1.2🌞
InterfaceIndex    : 21
InterfaceAlias    : Ethernet
AddressFamily     : IPv4
Type              : Unicast
PrefixLength      : 24
PrefixOrigin      : Manual
SuffixOrigin      : Manual
AddressState      : Preferred
ValidLifetime     :
PreferredLifetime :
SkipAsSource      : False
PolicyStore       : ActiveStore
````


🌞 **Tester que votre LAN + votre adressage IP est fonctionnel**

```
PS C:\Users\dylan> ping 10.1.1.1

Envoi d’une requête 'Ping'  10.1.1.1 avec 32 octets de données :
Réponse de 10.1.1.1 : octets=32 temps=2 ms TTL=128
Réponse de 10.1.1.1 : octets=32 temps=2 ms TTL=128
Réponse de 10.1.1.1 : octets=32 temps=2 ms TTL=128
Réponse de 10.1.1.1 : octets=32 temps=2 ms TTL=128

Statistiques Ping pour 10.1.1.1:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 2ms, Maximum = 2ms, Moyenne = 2ms
```

# II. Utilisation des ports

🌞 **Sur le PC serveur**

Dans notre terminal en admin 
````
PS C:\Users\dylan\Desktop\netcat-1.11> ./nc64.exe -l -p 9999
````


On ouvre un autre terminal 
```
PS C:\Windows\system32> netstat -a -b -n

Connexions actives
TCP    0.0.0.0:9999           0.0.0.0:0              LISTENING
 [nc64.exe]
```

🌞 **Sur le PC client**
 ````
 PS C:\Users\dylan\Desktop\netcat-1.11> ./nc 10.1.1.1 6666

````
🌞 **Echangez-vous des messages**
````
PS C:\Users\dylan\Desktop\netcat-1.11> ./nc 10.1.1.1 6666
🌞je suis la
🌞ouais
````
🌞 **Utilisez une commande qui permet de voir la connexion en cours**

**Moi serveur**
````
PS C:\Users\dylan\Desktop\netcat-1.11> netstat -an | findstr :9999
  TCP    10.1.1.2:9999          10.1.1.1:2734          ESTABLISHED

````
**Moi client**
````
PS C:\Users\dylan\Desktop\netcat-1.11> netstat -an | findstr :6666
  TCP    10.1.1.2:53518         10.1.1.1:6666          ESTABLISHED
````

# III. Analyse de vos applications usuelles



**Premiere applications (Spotify)**
````
PS C:\Users\dylan\Desktop\netcat-1.11> netstat -a -b -n
  TCP    192.168.1.10:50056     104.199.65.9:4070      ESTABLISHED
 [Spotify.exe]
 ````

 **Deuxieme applications (Riot)**

 ````
 PS C:\Users\dylan\Desktop\netcat-1.11> netstat -a -b -n
 TCP    192.168.1.10:49747     172.64.146.73:443      CLOSE_WAIT
 [RiotClientServices.exe]
 ````
**Troisieme applications (chrome)**

`````
PS C:\Users\dylan\Desktop\netcat-1.11> netstat -a -b -n
  TCP    192.168.1.10:50610     140.82.112.26:443      ESTABLISHED
 [chrome.exe]
  TCP    192.168.1.10:53799     185.199.110.154:443    ESTABLISHED
 [chrome.exe]
  TCP    192.168.1.10:53803     140.82.113.21:443      ESTABLISHED
 [chrome.exe]
 ``````

**Quatrième applications (Discord)**

`````
 TCP    192.168.1.10:62468     162.159.130.234:443    ESTABLISHED
 [Discord.exe]
  TCP    192.168.1.10:65185     162.159.130.235:443    ESTABLISHED
 [Discord.exe]

``````

**Cinquieme applications (Word)**

`````
PS C:\Users\dylan\Desktop\netcat-1.11> netstat -a -b -n
  TCP    192.168.1.10:55288     52.113.194.132:443     ESTABLISHED
 [WINWORD.EXE]
``````

