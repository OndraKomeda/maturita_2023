
# Table of contents
- [[#Proč potřebujeme DHCP4?]]
- [[#Jaké jsou kroky pro získání nebo obnovení IPv4?]]
	- [[#Vypůjčení]]
	- [[#Obnovení]]

## Proč potřebujeme DHCP4?
DHCP4 slouží pro automatické nastavení ipv4 adres v síťi.
Toto je nám užitečné, když nastavujeme velkou síť a nechceme manuálně nastavovat všechny IP adresy nebo hodně užitečné je to s používáním WAP. Místo toho aby třeba každý zákazník 
v kavárně si sám zadával IP, tak ji dostane automaticky a nemusí se o nic starat.

## Jaké jsou kroky pro získání nebo obnovení IPv4?
### Vypůjčení
1. **DHCP Discover (DHCPDISCOVER)**
Broadcast z clienta aby nasel DHCP server

2. **DHCP Offer (DHCPOFFER)**
Server posle clientovy ip adresu na vypujceni a zapise si ji do arp stolu.

3. **DHCP Request (DHCPREQUEST)**
Broadcast z clienta s informacemi přijatí, aby ostatní DHCP servery věděli.
Potom co server prijme request, tak zkusí pingnout danou ip adresu a pokud ji nikdo nepoužívá, tak pošle:

4. **DHCP Acknowledgment (DHCPACK)**
Až přijde klientovy, tak zkontroluje arp table, jestli nekdo danou adresu používá, pokud ne, tak ji začne používat jako svoji.
Klient si ale může vypůjčit ip adresu jenom na danou dobu, těsně před vypršením se klient zeptá pro obnovení.

![[Pasted image 20230112124806.png]]

### Obnovení 
1. **DHCP Request (DHCPREQUEST)**
Client pošle request danému serveru ke kterému byl připojen. Pokud mu nepřijde daný pack, tak to rozešle jako Broadcast

2. **DHCP Acknowledgment (DHCPACK)**
Server posílá jako potvrzení clientovy a vypůjčení se prodlužuje.
