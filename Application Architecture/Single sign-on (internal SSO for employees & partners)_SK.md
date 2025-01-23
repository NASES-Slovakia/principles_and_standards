| Názov | Single sign-on (internal SSO for employees & partners) |
|-|-|
| Dátum schválenia | 15.01.2025 |
| Kategória | Štandard |


# Definícia

Všetky interné nástroje používané organizáciou, ktoré vyžadujú autentifikáciu, musia, ak je to možné, používať SSO. Preferovaný je OpenID Connect.

Všetky nástroje by mali mať lokálny administrátorský účet, ktorý umožňuje rekonfiguráciu nástroja v prípade zlyhania poskytovateľa identity.

# Účel

Zabezpečiť flexibilný, udržateľný, replikovateľný a bezpečný prístup používateľov.

# Rozsah

Tento štandard sa vzťahuje na všetky nasadené nástroje v rámci organizácie, ktoré vyžadujú autentifikáciu používateľov.

Zahŕňa vývojové, testovacie a produkčné prostredia.

# Dôvod

SSO zlepšuje bezpečnosť a štandardizáciu v správe používateľov, ako aj samotnú autentifikáciu.

# Požiadavky

- Na zachovanie tejto štandardizácie by mala všetka autentifikácia v integrovaných nástrojoch byť vykonávaná pomocou SSO.
- Na umožnenie núdzového obnovenia konfigurácie musia mať všetky nástroje lokálne administrátorské účty na správu nástrojov, ktoré umožňujú rekonfiguráciu nástroja v prípade zlyhania pripojenia k poskytovateľovi identity.

# Súlad

- Pravidelné audity budú vykonávané na zabezpečenie dodržiavania tohto štandardu.
- Všetky účty nástrojov, ktoré neexistujú u poskytovateľa identity, musia byť zdokumentované. Rovnako musia byť naplánované a realizované nápravné opatrenia.
