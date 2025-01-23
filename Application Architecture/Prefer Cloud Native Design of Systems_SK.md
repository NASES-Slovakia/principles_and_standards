| Názov | Prefer Cloud Native Design of Systems |
|-|-|
| Dátum schválenia | 17.07.2024 |
| Kategória | Princíp |


# Vyhlásenie

Navrhovať a vyvíjať systémy pomocou princípov cloud-native dizajnu na zabezpečenie škálovateľnosti, odolnosti a agility.

# Dôvod

- **Škálovateľnosť**: Architektúry cloud-native sú prirodzene navrhnuté na horizontálne škálovanie, čím efektívne spĺňajú požiadavky.
- **Odolnosť**: Využívanie cloud-native vzorov, ako sú mikroslužby a distribuované systémy, zvyšuje toleranciu voči chybám a odolnosť systémov.
- **Agilita**: Cloud-native dizajn podporuje rýchly vývoj, nasadzovanie a iteráciu aplikácií v súlade s DevOps a CI/CD praktikami.
- **Efektívnosť nákladov**: Modely „platba za použitie“ a elastické škálovanie znižujú náklady na infraštruktúru prispôsobením zdrojov aktuálnym požiadavkám.
- **Prenosnosť**: Cloud-native aplikácie sú často navrhnuté tak, aby boli nezávislé od platformy, čo zvyšuje flexibilitu pri výbere poskytovateľov cloudu.

# Dôsledky

## Architektúra
- Prijímať mikroslužby, serverless computing a ďalšie cloud-native architektúry.
- Navrhovať systémy tak, aby boli podľa možnosti bezstavové a využívali cloudové služby na správu stavu.

## Vývoj
- Prijať praktiky, ako sú CI/CD, automatizované testovanie a kontinuálne monitorovanie, na podporu rýchlych cyklov vývoja a nasadzovania.

## Zručnosti
- Investovať do školení vývojových a prevádzkových tímov v oblasti cloud-native technológií a praktík.

## Bezpečnosť
- Implementovať bezpečnostné najlepšie praktiky pre cloudové prostredia vrátane správy identity a prístupu, šifrovania a súladu s relevantnými normami.

## Infraštuktúra
- Využívať spravované cloudové služby na potreby infraštruktúry a zabezpečiť praktiky infraštruktúry ako kód (IaC) pre reprodukovateľnosť a automatizáciu.

## Neutralita voči dodávateľom
- Navrhovať systémy tak, aby sa predišlo závislosti na jednom dodávateľovi (vendor lock-in) použitím otvorených štandardov a zabezpečením prenosnosti medzi rôznymi cloudovými platformami, ak je to možné.

# Príklady implementácií

- **Architektúra mikroslužieb**: Rozdelenie monolitických aplikácií na mikroslužby, ktoré môžu byť nezávisle nasadzované a škálované.
- **Serverless computing**: Používanie serverless rámcov na budovanie aplikácií, ktoré sa automaticky škálujú na základe dopytu a znižujú náklady na správu serverov.
- **Kontajnery a Kubernetes**: Nasadzovanie aplikácií pomocou kontajnerov, ktoré sú riadené Kubernetes na efektívne škálovanie a spravovanie.
- **Cloud-native databázy**: Využívanie cloud-native databáz a dátových služieb, ktoré poskytujú vysokú dostupnosť, škálovateľnosť a spravované operácie.
