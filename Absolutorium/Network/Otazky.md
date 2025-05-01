# 4
## Wire
### Metal
- elektricky 0/1
- Coaxial - Tenky - Tlusty
	- tenky na anteny do televize, opleten pro interferenci, max 200 m, 10 mb/s
- TP  
	- UTP 
	- STP 
	- SFTP

### Optic
- Multi Mode
	- umoznuje propoustet vice frekvenci svetla (ruzne barvy) - vic informaci pro jeden kabel
- Single Mode
	-  uzsi jadro nez multi-mode kabel, jeden paprsek
- 100 km nejdelsi tahani - zesilovace poskytuji delsi dodani dat
## Wireless
- BT (Bluetooth)
	- 802.15 (standart)
		- 10ky metru dosah
		- 1 Mb/s prenos
- Wifi
	- 802.11 (standart)
		- 2,4 GHz
		- 5 GHz
		- 6 GHz
	- 802.11a a 802.11b (wifi 2 a wifi 1 oznaceni)
	- 802.11g - s rychlosti a-cka
	- 802.11n - 2,4 ghz a 5ghz (600/600, 300/600)
	- 802.11ac - 5ghz (1 gb)
	- 802.11ax - wifi 6 - 2,4 ghz, 5ghz, 6ghz (5 gb)
	- 802.11bn - wifi 7 - 2,4 ghz, 5ghz, 6ghz (10 gb )
- LORNA
	-  specialni sit pro IoT zarizeni
- Cellular (Data)
	- 1 - 5 G generace
	- FUP - fair user policy od operatora 
- IRDA (infrared)
	-  Ovladace k telce
- Star Link
	-  satelitni 
- NFC
	- nabije civku v zarizeni a tim to posle data


Domaci smlouva na internet - muzou slibovat minimalni internet a kdyz je vypadek tak musime cekat kym se to vyresi
- Agregovana linka - linka ktera neni jenom nasa ale je na ni vicero domacnosti

Firma smlouva - slibujou vyssi stabilitu a maximalni pocet hodin vypadku
- dedikovana linka - linka ktera patri primo jen pro tu firmu a nikdo na ni nikto jinej neni
- cenna je o hodne vyssi - i v 10 000-ich

# 6
Unicast - jeden posila jenemu - 1:1
Multicast - jeden posila skupine - 1:1N
Broadcast - jeden posila do site vsem - 1:N

half-duplex - zarizeni nedokazou vysilat i prijmat zaroven ale jenom vysilat nebo prijimat 
- Coaxialni kabely - jeden vodic 
- Sbernicova topologie - naslouchali zarizeni jestli tam 

full-duplex - zarizeni dokazou i prijmat i vysilat zaroven

# 7
Ramec 
Preambule - Mac Dest. - Mac Src. - Typ ramce - L3 Data - Kontrol soucet (CRC)

Preambule - udava zacatek ramce 
Mac Dest. - Macovka konecneho uzivatela
Mac Src. - Macovka zacatecniho uzivatela - sendra
Typ ramce - Oznaceni podle prenosoveho media
L3 Data - Packat - data z L3 (zapouzdreni)
Kontrolni soucet - kontrola provedena binarnim souctem

CAN tabulka
- na switchi
- cislo fyzickeho portu
- macovka

Etherchannel
- vytvari redundanci na L1 a L2
- rozlozeni zateze

# 9 
Funkce operacniho systemu siti
- routerOS
- IOS
- pomaha menezovat sitove zarizeni a pokrocilejsi nastaveni

Struktura a komponenty
- porty (fastethernet, gigabit, optika, AUX, USB, flash-port)
- signalizacni diody
- tlacika na prepinani modu
- zapinaci a vypinaci tlacitko na zdroji

- ROM pamet
- Flash pamet
- CPU
- RAM
- NVRAM

- POST - test hardware-u
- inicializace flash pameti - prohleda jej obsah - najde OS a inicializuje ho (OS s nejvyssi verzi/nazvem)
- koukne se do NVRAM a nacte start-up config
- provede start-up config - prekopiruje se do RAM pokud mame running config

# 10
Sitova vrstva

Packet
- nespojeny - nenavazuji spojeni po ceste
- nespolehlivy - jenom koncovy zarizeni resi zda li prisli vsechny / nemaj omezenou velikost (MTU)
- nezavisly - je jedno zda li prijde pres wifi nebo kabel - nemeni se mu hlavicka

Routovani = hledani nejlepsi cesty z host site do destination site pres routovaci tabulky

Router
- propojuje site

Routovaci tabulka
- site (na interface nebo vzdalenou)
- cilovou sit
- port
- masku site
- next-hop

# 12
Adresace v IP

Dekadicky zapis
Musi mit masku
Maska rozdeluje na:
- Sitova cast - identifikator site
- Uzivatelska cast - identifikator uzivatele v siti

IP i Maska ma 32-bitu po 8 bitech

A - E tridy sit

A - od 0.0.0.0 do 127.255.255.255
B - od 128.0.0.0 do 191.255.255.255 
C - od 192.0.0.0 do 223.255.255.255
D - od 224.0.0.0 - 239.255.255.255 - multicast - ip televize
E - 240.0.0.0 - 255.255.255.255 

Rozdeleni podle binarni podoby

ICMP - Internet Controller Message Protocol
- ping  ip adresa

Traceroute
 - posle packet s TTL - 1 a pak packet zemre na tom hopu a routr mu odosle kde umrel. Nadale to posle s TTL - 1+1

# 15
Three-way handshake

Client posle Sync. packet -> Server posle Sync. + Ack. packet -> client posle na server Ack. packet -> vytvori sa pripojenie 

Transportni vrstva
- zapouzdreni
- segmentace dat

UDP - DNS, DHCP
TCP - SSH, FTP, TELNET...

TCP - segmenty
UDP - datagramy

Multiplexing - 

Demultiplexing - 

# 16 
Na co je rozdelni site (podsite)
- zlepsuji efektivitu a mensi site znizuji potrebni vykon procesoru

172.32.65.165 /23

adresa site: 172.32.64.0
broadcast site: 172.32.65.255
maska: 255.255.254.0

0 - 255 /27


256/8 = 

2 4 8 16 32 64 128

# 17
Rozdil mezi OSI a TCP/IP 
 - Prezentacni
	 - Kodovani, sifrovani, desifrovani
	
 - Relacni
	 - Obnovi relaci, zacne relaci, ukonci relaci
	 
 - Aplikacni
	 - Resi rozhrani (GUI, CLI)

# 18
Bezpecnost pocitacovych siti

OSI
Aplikacni - Nastaveni hesel, Autentikace, Deep packet inspection
Prezentacni
Relacni
Transport
Sitova - Firewall, Cisco whitelist - resime IP adresy
Linkova - Port security, Whitelist
Fyzicka - Elektronicky zamek, biometricky

Utoky z lokalni vs verejne

Lokalni - NMap, password spoofing, DoS, IDoS, 

Vir - robi cinnost bez vedomi uzivatele (pridavani, odobrani programu, snizuje vykon pocitace, obtezovani uzivatele)

# 20
Smerovac 
- aktivni hardwarovy prvek ktery nam umoznuje komunikaci mezi sitema
- musi mit nejmene 2 porty
- musi mit aspon zapnuty porty (defaultne vypnuty), nastavene IP
- 

Routovaci tabulka
- zaznamy do dalsi site - kam ma skocit dal, adr. cilve site,  maska cil site
- musi obsahovat implicitku 

Metrika
- vypocitava kudy posle packety - nejnizsi soucet AV je lepsi

Administrativni vzdalenost
- spusoby jak routovat ma jiny admin. vzdalenosti

Implicitka
- nulova adresa 
- kdyz router nenajde cilovou sit packetu tak ho posle implicitkou - povoluje hocijaku sit

# 21 
- Hello world

# 22
Moderni trendy v pocitacovych sitich
- BOD - bring your own device
	- zamestnanci si sami prinesou svoje zarizeni
	-  pripojujou se wifinou na radius server - server pro autentikaci (prihlasujeme se na svuj profil)
	- filtrace provozu
	- omezenej az zadnej pristup do skolnich serveru
	- 
- IoT
	-  minimalizacni komunikacni zarizeni
		- wearables - prstinky, hodinky, RayBan Meta, VisionPro
		- chytra domacnost
	- nebezpecne - nedostatek zabezpeceni
- Cloud
	- sluzba ktora pouziva cizi hardware
	- Vyuziti:
		- Sluzby:
			- Azure
			- AWS
		- WPS:
		- Site:
			- Merak
- Powerline networking
	- vedeni internetu pomocou medenych vodicov pomocou 2 krabiciek v jednom okruhu
	- idealne tam kde sa nemoze vrtat (najem)
	- zhazuje rychlost o 20% - 30%
- komunikacni nastroje pro spolupraci
	- msteams - socialni sit/forum
	- github - platforma pro git verzovaci system
	- instamessaging

# 23
DHCP
- Client musi mat nastavene dynamicke IP
- Pripojeny kabel
Vyjednavanie dhcp
-  DHCP discover -> DHCP Offer -> DHCP Request -> DHCP Acknowledge

- ip adresa sa viaze na MAC adresu

DHCP na ruznych platformach
DHCP na cisco
- DHCP pool + maska
- Gateway
- DNS

DHCP Relay
- relay dovoluje klientum mimo site DHCP Serveru ziskat adresu
- relay zabali L2 do packetu a da mu destination IP serveru a zdrojovku (port)

DHCP na mikro
- Vytvori se pool ktery obsahuje cely rozsah site a pak odsud excludujeme site co nema pouzivat

DHCP IP by nikdy nemali byt na Serveroch, NAS, Tiskarny

Nebezpeci
- DHCP starvation
- DoS
- Man in the middle 

### DNS
- preklada domeny na IP
- Rekurzivni - vyhledava podle domeny
- Nerekurzivni - nevyhledava - ma natvrdo nastavene

Typy zaznamu
- Ackove - domena a IPv4
- AAAA -  IPv6 a domena
- Cname - alias (nemusime davat www. pred domenu)
- Mx zaznam - 
- NS - autoritaritvni server ktery nam rekne kde nadem domenu
- Txt - retezce co se vrati kdyz kontaktujeme server

Urovni domeny
 - .com, .cz
 - podle zeme(.eu, .hr, .sk, .cz)
 - generic (.gov, .mil, .com)
 - ridi to celkove trinact root servru po svete ktere spravuji domeny prvniho radu (pro cesko NIC.cz)