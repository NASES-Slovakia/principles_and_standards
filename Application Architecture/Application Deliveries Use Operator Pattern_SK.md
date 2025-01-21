| Názov | Application Deliveries Use Operator Pattern |
|-|-|
| Dátum schválenia | 17.7.2024 |
| Kategória | Štandard |

# Definícia

Riadenie dodávok aplikácií a ich životného cyklu musí využívať vzor Operátorov na zvýšenie automatizácie, škálovateľnosti a spoľahlivosti v prostredí Kubernetes.

# Účel

Zabezpečiť, aby všetky aplikácie nasadené v rámci organizácie nasledovali jednotný prístup k operačnej automatizácii, pričom sa využívajú Kubernetes Operátory na efektívne riadenie.

# Rozsah

Tento štandard sa vzťahuje na všetky nové nasadenia aplikácií a významné aktualizácie existujúcich aplikácií v rámci organizácie, ktoré sú spravované na Kubernetes.

# Dôvod

## Automatizácia:
- Operátory automatizujú zložité operačné úlohy, čím znižujú manuálne zásahy a operačné zaťaženie.

## Škálovateľnosť:
- Efektívne riadenie nasadení aplikácií vo veľkom rozsahu, zabezpečenie konzistentných operácií naprieč prostrediami.

## Spoľahlivosť:
- Zníženie rizika ľudskej chyby a zvýšenie spoľahlivosti systémov prostredníctvom kodifikovaných najlepších praktík.

## Konzistentnosť:
- Zabezpečenie konzistentného riadenia životného cyklu aplikácií a operácií naprieč rôznymi prostrediami.

## Prispôsobenie:
- Umožnenie prispôsobeného riadenia stavových a komplexných aplikácií na splnenie špecifických požiadaviek.

# Vývoj

- Aplikácie musia byť navrhnuté na využívanie vzoru Operátorov pre úlohy riadenia životného cyklu.
- Využívanie zavedených rámcov (napr. Operator Framework, Kubebuilder) na vývoj Operátorov.

# Zručnosti

- Tímy pre vývoj a prevádzku musia byť vyškolené na tvorbu a správu Kubernetes Operátorov.

# Nástroje a rámce

- Implementovať a používať nástroje, ktoré podporujú vývoj a nasadzovanie Operátorov.
- Udržiavať a verzionovať kód Operátorov a konfigurácie pomocou praktík infraštruktúry ako kódu (IaC).

# Správa

- Zabezpečiť najlepšie praktiky a spravovanie vývoja a údržby Operátorov.
- Zabezpečiť, že Operátory sú v súlade s organizačnými bezpečnostnými, súladovými a výkonnostnými štandardmi.

# Monitorovanie a správa

- Implementovať robustné mechanizmy monitorovania a upozorňovania pre Operátory.
- Zabezpečiť, že Operátory dokážu zvládať zlyhania a poskytujú dostatočné logovanie a diagnostiku.

# Súlad

- Pravidelné audity sa budú vykonávať na zabezpečenie dodržiavania tohto štandardu.
- Nedodržiavanie musí byť zdokumentované a nápravné opatrenia by mali byť naplánované a realizované.

# Príklady implementácií

- **Správa databáz**: Operátory musia spravovať úlohy životného cyklu databáz vrátane zriadenia, škálovania a záloh.
- **Aktualizácie aplikácií**: Operátory by mali zvládať postupné aktualizácie a návraty k predošlej verzii, aby sa zabezpečila nulová doba výpadku.
- **Vlastné zdroje**: Definovať a spravovať komplexné aplikácie pomocou Custom Resource Definitions (CRDs) a zodpovedajúcich Operátorov.
- **Service Mesh**: Používať Operátory na nasadzovanie a správu Service Meshes, zabezpečenie konzistentnej konfigurácie a monitorovateľnosti.

