Celá maturitní otázka 
Komunikace v síti - Využití UDP a TCP protokolu

# Table of contents
- [[#UDP]]
	- [[#Výpočet checksum]]
- [[#TCP]]
	- [[#TCP kroky]]

# UDP
Je to protokol 4. vrstvy transport. Kontroluje pouze korupci datagramu. K datům z aplikační vrstvy je přidán header a PDU název je Datagram. Je užitečný, když důležitá je rychlost a ne přesnost. Třeba při hrách nebo sledování videí.

Header datagramu obsahuje pouze 4 věci
Source a destination port
Datagram length - delka celeho datagramu i s daty - 2 byte
Checksum - při odesílání se vypočítá a pošle se. Adresátor si sám od sebe checksum vypočítá a porovná checksum v headru, pokud se nerovnají, tak packet je koruptovaný a adresátor packet zničí.

## Výpočet checksum
Bity v datech rozdělí do dvou-byteových částí a sečte všechny pod sebou.
Výsledek součtu je checksum.

# TCP
Je to protokol 4. vrstvy transport. Je odpovědný za spolehlivé doručení packetů ve správném pořadí. K datům z aplikační vrstvy je přidán header a PDU název je Segment. Slouží k přesnosti, protože kontroluje správné odeslání všech packetů pomocí ACK.

Header segmentu obsahuje 
Source port - destination port
Sequence number - určuje pořadí packetů.
Acknowledgement number 
ACK, SYN, FIN - boolean
a další flagy.

## TCP kroky
1. Pomocí three-way handshake domluvit komunikaci. Tyto segmenty neobsahují žádné data a následující info je uloženo v headeru. Pokud se handshake povede, tak se začnou posílat data.
	1. syn ->
	2. syn + ack <-
	3. ack ->
![[Pasted image 20230117103926.png]]
2. Poslání packetů s datami.
	Při přijmutí packetu dat musí vždy odpovědět, že data dostal pomocí ACKNOWLEDGE. Zase packet bez dat. Acknowledge number se zvětší o počet bitů, které přijmul
	![[Pasted image 20230117103912.png]]
3. Ukončení spojení
	3 way handshake akorát místo SYN se použije FIN
4. Detekce ztracených packetů
	Když odesílatel nedostane ack, tak spustí timer. Když neobdrží ACK do konce timeru tak packet odesílá znovu. Kdyby klient dostal více stejných packetů, muže je zničit.
5. Špatné pořadí packetů.
	Když přijde jiný packet než očekávaný, tak klient odešle ACK s ACKNOWLEDGE NUMBER nastaveným na poslední seq. Ale client si je často sám poskládá.
