Skládá se z osmi skupin dělené dvojtečkou, kde každá skupina obsahuje čtyři hexadecimální znaky. Tedy 0-9 a A-F. Jeden hex charakter jsou 4 bity / půl bytu.

Druhy IPv6

![[Pasted image 20230123084535.png]]

## Unicast
Send to one address
Link-local - FE80::/10 - slouží na komunikaci po lokální síťi. Nemůžou být routované
Loopback ::1/128 - localhost
Global unicast 2000::/3
Unique local FC00::/7 - Komunikace v jedné routing domain a né po celém internetu.

## Multicast
Send to multiple address 
FF00::/8 Assigned - treba pro dhcpv6 servery nebo rip routery
Solicited Node - slouzi na NDP pro dad a slacc

## Anycast
Send to one address of multiple addresses(closest one)

## Packet
Header má 320 bitů, kde 256 bitů obsahuje destination a source adresy. Dál obsahuje verzi adresy, délku celého packetu Hop limit a dále.

## Porovnání s IPv4
Hlavní důvod, proč vzniklo IPv6 byl nedostatečný počet IPv4. Teď obsahuje 128 bitů místo 32. Oproti ipv4 nemá subnetmasku, dělí se pouze pomocí / a počet bitů
