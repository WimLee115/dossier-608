---
layout: default
title: "Bronnen — Alle gebruikte openbare bronnen"
description: "Verantwoording van alle bronnen: Handelsregister (KvK), rechtspraak.nl, DNS/WHOIS, openbare websites. Methodologie en integriteitsborging."
keywords: "bronnen onderzoek bewindvoering, handelsregister KvK, rechtspraak.nl, DNS WHOIS, openbare bronnen, OpenTimestamps"
---

# Bronnen

Alle informatie op deze website is afkomstig uit de volgende openbare bronnen.

## Handelsregister

Het Handelsregister van de Kamer van Koophandel is op grond van de [Handelsregisterwet 2007](https://wetten.overheid.nl/BWBR0021777/) openbaar toegankelijk. Er zijn uittreksels geraadpleegd van acht bedrijven die betrokken zijn bij de structuur van de onderzochte kantoren.

De uittreksels bevatten bedrijfsnaam, KvK-nummer, vestigingsadres, bestuurders, aandeelhouders, gevolmachtigden, geplaatst en gestort kapitaal, en de datum van de laatste gedeponeerde jaarrekening. Alle uittreksels zijn gearchiveerd.

## Rechtspraak

Rechterlijke uitspraken zijn openbaar gepubliceerd op [rechtspraak.nl](https://www.rechtspraak.nl/). Er zijn drie uitspraken geraadpleegd die betrekking hebben op de onderzochte kantoren:

- Ontslag bewindvoerder wegens tekortkoming in het bewind (Gerechtshof, 2025)
- Benoeming mentorschap (Rechtbank, 2026)
- Aanstelling opvolgend bewindvoerder (Rechtbank, 2025)

## DNS en WHOIS

DNS-gegevens zijn publiek opvraagbaar via het DNS-protocol. Het betreft:

- **A-records** — welk IP-adres hoort bij een domeinnaam
- **TXT-records (SPF)** — welke mailservers gemachtigd zijn voor een domein
- **NS-records** — welke nameservers een domein bedienen

De gegevens zijn geraadpleegd via vier publieke DNS-resolvers:

| Resolver | IP-adres | Beheerder |
|----------|----------|-----------|
| Google Public DNS | 8.8.8.8 | Google |
| Cloudflare DNS | 1.1.1.1 | Cloudflare |
| Quad9 DNS | 9.9.9.9 | Quad9 Foundation |
| SIDN | ns1.dns.nl | SIDN (registrar .nl-domeinen) |

WHOIS-gegevens (domeinregistratie, verloopdatum) zijn opvraagbaar via het WHOIS-protocol.

## Openbare websites

De websites van de onderzochte kantoren zijn publiek toegankelijk via het internet. Er is uitsluitend gebruik gemaakt van:

- Standaard HTTP-verzoeken aan publiek toegankelijke URL's
- De openbare broncode van webpagina's (View Source / Ctrl+U)
- Openbare WordPress-metadata (`datePublished`, `article:modified_time`)

Er is **geen** gebruik gemaakt van:

- Inloggegevens of beveiligde accounts
- Niet-openbare API's of beheerderspanelen
- Technieken om beveiligingsmaatregelen te omzeilen

## Overige openbare bronnen

| Bron | Type | Doel |
|------|------|------|
| [Belastingdienst ANBI-register](https://www.belastingdienst.nl/wps/wcm/connect/nl/aftrek-en-kortingen/content/anbi-702-background) | Publiek register | Verificatie ANBI-status gerelateerde stichtingen |
| [Wayback Machine](https://web.archive.org/) | Publiek webarchief | Historische websiteversies |
| [OpenTimestamps](https://opentimestamps.org/) | Tijdstempelprotocol | Onafhankelijke tijdstempels via Bitcoin-blockchain |

## Integriteitsborging

- Alle bronnen zijn openbaar en door derden verifieerbaar
- KvK-uittreksels zijn op het moment van raadpleging gearchiveerd
- Voor elke gecontroleerde webpagina is een SHA-256 hash vastgelegd
- Tijdstempels zijn onafhankelijk vastgelegd via OpenTimestamps
- Feitelijke onjuistheden worden op verzoek gerectificeerd (zie [rectificatiebeleid](over#rectificatie))
