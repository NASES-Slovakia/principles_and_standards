| Name | DevSecOps Guideline |
|-|-|
| Approval date | 6.2.2025 |
| Category | Odporúčanie |

# Development

Všetky zdrojové kódy musia byť uložené v GitLab repozitári v čitateľnej
a prehľadnej forme a v anglickom jazyku. V prípade krabicového softvéru,
ktorý je distribuovaný binárne, je potrebné container dodať image do
príslušného container registry v GitLabe. Rovnakoje potrebné dodať
Kubernetes Operator alebo Helm chart s príslušnou dokumentáciou.

Zmeny musia dodržiavať štandardný git trunk-based workflow zahŕňajúci
feature branches a merge requests do master vetvy.

Master vetva je chránená.

Merge feature branchov do mastra je možný iba pomocou merge-requestu a
master a nie je možné force-pushovať.

Všetky časti kódu musia mať určených code-owners.

Hlavná vetva master/main je automaticky nasadzovaná do testovacieho
prostredia pri každom commite.

Commity musia byť ucelené ale primerane veľké s vhodnou commit message,
ktorá stručne popisuje zmeny a odkazuje sa na issue v issue trackeri.

Merge request obsahuje odkaz na problém a prípadne popis na doplnkové
zdôvodnenie zmien, ak je to potrebné.

Pri práci s gitom dodržiavame postup, ktorý generuje lineárnu git
históriu:

-   Všetky merge-requesty musia byť rebasnuté na najnovší commit base
    branche pred mergom.

-   Používame rebase na update feautre branch a vyriešenie konfliktov.
    Nemergujeme base branch do feature branch.

-   Merge-requesty sa merguju merge-commitom.

# Code review

Každá zmena kódu musí prejsť cez code-review v rámci merge requestu
aspoň 1 reviewerom.

Jednotlivé časti a typy zdrojových kódov musia mať definovaných svojich
vlastníkov cez „CODEOWNERS". Každý typ, resp. každá časť musí mať
skupinu vlastníkov min. dvoch osôb, pre účely zastupiteľnosti.

Pri code review sa posudzuje správnosť a úplnosť zmien, dodržiavanie
všetkých pravidiel a zásad, kvalita kódu atď. Taktiež sa posudzujú
reporty zo skenovacích zariadení o kvalite kódu ako testovacie pokrytie,
alebo stav zraniteľností v závislostiach.

Nedostatky reviewer okomentuje priamo v merge-requeste a developer ich
zapracuje pridaním commitov do merge-requestuNapokom znovu vyžiada v
GitLabe opakovanú review.

Po schválení maintainer alebo developer môže squashnúť commity pred
mergom bez ďalších úprav.\
Pokiaľ je potrebný rebase kvôli riešeniu konfliktu je postup na dohode medzi
developerom a reviewerom.

# CI/CD

Každý projekt musí mať funkčné CI/CD na buildovanie a testovanie,
vrátane všetkých potrebných typov testov podľa požiadaviek. Výstupy
buildu -- packages, images, reporty a podobne, musia byť uložené do
relevantných registrov v rámci GitLab repozitára.

Dodávateľ je zodpovedný za dodanie:

-   CI pipeline prebuild a vykonanie testov modulu,

-   CI pipeline pre vytvorenie a podpísanie container image,

-   kubernetes operátor alebo helm chart pre nasadenie do kubernetes
    klastra,

-   konfiguráciu nasadenia pre helm/operátor pre definované prostredia,

-   terraform šablónu na aktualizáciu infraštruktúry,

-   dokumentáciu závislostí, parametrov a popis nasadenia do všetkých
    prostredí.

Pri CD sa počíta s nasadzovaním pomocou ArgoCD. Utajované
skutočnosti/tajomstvá sa ukladajú do Hashicorp Vault. Infraštruktúra je
riadená pomocou terraform skriptov.

Releasy musia byť označené tagom a určením verzie, podľa metodiky
SemVer: <https://semver.org/>.

Aplikácie musia byť distribuované vo forme Docker image. Docker image má
byť výsledkombuildu v GitLab CI.

# Zabezpečenie

Docker image musí byť „hardened" - musí byť postavený na oficiálnom
minimalistickom base image pre konkrétnu technológiu. Docker image musí
obsahovať iba runtime závislosti, nesmie obsahovať build-time
závislosti. Očakáva sa použitie multi-stage Docker buildu.

Jeden docker image musí obsahovať iba jednu službu.

Image musia spĺňať odporúčania:

-   [CIS Docker
    Benchmark](https://www.cisecurity.org/benchmark/docker/),

-   [[NIST SP
    800-190](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-190.pdf)](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-190.pdf),

-   [[OWASP Docker Security Cheat
    Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html)](https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html).

Požiadavky na dodané komponenty v kuberentes prostredí:

-   network segmentation -- Network policy, Default deny,

-   secure configuration -- secrets v HashiCorp Vault,

-   access control - Admission Controllers, ServiceAccount,

-   resource limits pre kontainery,

# Observability 

Použitý framework: [OpenTelemerty](https://opentelemetry.io).

Zberané dáta:

-   logy - centralizované spracovanie logov s kontainerov, auditné logy,

-   metriky -- Prometheus, RED metrics ,USE metrics,

-   trace -- Jaeger, distributed trace, service mesh.

Každý proces služby musí obsahovať koncový bod pre zistenie stavu služby
pre integráciu na monitoring.

Každý pod v kuberenetes prostredí obsahuje Liveness, Readiness, Startup
probe.

Logy musia byť zapisované do STDOUT alebo STDERR docker imagu. Formát
logov musí by konfigurovateľný.

# Dokumentácia 

Dokumentácia musí byť súčasťou repozitára v textovom formáte, ktorý vie
GitLab zobrazovať - preferuje sa Markdown alebo AsciiDoc.

# Prostredie

Aplikácia bude bežať v Oracle PCA v OKE klastri, perspektívne možno v
RedHat Openshift. Na nasadenie sa používa ArgoCD.

Rozdelenie prostredí podľa účelu:

-   vývojové,

-   testovacie,

-   UAT,

-   produkčné.

Produkčný klaster bude oddelené od testovacích a vývojových
v samostatnom produkčnom prostredí.

# Testovanie

Testovanie je vykonávané automatizovanými testami v rámci CICD pipeline.
Očakávame dodanie kompletných GitLab CI pipelines potrebných pre
testovanie a build.

Testy sa spúšťajú automaticky pri pushnutí nových zmien do
merge-requestu v GitLabe a pri builde a nasadzovaní noveho releasu.

Testy musia bežať v GitLab CI runneri v headless režime. Runner je
určený do kontajnerov pomocou Dockeru. Výstupné reporty musia byť
čitateľné v rámci GitLab pipeline.

GitLab má aktivovanú Ultimate licenciu. Preferujeme využitie možností,
ktorétáto licencia poskytuje a prípadne doplnenie ďalších open-source
nástrojov.

Testovacie pipelines by mali zahŕňať:

- unit testy (pytest, JUnit, PHPUnit, Jasmine, Karma),

- integračné testy ([Test containers](https://testcontainers.com/),
Docker compose, [BDD Cucumber](https://cucumber.io/)),

- API testy ([Postman](https://www.postman.com/), Smartbear),

- end-to-end testy (Cypress, Selenium, Playwright),

- load testy (JMeter),

- bezpečnostné testy (GitLab Ultimate features):

SAST (GitLab Ultimate, Sonarqube, Snyk,

DAST (GitLab Ultimate, Zaproxy),

Security dependeny check (GitLab Ultimate),

Container security check (GitLab Ultimate).

Repozitáre musia mať aktivované skenovanie závislostí gitlabom a
integrovaný automatický nástroj na aktualizáciu závislostí - Dependabot
alebo Renovate.

Všetky použité závislosti musia byť na aktívne udržiavaných verziách a
na verziách s najnovšími bezpečnostnými záplatami. Ideálne na najnovších
stabilných verziách.

Rozdelenie testovacích prostredí na test kubernetes klastre bude pomocou
namespace.

## Priradenie testov pre prostredia

 
 | Prostredie            | Testy                          | Spustenie
 | --------------------- | ------------------------------ | -------------------
 | Vývojové              | Unit , SAST, Integračné        | Automatické
 | Testovacie prostredie | E2E, DAST                      | Automatické
 | Testovacie prostredie | PEN, Záťažové                  | Manuálne
 | UAT                   | UAT                            | Manuálne
 

# GitLab -- GitHub workflow

Všetky projekty majú primárny repozitár v NASES GitLabe.

Žiadny git repozitár nesmie obsahovať citlivé údaje, žiadne tokeny,
heslá, certifikáty, kľúče. Všetky takéto hodnoty musia byť
reprezentované, resp. popísane z hľadiska parametrov.

Build-time secrets musia byť uložené v GitLab Variables s primeraným
nastavením ochrany a viditeľnosti.

Run-time secrets musia byť uložené v Hashicorp Vault a referencované
pomocou súborov.

Všetky repozitáre musia obsahovať informácie o licencii „LICENSE" súbore
a základné informácie, popisy a návody v „README" s relevantnými odkazmi
do detailnej dokumentácie, ktorá sa primárne očakáva v priečinku .doc v
danom repozitári.

Repozitáre sú otvorené na čítanie pokiaľ to licencia umožňuje.

Otvorené repozitáre budú automaticky replikované do GitHubu pre lepšiu
dostupnosť za účelom auditu alebo komunitného development príspevku a
zároveň ako off-site záloha.

Prípadné verejné príspevky zatiaľ očakávame že budú manuálne prenesené
do GitLabu a zapracované udržiavateľom projektu. Ak sa časom ukáže, že
verejných príspevkov je tak veľa, že tento postup je neudržateľný, dôjde
k prehodnoteniu tohoto postupu.

# **Kubernetes Operátory**

Kubernetes operátory sú rozšírenia Kubernetes API, ktoré umožňujú
automatizáciu komplexných operácií, ako je nasadenie, škálovanie,
zálohovanie a obnova aplikácií. Operátory sú obzvlášť užitoční pre
stavové aplikácie a služby, ktoré vyžadujú špecifickú logiku správu.

## Kedy použiť Kubernetes Operátor

Operátory by mali byť zvažované v nasledujúcich prípadoch:

-   **stavové aplikácie** ak riešenie vyžaduje správu stavu (napr.
    databázy, message brokery, alebo distribuované systémy),

-   **komplexná logika nasadenia** - ak nasadenie vyžaduje špecifické
    kroky, ktoré presahujú možnosti Helm chartov alebo základných
    Kubernetes manifestov,

-   **automatizácia operácií** - ak je potrebná automatizácia operácií
    ako zálohovanie, obnova, škálovanie alebo upgrady.

## Požiadavky na Operátor

-   **Operator SDK:** Operátory by mali byť vyvíjané pomocou **Operator
    Framework** alebo **Kubebuilder**, čo sú štandardné nástroje pre
    vývoj Kubernetes operátorov.

-   **CRD (Custom Resource Definitions):** Operátor by mal definovať
    vlastné Kubernetes zdroje (CRD), ktoré popisujú konfiguráciu a stav
    aplikácie.

-   **Reconciler Loop:** Operátor by mal implementovať **reconciler
    loop**, ktorý neustále monitoruje stav systému a vykonáva potrebné
    zmeny na dosiahnutie požadovaného stavu.

-   **Testovanie:** Operátor by mal byť dôkladne testovaný, vrátane unit
    testov a integračných testov v reálnom Kubernetes prostredí.

## Príklad Použitia Operátora

-   **Databázový Operátor:** Pre stavové databázy (napr. PostgreSQL,
    MySQL) môže operátor automatizovať vytváranie, škálovanie,
    zálohovanie a obnovu.

-   **Message Broker Operátor:** Pre systémy ako Apache Kafka alebo
    RabbitMQ môže operátor spravovať klastre, témy a poradia.

-   **Vlastný Operátor:** Pre špecifické potreby riešenia môže byť
    vytvorený vlastný operátor, ktorý spravuje životný cyklus aplikácie.

## Integrácia s Helm a ArgoCD

-   **Helm:** Operátor môže byť distribuovaný ako súčasť Helm chartu,
    kde CRD a operátor sú nainštalované spolu s aplikáciou.

-   **ArgoCD:** ArgoCD môže byť použité na nasadenie a správu operátora,
    ako aj na sledovanie stavu aplikácie prostredníctvom operátora.

## Dokumentácia a Školenia

-   **Dokumentácia:** Každý operátor by mal mať podrobnú dokumentáciu,
    ktorá popisuje, ako ho nainštalovať, konfigurovať a používať.

-   **Školenia:** Tímy, ktoré budú operátor používať, by mali byť
    vyškolené v jeho používaní a údržbe.
