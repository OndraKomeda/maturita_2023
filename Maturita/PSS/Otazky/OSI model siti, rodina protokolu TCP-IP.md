# Table of contents
- [[#TCP-IP model]]
- [[#OSI model]]
	- [[#Kroky komunikace]]
- [[#OSI vs TCP-IP]]

# TCP-IP model
1. Network interface 
2. Network - Přidání headeru
3. Transport - Komunikace pomocí [[UDP a TCP]].
4. Application - Tato vrstva se v OSI modelu dělí na
	1. Session - Z části zbyt
	2. Presentation - Tato vrstva má za úkol zašifrovat a zkomprimovat data z aplikační vrsvty OSI modelu.
	3. Application - Data přímo z aplikace. (Formát dat určuje aplikační protokol např. SSH nebo SMTP)

# OSI model
Layers
1. Physical 
	Slouží na přenášení bitů pomocí rúzných fyzických médií jako třeba impulsama elekřiny v drátu, světlem v optic kabelech nebo dokonce i elektromagnetickéma frekvencema.
	Devices: Coax cable, cross-over cable, WAP, HUB
2. Data link
	Vytvoří z bitů frame podle nějakého standartu. Nejčastěji je to Ethernet.
	Devices: Switch
3. Network
	Slouží k mezisíťové komunikaci pomocí packetu. Určuje next-hop pomocí routing tableu.
	Devices: Router, Layer 3 switch
4. Transport
	IP určuje jak data rozdělit do více packetů, ale aby se dostali ve správném pořadí k adresátovi, tak je potřeba kontrolovat jejich pořadí a jestli packet byl správně přijatý, to dělá [[UDP a TCP]]
5. Session
	Přidá data o session do metadata packetu. Slouží pro vytvoření nebo ukončení session. Session není potřeba pro jeden packet, ale když je jich více, tak je užitečný.
6. Presentation
	Tato vrstva je odpovědná za přeložení dat na formát ať jim aplikační vrstva rozumí pomočí šifrování a komprese.
	SSL, TLS, JPG
7. Application
	Data z aplikací jako například SSH nebo SMTP.

## Kroky komunikace
1. data z aplikace
2. data jsou zašifrována a zkomprimována.
3. data jsou
4. L4 header + =||= 
5. L3 header + =||=
6. L2 header + =||= + L2 trailer

# OSI vs TCP-IP
![[Pasted image 20230117102122.png]]

