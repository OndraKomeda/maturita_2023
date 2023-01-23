# Table of contents 
- [[#Obecně]]
- [[#Dedicnost]]
- [[#Method overriding]]
- [[#Function overloading]]

# Obecně
Všechny následující témata jsou možné pouze v objektovém programování. Například ikdyž nevytváříme classu u function overloading, tak i tak ji nemůžeme použít například v C, protože není objektové.

# Dedičnost
Schopnost class převzít variables a metody jiné classy se nazývá dědičnost. Private variably se dědí, ale nemůžeme je nijak accessnout. Dědí se z důvodu, aby public metody, které jsou s těmito variably spojené.

# Method overriding
Kdybychom se nám nelíbila zděděná verze metody, tak ji můžeme celou přepsat pomocí method overriding. Prostě ji "napíšeme znovu". Příklad
Classa zvíře, která ma basic metodu udelat_zvuk(), ale budeme mít psa, který by chtěl v této metodě zaštěkat, tak ji přepíšeme pro zděděnou classu psa.

# Function overloading
Slouží na vytvoření dvou a více funkcí se stejným názvem a return typem, které se liší v argumentech.

float multiply(int first, int second);
float multiply(double first, double second);