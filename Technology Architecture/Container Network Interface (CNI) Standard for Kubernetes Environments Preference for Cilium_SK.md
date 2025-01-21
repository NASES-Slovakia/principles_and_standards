# Definícia

Tento štandard vyžaduje preferované rozhranie Container Network Interface (CNI) pre Kubernetes prostredia nasadené v rámci organizácie. Cilium je stanovené ako preferované CNI vďaka svojej vynikajúcej výkonnosti, schopnostiam sieťovej evolúcie a pretrvávajúcej podpore zo strany spoločnosti Cisco po akvizícii Isovalent.

# Účel

Zabezpečiť vysokokvalitné, škálovateľné a bezpečné sieťové riešenie pre Kubernetes klastry v rámci organizácie štandardizáciou na jedno vysoko výkonné CNI. Cilium je preferované kvôli svojej kompatibilite s modernými sieťovými architektúrami, integrácii s Kubernetes a RedHat OpenShift a svojmu neustálemu vývoju a stabilite podporovanej odbornými znalosťami spoločnosti Cisco v oblasti sieťových technológií.

# Rozsah

Tento štandard sa vzťahuje na všetky nasadenia Kubernetes v rámci organizácie, vrátane vývojových, testovacích, stagingových a produkčných prostredí. Štandard pokrýva nové nasadenia aj aktualizácie existujúcich klastrov.

# Dôvod

## Výkon a kvalita

- Cilium je konzistentne hodnotené ako jedno z najvýkonnejších CNI pre Kubernetes prostredia, ponúkajúce nízku latenciu a vysokú priepustnosť, čo bolo demonštrované v benchmarkových štúdiách.
- Podľa ITNEXT Benchmark Results pre Kubernetes Network Plugins CNI poskytuje Cilium špičkový výkon na sieťach s priepustnosťou nad 40 Gbps.

## Akvizícia Isovalent spoločnosťou Cisco

- S Isovalent, hlavným vývojárom Cilium, teraz pod vlastníctvom Cisco, existuje zvýšená istota o dlhodobej stabilite, vývoji a integrácii Cilium s budúcimi sieťovými technológiami.
- Táto strategická akvizícia je v súlade so silnými stránkami spoločnosti Cisco v oblasti sieťových riešení a zabezpečuje kompatibilitu s ďalšími generáciami architektúr.

## Integrácia s RedHat OpenShift

- Podľa blogu Isovalent o nasadení Red Hat OpenShift s Cilium sa Cilium môže bezproblémovo integrovať s RedHat OpenShift, čo posilňuje jeho pozíciu ako preferovaného CNI pre podnikové nasadenia Kubernetes.

## Škálovateľnosť a bezpečnosť

- Použitie eBPF (extended Berkeley Packet Filter) v Cilium poskytuje pokročilé sieťové, pozorovacie a bezpečnostné funkcie, ktoré spĺňajú požiadavky moderných Kubernetes nasadení vo veľkom rozsahu.
- Schopnosť implementovať bezpečnostné politiky na úrovni jadra umožňuje vysokú úroveň kontroly a viditeľnosti.

# Požiadavky

## Preferované CNI - Cilium

- Cilium musí byť použité ako rozhranie Container Network Interface pre všetky nasadenia Kubernetes. Akékoľvek odchýlky musia byť výslovne schválené a sprevádzané komplexným odôvodnením.

## Sieťový výkon

- Cilium musí byť nakonfigurované tak, aby využívalo vysoko výkonné funkcie na maximalizáciu priepustnosti siete a minimalizáciu latencie.

## Kompatibilita a integrácia

- CNI musí byť kompatibilné so všetkými hlavnými distribúciami Kubernetes používanými v organizácii, vrátane RedHat OpenShift, ako bolo preukázané úspešnými integráciami.
- CNI musí podporovať bezproblémovú integráciu s Cisco sieťovou infraštruktúrou, čím sa zabezpečí kompatibilita s existujúcimi on-premises, hybridnými a multi-cloud prostrediami.

## Prevádzkové riadenie a pozorovanie

- Nativné pozorovacie funkcie Cilium musia byť povolené na poskytovanie hlbokej viditeľnosti do sieťových tokov, vynucovania politík a výkonnostných metrík.
- Použitie nástroja Hubble, pozorovacieho komponentu Cilium, je povinné na podporu monitorovania, sledovania a auditovania sieťovej prevádzky v Kubernetes klastroch.

## Bezpečnostné politiky

- Bezpečnostné politiky Cilium musia byť využité na vynútenie jemne zrnitého riadenia siete v Kubernetes klastroch.
- Politiky by mali využívať schopnosti eBPF na efektívne vynucovanie na úrovni jadra bez ovplyvnenia výkonu aplikácie.

## Škálovateľnosť

- Cilium musí byť nasadené tak, aby podporovalo požiadavky na škálovateľnosť veľkých Kubernetes prostredí, najmä tých, ktoré zahŕňajú multi-cloud alebo hybridné nasadenia.
- Musí byť implementované automatizované nasadzovanie a konfigurácia, aby sa zabezpečilo, že nasadenia Cilium sú v súlade s rastovými a škálovacími stratégiami organizácie.

## Podpora a údržba

- Vzhľadom na podporu Cisco musia byť nasadenia Cilium podporované komerčnou SLA na zabezpečenie vysokej dostupnosti a rýchleho riešenia problémov.
- Organizácia musí udržiavať aktuálne verzie Cilium, aby mohla využívať najnovšie zlepšenia výkonu, bezpečnosti a kompatibility.

# Súlad

## Audity

- Pravidelné audity budú vykonávané na zabezpečenie, že Cilium je nasadené a nakonfigurované podľa tohto štandardu. Audity overia správne používanie pozorovacích nástrojov Cilium, implementáciu bezpečnostných politík a súlad so škálovateľnými požiadavkami.

## Nedodržiavanie

- Akékoľvek odchýlky od tohto štandardu musia byť zdokumentované a musia byť implementované nápravné opatrenia. Nedodržiavanie vyžaduje formálne schválenie a musí byť podporené hodnotením rizika a alternatívnym plánom.

# Dokumentácia

## Podrobnosti o nasadení

- Všetky nasadenia Cilium musia byť zdokumentované, vrátane nastavení integrácie, konfigurácií a pozorovaných výkonnostných metrík.

## Prevádzkové pokyny

- Musia byť poskytnuté komplexné prevádzkové postupy pokrývajúce inštaláciu, konfiguráciu, monitorovanie a riešenie problémov v sietiach založených na Cilium.
