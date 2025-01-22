| Názov | Preference for REST integrations |
|-|-|
| Dátum schválenia | 17.07.2024 |
| Kategória | Princíp |


# Vyhlásenie

RESTful webové služby by mali byť uprednostnené pred integráciami založenými na SOAP pre všetky nové systémové rozhrania. Existujúce SOAP integrácie by mali byť postupne nahradené RESTful službami.

# Dôvod

RESTful webové služby ponúkajú flexibilnejší, škálovateľnejší a efektívnejší prístup k systémovej integrácii v porovnaní so SOAP. REST používa štandardné HTTP metódy a podporuje rôzne formáty dát, čo ich robí jednoduchšími na použitie a širšie prijímanými. Nahradenie zastaraných SOAP integrácií RESTful službami zlepší interoperabilitu, zníži komplexnosť a zvýši výkon.

# Dôsledky

## Návrh a vývoj

- Všetky nové integrácie by mali byť navrhované a vyvíjané pomocou RESTful API.
- Vývojové tímy musia byť zdatné v princípoch návrhu a najlepších praktikách RESTful API.

## Existujúce systémy

- Musí byť vypracovaný strategický plán na postupné nahradenie existujúcich SOAP integrácií RESTful službami.
- Prechodové plány by mali obsahovať dôkladné testovanie a validáciu na zabezpečenie funkčnej rovnocennosti a integrity dát.

## Interoperabilita

- RESTful služby musia byť navrhnuté tak, aby podporovali rôzne klientské aplikácie a platformy.
- Štandardizácia dokumentácie REST API pomocou nástrojov, ako sú Swagger/OpenAPI, je nevyhnutná na zabezpečenie konzistencie a jednoduchosti použitia.

## Bezpečnosť

- RESTful služby musia dodržiavať bezpečnostné najlepšie praktiky vrátane OAuth na autentifikáciu a HTTPS na zabezpečenú komunikáciu.
- Existujúce SOAP integrácie by mali zachovávať aktuálne bezpečnostné štandardy až do ich nahradenia.

## Výkon a škálovateľnosť

- RESTful služby by mali byť optimalizované na výkon a škálovateľnosť, aby zvládali rastúce zaťaženie a poskytovali responzívnu používateľskú skúsenosť.
- Počas prechodného obdobia by mali byť zavedené monitorovacie mechanizmy a výkonnostné metriky na sledovanie efektivity RESTful aj existujúcich SOAP integrácií.

## Správa

- Zaviesť politiky správy na vynútenie preferencie RESTful integrácií a riadenie postupného vyradenia SOAP.
- Pravidelné kontroly a audity by mali byť vykonávané na zabezpečenie dodržiavania princípov a monitorovanie pokroku pri nahrádzaní starších systémov.
