| Názov | Security by Design |
|-|-|
| Dátum schválenia | 03.10.2024 |
| Kategória | Princíp |


# Vyhlásenie

Bezpečnosť musí byť integrovaná do celého životného cyklu návrhu, vývoja a prevádzky systémov, namiesto spoliehania sa na skrytosť ako prostriedok ochrany systémov. Každá architektonická súčasť musí byť navrhnutá s najvyššou prioritou na bezpečnosť, pričom sa kladie dôraz na stratégiu „shift left“, ktorá rieši bezpečnostné otázky už v najskorších fázach vývoja.

# Dôvod

Budovanie bezpečnosti do architektúry od samého začiatku („Security by Design“) zabezpečuje robustnú a odolnú infraštruktúru. Spoliehanie sa na tajomstvá, nedokumentované vlastnosti alebo skryté detaily na zabezpečenie („Security by Obscurity“) je nedostatočné, pretože tieto prvky môžu byť ľahko objavené útočníkmi. Proaktívnym prístupom k bezpečnosti a presunutím bezpečnostných opatrení do najskorších fáz vývoja („shift left“) môže podnik zmierniť zraniteľnosti skôr, než sa stanú rizikami, minimalizovať útokový povrch a zabezpečiť súlad s predpismi a osvedčenými postupmi. Tento princíp znižuje pravdepodobnosť kritických bezpečnostných chýb a posilňuje celkovú kybernetickú bezpečnosť organizácie.

# Dôsledky

## Skorá integrácia bezpečnosti („Shift Left“):

- Bezpečnostné požiadavky musia byť identifikované a riešené v najskorších fázach vývoja riešení a plánovania architektúry.
- Prístup „shift left“, ako odporúča CNCF, zabezpečuje, že bezpečnosť sa berie do úvahy počas zhromažďovania požiadaviek, návrhu a dokonca aj počas počiatočných fáz vývoja, namiesto čakania na fázu testovania alebo nasadenia.

## Transparentné bezpečnostné opatrenia:

- Bezpečnostné mechanizmy a kontroly musia byť transparentné a testovateľné, pričom sa spoliehajú na robustné bezpečnostné metódy namiesto tajností.
- Bezpečnostné opatrenia, ako sú šifrovanie, kontrola prístupu a auditovanie, by mali byť dobre zdokumentované a implementované podľa priemyselných štandardov.

## Obrana v hĺbke:

- Musí byť aplikovaný viacvrstvový prístup k bezpečnosti, ktorý zabezpečuje, že existuje viacero ochranných opatrení na ochranu citlivých údajov a systémov.
- Žiadna jednotlivá bezpečnostná kontrola by sa nemala považovať za dostatočnú a kľúčom k zmierneniu rizika je redundancia.

## Konzistentné bezpečnostné štandardy:

- Bežné bezpečnostné štandardy a rámce, ako sú CIS, ISO 27001 a OWASP, by mali byť dôsledne aplikované na všetky systémy.
- To znižuje pravdepodobnosť chýb a zabezpečuje konzistentný prístup k zmierňovaniu rizík.

## Testovanie a validácia bezpečnosti:

- Musia byť vykonávané pravidelné bezpečnostné kontroly, vrátane kontrol kódu, hodnotení zraniteľností a penetračných testov, aby sa overila účinnosť bezpečnostných opatrení.
- Dôraz na „shift left“ tiež znamená vykonávať automatizované bezpečnostné testovanie čo najskôr a integrovať bezpečnosť do CI/CD pipeline.
