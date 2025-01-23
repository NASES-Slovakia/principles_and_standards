| Názov | Software design based on 12factor.net |
|-|-|
| Dátum schválenia | 15.01.2025 |
| Kategória | Princíp |


# Definícia

Všetky služby navrhnuté organizáciou NASES alebo pre NASES by mali byť navrhnuté v súlade s manifestom „12 Factor Apps“.

# Účel

Zabezpečiť vysokokvalitný a udržateľný dizajn aplikácií.

# Rozsah

Tento štandard sa vzťahuje na všetok softvér vytvorený na mieru, ktorý vlastní organizácia.

Softvérové produkty z pultu, ktoré porušujú dizajn „12 Factor Apps“, by sa mali vylúčiť.

# Dôvod

Manifest „12 Factor Apps“ je dobre známy súbor najlepších praktík v odvetví softvérového vývoja a dizajnu.

Je to metodológia nezávislá od platformy a technológie, ktorá je použiteľná na väčšinu softvérových projektov v rámci NASES.

# Požiadavky

Podrobná technická špecifikácia projektu by mala obsahovať vysvetlenie, ako je každý faktor riešený.

# Súlad

Všetky projektové požiadavky by mali obsahovať odkaz na manifest „12 Factor“.

Projektové špecifikácie, ktoré neobsahujú informácie o tom, ako sú faktory riešené, alebo priamo navrhujú dizajny porušujúce manifest „12 Factor Apps“, by mali byť zamietnuté.

# Faktory manifestu 12 Factor Apps

## I. Zdrojový kód
Jeden kódový základ sledovaný v systéme správy verzií, mnoho nasadení.

## II. Závislosti
Explicitné deklarovanie a izolácia závislostí.

## III. Konfigurácia
Konfigurácia uložená v prostredí.

## IV. Podporné služby
Podporné služby zaobchádzajú ako s pripojenými zdrojmi.

## V. Zostavenie, vydanie, spustenie
Prísne oddelenie fáz zostavenia, vydania a spustenia.

## VI. Procesy
Spúšťanie aplikácie ako jedného alebo viacerých bezstavových procesov.

## VII. Väzba s portom
Export služieb prostredníctvom väzby na port.

## VIII. Súbežnosť
Škálovanie prostredníctvom modelu procesov.

## IX. Jednoduchosť ukončenia
Maximalizácia robustnosti rýchlym spustením a elegantným ukončením.

## X. Podobnosť prostredí vývoj/test/produkcia
Zachovanie podobnosti medzi vývojovým, testovacím a produkčným prostredím.

## XI. Logy
Logy spracovávané ako prúdy udalostí.

## XII. Administračné procesy
Administračné a manažérske úlohy spúšťané ako jednorazové procesy.
