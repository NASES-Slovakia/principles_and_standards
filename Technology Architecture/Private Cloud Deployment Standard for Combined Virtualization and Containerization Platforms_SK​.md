| Názov | Containerize Before Virtualization |
|-|-|
| Dátum schválenia | 03.10.2024 |
| Kategória | Štandard |

# Definícia

Tento štandard stanovuje preferované technológie na nasadenie privátneho cloudového riešenia, ktoré podporuje virtualizáciu aj kontajnerizáciu. Primárne odporúčané riešenie je založené na RedHat OpenShift, pričom SUSE Rancher integrovaný s Longhornom je sekundárnou možnosťou, uznávajúc jeho obmedzenia v porovnaní s RedHat OpenShift.

# Účel

Zaviesť jednotný prístup k nasadzovaniu kombinovanej platformy pre virtualizáciu a kontajnerizáciu v privátnom cloude. Tým sa zabezpečí efektívne riadenie tradičných virtuálnych strojov aj kontajnerizovaných aplikácií, čím sa umožní škálovateľnosť, flexibilita a zlepšené využitie zdrojov. Cieľom je poskytnúť konzistenciu vo výbere technológií, umožňujúcu bezproblémovú integráciu a spoľahlivú prevádzku v infraštruktúre organizácie.

# Rozsah

Tento štandard sa vzťahuje na všetky projekty vyžadujúce nasadenie privátneho cloudu v rámci organizácie. Zahŕňa vývojové, testovacie a produkčné prostredia, kde je potrebná kombinovaná platforma pre virtualizáciu a kontajnerizáciu. Podporuje hybridné pracovné záťaže, vrátane tradičných aplikácií bežiacich na virtuálnych strojoch a moderných kontajnerizovaných aplikácií.

# Dôvod

## Primárna preferencia pre RedHat OpenShift

- Podľa výskumu spoločnosti Gartner (G00803119) je RedHat OpenShift vedúcou platformou na správu kontajnerov a hybridných privátnych cloudových nasadení.
- OpenShift ponúka robustné schopnosti na škálovanie v on-premises, edge a multi-cloud prostrediach a je považovaný za zrelé riešenie pre podnikové nasadenia.

## Dostupnosť zdrojov

- V Slovensku je dostupný významný počet kvalifikovaných a certifikovaných odborníkov na RedHat OpenShift, čo je výsledkom blízkosti Brna, kde má RedHat hlavné vývojové centrum.
- Táto dostupnosť miestnych odborníkov zabezpečuje rýchlejšie nasadenie, lepšiu prevádzkovú podporu a optimalizované využitie zdrojov.

## Prevádzková efektivita a vysoká dostupnosť

- RedHat OpenShift poskytuje komplexné nástroje na správu kontajnerizovaných aj virtualizovaných pracovných záťaží, ponúkajúc jednotné riadenie a vysokú mieru automatizácie.
- SUSE Rancher s Longhornom, hoci je životaschopnou alternatívou, zaostáva za OpenShift v zrelosti produktu, integrácii ekosystému a podnikových funkciách.

## Jednotná správa a škálovateľnosť

- Obidve platformy podporujú multi-cloud, edge a hybridné nasadenia, ale RedHat OpenShift má lepšie integračné schopnosti a silnejšie partnerské siete, čo poskytuje väčšiu istotu pre strategické prijatie.

# Požiadavky

## Výber technológie

- Všetky privátne cloudové nasadenia zahŕňajúce virtualizáciu a kontajnerizáciu musia primárne používať RedHat OpenShift ako predvolenú platformu.
- SUSE Rancher s Longhornom môže byť použitý len s výslovným schválením a odôvodnením, pretože je považovaný za menej zrelý a s menším počtom dostupných certifikovaných zdrojov.

## Podpora kombinovanej virtualizácie a kontajnerizácie

- Platforma musí podporovať virtuálne stroje aj kontajnerizované aplikácie integrovaným spôsobom. RedHat OpenShift je preferovaný pre svoje pokročilé funkcie na správu zmiešaných prostredí.

## Škálovateľnosť a flexibilita

- Vybraná platforma musí podporovať multi-cloud, hybridné cloudové a edge scenáre. To zahŕňa nasadenie v on-premises dátových centrách, na vzdialených lokalitách a integráciu s verejnými cloudovými službami.

## Prevádzkové riadenie

- RedHat OpenShift poskytuje centralizované nástroje na provisionovanie, monitorovanie a správu životného cyklu virtuálnych strojov aj kontajnerových pracovných záťaží.

## Vysoká dostupnosť a ochrana dát

- Platforma musí zahŕňať zabudovanú vysokú dostupnosť pre výpočtové a úložné vrstvy.
- RedHat OpenShift ponúka komplexnejšie riešenie vysokej dostupnosti a obnovy po havárii vhodné pre podnikové nasadenia.

## Podpora

- Platforma musí poskytovať komerčnú podporu, ktorá zabezpečí spoľahlivú prevádzku a rýchlu reakciu na problémy.
- Musí existovať jasná SLA pre dostupnosť a podporu, ktorá zodpovedá potrebám produkčných systémov organizácie.

## Správa a súlad

- Nasadenia musia dodržiavať definované bezpečnostné politiky a platformy musia podporovať centralizovanú správu a súlad vrátane riadenia prístupu na základe rolí, vynucovania politík a logovania.

# Súlad

## Audity

- Pravidelné audity budú vykonávané na zabezpečenie, že nasadené privátne cloudové platformy sú v súlade s týmto štandardom, pričom RedHat OpenShift je primárnym riešením.

## Nedodržiavanie

- Akékoľvek nedodržiavanie tohto štandardu musí byť zdokumentované a musia byť plánované a realizované nápravné opatrenia.

# Dokumentácia

## Detaily platformy

- Každé nasadenie musí byť zdokumentované vrátane použitej platformy, architektúry, konfigurácie vysokej dostupnosti a detailov o virtualizovaných a kontajnerizovaných pracovných záťažiach.

## Prevádzkové postupy

- Dokumentácia musí obsahovať prevádzkové postupy pre správu a škálovanie privátnej cloudovej platformy, pokrývajúc virtualizačné a kontajnerové prostredia.
