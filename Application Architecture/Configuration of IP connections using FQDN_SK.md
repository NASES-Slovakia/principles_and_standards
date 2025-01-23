| Názov | Configuration of IP connections using FQDN |
|-|-|
| Dátum schválenia | 17.7.2024 |
| Kategória | Štandard |

# Definícia

Tento štandard vyžaduje, aby IP pripojenia boli konfigurované pomocou úplných doménových mien (FQDN) namiesto priamych IP adries, pričom konfiguračné parametre musia byť uložené v externých konfiguračných súboroch alebo parametroch namiesto toho, aby boli pevne zakódované v zdrojovom kóde.

# Účel

Zabezpečiť flexibilný, udržateľný a bezpečný prístup ku konfigurácii IP pripojení v aplikáciách pomocou FQDN a externých konfiguračných mechanizmov.

# Rozsah

Tento štandard sa vzťahuje na všetky softvérové aplikácie a služby vyvíjané, udržiavané alebo nasadzované v rámci organizácie, ktoré vyžadujú IP pripojenia.

Zahŕňa vývojové, testovacie a produkčné prostredia.

# Dôvod

- **Flexibilita a údržba**: Používanie FQDN a externých konfiguračných súborov umožňuje jednoduchšie aktualizácie a zmeny sieťových konfigurácií bez úprav zdrojového kódu.
- **Škálovateľnosť**: Uľahčuje nasadenie aplikácií v rôznych prostrediach umožnením správy špecifických konfigurácií pre jednotlivé prostredia samostatne.
- **Bezpečnosť**: Minimalizuje riziko odhalenia citlivých informácií v zdrojovom kóde uložením konfiguračných detailov v kontrolovaných externých súboroch.

# Požiadavky

- **Používanie FQDN**: Všetky IP pripojenia musia byť definované pomocou úplných doménových mien namiesto priamych IP adries.
- **Externá konfigurácia**: Konfiguračné parametre pre IP pripojenia musia byť uložené v konfiguračných súboroch alebo parametroch aplikácie, nie pevne zakódované v zdrojovom kóde.
- **Správa konfigurácií**: Konfiguračné súbory musia byť jednoducho dostupné a upraviteľné bez potreby zmien v zdrojovom kóde aplikácie. Musí byť zavedené verzionovanie konfiguračných súborov na sledovanie zmien.
- **Dokumentácia**: Musí byť poskytnutá adekvátna dokumentácia, ktorá popisuje konfiguračné parametre a ich použitie.

# Súlad

- Pravidelné audity budú vykonávané na zabezpečenie dodržiavania tohto štandardu.
- Nedodržiavanie musí byť zdokumentované a nápravné opatrenia by mali byť naplánované a realizované.


