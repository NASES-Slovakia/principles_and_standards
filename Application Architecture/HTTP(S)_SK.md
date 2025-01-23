| Názov | HTTP(S) |
|-|-|
| Dátum schválenia | 15.1.2025 |
| Kategória | Štandard |

# Definícia

Všetka HTTP komunikácia by mala byť zabezpečená pomocou HTTPS. Nezabezpečená komunikácia je povolená iba na presmerovania na zabezpečené pripojenia a na účely overovania domén.

Akceptované by mali byť iba certifikáty podpísané dôveryhodnými certifikačnými autoritami (CA).

# Účel

Zabezpečiť bezpečnú komunikáciu.

# Rozsah

Tento štandard sa vzťahuje na všetky služby pracujúce s HTTP.

# Dôvod

HTTPS zaručuje bezpečnú komunikáciu iba vtedy, ak je správne overená autentickosť certifikačnej autority (CA). Pri použití vlastných certifikačných autorít (self-signed CA) je vyššie riziko vynechania overenia alebo akceptácie neplatnej CA.

LetsEncrypt poskytuje dôveryhodné certifikáty zadarmo s nástrojmi na automatizáciu, čo prináša iba minimálnu záťaž v porovnaní s nezabezpečenou komunikáciou.

# Požiadavky

- Všetky poskytovania certifikátov by mali byť automatizované.
- Expirácia certifikátov musí byť monitorovaná, pretože expirovaný certifikát povedie k nedostupnosti služby (DoS).

# Súlad

- Pravidelné audity budú vykonávané na zabezpečenie dodržiavania tohto štandardu.
- Všetky služby, ktoré tento štandard nedodržiavajú, musia byť zdokumentované a musia byť naplánované a realizované nápravné opatrenia.
