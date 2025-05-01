
VL10/VL20/VL30 - SW (MVL30) =ether=L3SW

VL10 PC - 10.4.10.10/24
VL20 PC - 10.4.20.10/24
VL30 PC - 10.4.30.10/24

MVL30 SW - 10.4.30.11/24

### L3 SW:
- vypnut nepotrebne porty - shutdown, no ip
- vytvori portchannel (spoji porty do jednyho) - int range f0/1 - 2 , channel-group mode on
- nastavenie etherchannelu - port-channel 1 
- nastavenie trunku - sw trunk encapsulation dot1q, switchport mode trunk, switchport trunk allowed vlan 10,20,30
- UJISTIT SE ZE SU PORTY ZAPNUTE - no shut

### VLANY:
- vytvorit vlan 10/20/30 - vlan 10/20/30
- pre kazdou vlan- int vlan 10/20/30, ip add 10.4.10/20/30.1 255.255.255.0

### SW:
- vytvorit vlan 10/20/30
- spravit vychozi nastaveni etherchannelu - channel-group 1 mode on
- spravit trunk - int port-channel 1, sw mode trunk, sw mode trunk allowed vlan 10,20,30
- defaultni gw pro mvlan30 - ip default-gateway 10.4.30.1 
- nastavit porty na access - sw mode access, sw access vlan 10,20,30
- nastavit portfast - spanning-tree portfast

## Access List
### SW:
- zalozeni access-listu: ip access-list extended pristupMNG30
- nastaveni pristupu: permit tcp 10.4.30.0 0.0.0.255 host 10.4.30.2 eq 22
- nastaveni aby se dokazali ostatni pingnout - permit icmp any any
- zabezpeceni konzole - ip domain-name pokus.cz, ip ssh version 2, crypto key generate rsa, 1024, username admin secret 1234
- zabezpeceni portu - line vty 0 15, transport input ssh

