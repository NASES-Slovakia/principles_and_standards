| Názov | Infrastructure as code (IaC) |
|-|-|
| Dátum schválenia | 15.1.2025 |
| Kategória | Štandard |


# Definícia

Tento štandard vyžaduje, aby všetky infraštruktúrne zdroje boli spravované pomocou Infraštuktúry ako Kód (IaC). Pre IaC sa používa ekosystém Terraform / OpenTofu.

# Účel

Zabezpečiť flexibilný, udržateľný, replikovateľný a bezpečný prístup k správe infraštruktúrnych zdrojov.

# Rozsah

Tento štandard sa vzťahuje na všetku nasadenú infraštruktúru v rámci organizácie, ktorá vyžaduje stavovú konfiguráciu.

Bude zavedený postupne, aby sa zabezpečila plynulá integrácia do existujúcich procesov a infraštruktúry. Zavádzanie do existujúcich projektov bude prebiehať postupne, podľa projektov alebo typov zdrojov.

Zahŕňa testovacie aj produkčné prostredia.

Všetky novo zavedené projekty musia implementovať všetky relevantné zdroje v IaC podľa aktuálneho stavu implementácie IaC v NASES.

# Dôvod

IaC prináša replikovateľnosť prostredí a zlepšuje bezpečnosť umožnením kontrol peer review a automatizovaných testov.

Iba výhradné používanie IaC môže zaručiť správnu konzistenciu prostredí, bezpečnosť a umožňuje skutočnú replikáciu alebo rekonštrukciu prostredia, ak je to potrebné. Akékoľvek manuálne zásahy obchádzajúce IaC narúšajú tieto záruky.

# Požiadavky

- Všetky zdroje v definovaných prostrediach by mali byť nasadené iba pomocou IaC.
- Manuálne zásahy do infraštruktúry sú povolené iba v núdzových situáciách a všetky zmeny by mali byť začlenené do IaC kódu čo najskôr po vyriešení núdze.
- Vybrať technológie, ktoré môžu byť správne nasadené pomocou IaC.
- Dodržiavať správny vývojový proces aj pri vývoji IaC.
- Parametrizovať IaC kód tak, aby bol znovu použiteľný a neobsahoval žiadne tajomstvá.

# Súlad

- Pravidelné audity budú vykonávané na zabezpečenie dodržiavania tohto štandardu.
- Všetky zdroje, ktoré neexistujú v IaC, musia byť zdokumentované a musia byť naplánované a realizované nápravné opatrenia.




