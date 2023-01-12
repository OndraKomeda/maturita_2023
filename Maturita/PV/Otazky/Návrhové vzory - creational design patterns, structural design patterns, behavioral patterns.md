## Materials.
[https://refactoring.guru](https://refactoring.guru)
[https://www.youtube.com/watch?v=tv-_1er1mWI](https://www.youtube.com/watch?v=tv-_1er1mWI)

# Table of contents.  
- [[#What are design patterns?]]
- [[#Creational patterns]]
	- [[#Singleton]]
	- [[#Factory]]
	- [[#Builder]]
	- [[#Prototype]]
- [[#Structured patterns]]
	- [[#Facade]]
- [[#Behavioral patterns]]
	- [[#Iterator]]
	- [[#Mediator]]
	- [[#Observer]]

## What are design patterns?
Návrhové vzory neboli design patterns jsou řešení pro často objevující se problém v objektovém programování. Narozdíl od algoritmu, což je seskupení instrukcí pro vyřešení problému jsou vzory spíse jako blueprint. Je to nápad jak vyřešit určitý problém, ale implementace je na vás, kód narozdíl od algoritmu vždy bude jiný.

Tyto vzory se potom dále dělí do tří skupin:

---
## Creational patterns
Zaměřuje se na problémy spojené s tím, jak jsou objekty vytvářené.

### Singleton
V jazycích, kde můžeme používat i jiný způsob programování než objektový jako třeba c++, tak v nich singleton je dokonce neoptimální, stačí vše napsat v interfaceu. Slouží ale k tomu, kdybychom chtěli mít pouze jednu instanci classy. Kdybychom takovou věc chtěli ? Třeba pro nastavení. Chceme data mít nějak seskupené v jednom celku, ale více nastavění třeba u hry nedává smysl.

### Prototype
clonene objekt(objekt je instance classy) a uloze se do sebe. Když constructor treba zatěžuje procesor. Runtime inheritance.

### Builder
Misto nastavovani vsech stavu v konstruktoru, muzeme vytvořit metody na treba add_roof (muzeme pouzit method chaining, kdyz metoda vrati sebe, tak muzeme na jednom radku zavolat nekolik metod)

### Factory
Priklad: mame vytvorit tlacitko pro ios nebo android. misto toho, ať furt děláme if statement jestli zarizeni je na ios nebo android udelame subclass nebo funkci, ktera bude mít if v sobě.

---
## Structured patterns

Zaměřuje se na spojení objektů nebo na jejich navázání. Mezitím co jsou furt flexibilní a optimální.

### Facade
Vytvoří lehký interface pro složitou classu se kterou uzivatel nepotrebuje pracovat. Zase pro jazyk jako třeba c++, kde nemusíme používat jenom classy by šlo prostě vytvořit funkce samy o sobě navázané na danou classu.

Priklad objednavka pres telefon.

---
## Behavioral patterns
Zaměřuje se na efektivní komunikaci mezi classama.  

### Iterator
Umožňuje iteraci přes kolekce. Muzeme delat jake chceme, treba preskakovat sude cisla.

### Observer
one to many relation ship. Jedna classa ktera sdeluje informace ostatním.

### Mediator
Je to jedna entita přes kterou ostatní komunikují. Jako třeba facebook je observer a my jsme ti co pres facebook komunikují.

### State
Meneni tela metod podle stateu. vytvori state pro kazdy state a overridne metody.