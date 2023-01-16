# Table of contents
- [[#Celá maturitní otázka]]
- [[#K čemu se tyto protokoly používají?]]
	- [[#IMAP]]
	- [[#SMTP]]
- [[#Kroky IMAP a SMTP]]
- Příklad packet tracer zapojení v Maturita/PSS/Packet tracer konfigurace/SMTP.pkt

# Celá maturitní otázka
IMAP, SMTP - princip odesílání pošty, synchronizace poštovních schránek se serverem

# K čemu se tyto protokoly používají?
Jsou to protokoly 7., tedy aplikační, vrstvy. 

## IMAP
Tento protokol slouží k získání zpráv ze serveru.
Pamatovat si podle I - ingress.

## SMTP
Tento protokol slouží k poslání zpráv na server.
Pamatovat si podle S - send.

# Kroky IMAP a SMTP
Jsou stejné, akorát jiný protokol a IMAP komunikuje pouze s osobním serverem. Jiný nepotřebuje.
Příklad bude na zapojení v obrázku.
![[Pasted image 20230116171815.png]]
Odesílatel PC0 z admin@admin.com na student@student.com
1. TCP mezi PC0
2. SMTP admin.com
3. SMTP zpět
4. @admin.com pomocí dns přeloží student.com na ip adresu
5. TCP s admin.com a student.com
6. SMTP student.com
7. SMTP zpět