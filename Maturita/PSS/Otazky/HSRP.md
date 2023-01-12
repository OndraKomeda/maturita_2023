Celá maturitní otázka:
HSRP, principy, funkce, použití, konfigurace

# Table of contents
- [[#Co je FHRP?]]
- [[#Co je HSRP?]]
	- [[#Kroky HSRP]]

## Co je FHRP?
FHRP je skupina protokolů, která slouží pro redundanci default gateway. 

## Co je HSRP?
HSRP je FHRP pouze cisca.

### Kroky HSRP
Vytvoří se jeden virtuální router a jeho virtuální ip bude sloužit jako default gateway.
Jeden ze switchů se rozhodne jako standby a jeden forwarding.
Forwarding posílá standby routerům hello message. Ve chvíli ale kdy prestane, tak se jeden standby router stává forwarding.
