| Názov | Streaming and messaging platforms |
|-|-|
| Dátum schválenia | 06.03.2025 |
| Kategória | Štandard |

## Definícia
Hlavnou platformou pre streaming a messaging v NASES je aplikácia Apache Kafka. Ak sú potrebné špecifické messaging funkcie a náklady na prispôsobenie presahujú prijateľný rozpočet, môže sa zvážiť ako alternatíva aplikácia RabbitMQ.

## Účel
Tento štandard definuje pokyny pre streaming dát a komunikáciu medzi službami v rámci NASES.

## Rozsah
Tento štandard sa vzťahuje na všetky služby spravované inštitúciou NASES.

## Odôvodnenie
- Technologický stack by mal byť čo najjednoduchší, aby sa zabezpečila prevádzková efektívnosť.
- Apache Kafka je najrobustnejšie open-source riešenie, široko uznávané ako de facto štandard pre streaming a messaging, a už je v používaní v NASES.
- Navrhovanie aplikácií s ohľadom na obmedzenia Kafky je bežnou praxou v priemysle.
- Ak náklady na prispôsobenie aplikácie Kafka presiahnu prijateľný rozpočet, RabbitMQ sa môže zvážiť ako alternatíva.

## Požiadavky
- Všetky služby spravované inštitúciou NASES musia dodržiavať tento štandard.
- Preferencia sa dáva produktom z „off-the-shelf“ riešení, ktoré sú natívne kompatibilné s Apache Kafka.
- Vlastné softvérové riešenia používajúce alternatívne streaming platformy musia byť zamietnuté alebo upravené v súlade s týmto štandardom, pokiaľ nie je udelená schválená výnimka.

## Zhoda
- Riešenia by mali uprednostniť integráciu s Apache Kafka všade, kde je to možné.
- Akékoľvek odchýlky od tohto štandardu si vyžadujú zdôvodnený obchodný prípad a schválenie od príslušnej autority.
- Používaniu alternatívnych streaming platforiem sa musíme ako NASES vyhnúť, pokiaľ nie je explicitne schválená iná platforma.