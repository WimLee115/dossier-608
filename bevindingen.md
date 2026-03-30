---
layout: default
title: "Bevindingen — Gedeelde servers, e-mail en gecoördineerde wijzigingen"
description: "Technisch bewijs: bewindvoerderskantoren delen IP-adressen, e-mailsystemen en softwareplatforms. Na één klacht verdwenen meer dan 70 pagina's bij 14 kantoren."
keywords: "gedeelde infrastructuur bewindvoerder, IP-adres bewindvoering, SPF-records, websitewijzigingen, gecoördineerd, bewindvoeringssector"
---

# Bevindingen

Onderstaande bevindingen zijn gebaseerd op publiek toegankelijke technische gegevens (DNS, WHOIS, SPF-records) en de openbare websites van de betrokken kantoren.

## 1. Gedeelde technische infrastructuur

### Gedeelde serveradressen

Meerdere kantoren delen serveradressen. Dit is vastgesteld via openbare DNS-lookups (dig-commando naar publieke DNS-resolvers).

| Cluster | Kantoren | Bijzonderheid |
|---------|----------|---------------|
| IP-cluster A | Almass Bewindvoering + een gelieerd kantoor | **Opeenvolgende IP-adressen** (.41 en .42) bij dezelfde hostingprovider |
| IP-cluster B | Twee kantoren | Zelfde IP-adres |
| IP-cluster C | De franchiseorganisatie + het ondersteuningsbedrijf | Zelfde IP-adres |

<p class="bron">DNS A-records (publiek opvraagbaar, geraadpleegd maart 2026)</p>

Het feit dat Almass Bewindvoering en een gelieerd kantoor op **opeenvolgende IP-adressen** staan bij dezelfde hostingprovider duidt op een gezamenlijk bestelde hostingomgeving.

### Gedeelde e-mailsystemen

Uit de openbare SPF-records (DNS TXT-records) blijkt dat meerdere kantoren dezelfde e-mailsystemen gebruiken. SPF-records zijn publiek opvraagbaar en geven aan welke mailservers gemachtigd zijn om e-mail te versturen namens een domein.

| Systeem | Kantoren die het gebruiken |
|---------|---------------------------|
| Bewindvoerderssoftware A | Almass Bewindvoering + de franchiseorganisatie |
| Bewindvoerderssoftware B | Twee andere kantoren |
| Boekhoudplatform | Een kantoor |

<p class="bron">DNS TXT-records / SPF (publiek opvraagbaar, geraadpleegd maart 2026)</p>

### Domeinredirect

Het persoonlijke domein van een gevolmachtigde van Almass Bewindvoering verwijst automatisch door naar de website van Almass. Dit is vastgesteld via een standaard HTTP-request.

<p class="bron">HTTP redirect-keten (publiek toegankelijk, geraadpleegd maart 2026)</p>

## 2. Websitewijzigingen na de sommatie

Na de sommatie van 4 maart 2026 aan Almass Bewindvoering zijn bij **alle veertien onderzochte kantoren** websitewijzigingen vastgesteld. De sommatie was gericht aan één kantoor; de overige dertien werden niet in de sommatie genoemd.

### Verwijderde pagina's

In totaal zijn **meer dan 70 webpagina's** verwijderd of offline gehaald. De verwijderingen betreffen:

| Type pagina | Aantal kantoren | Toelichting |
|-------------|-----------------|-------------|
| Medewerkerspagina's | 11 van 14 | Overzichten met namen en functies van medewerkers |
| Klachtenprocedures | Meerdere | Klachtenprocedure is wettelijk vereist voor bewindvoerders |
| Privacy-/AVG-beleid | Meerdere | Privacyverklaring conform de AVG |
| Tariefpagina's | Meerdere | Overzicht van kosten voor cliënten |

<p class="bron">Monitoring openbare websites, maart 2026</p>

### Gelijktijdige wijzigingen

Op **20 maart 2026** bleken bij zeven kantoren gelijktijdig 27 webpagina's offline te zijn gehaald. De pagina's retourneerden allemaal HTTP 404 ("niet gevonden") bij de eerste controle op die datum.

Dat zeven onafhankelijke organisaties op dezelfde dag dezelfde typen pagina's offline halen — medewerkersoverzichten, klachtenprocedures, tarieven — is een opvallende samenloop.

<p class="bron">Monitoring openbare websites met tijdstempels, 20 maart 2026</p>

### Navigatiewijzigingen

Op 30 maart 2026 verwijderde de franchiseorganisatie de menu-items "Franchiseformule", "Mijn [naam]" en "Ledenportaal" uit de publieke navigatie van haar website. De onderliggende pagina's zijn nog bereikbaar via directe URL's, maar niet meer vindbaar voor bezoekers die de site via het menu doorbladeren.

Het verbergen van de franchisestructuur vermindert de zichtbaarheid van het feit dat meerdere kantoren onder dezelfde organisatie opereren.

<p class="bron">Monitoring openbare website, 30 maart 2026</p>

## 3. Domeinmigraties

In het weekend van 29–30 maart 2026 zijn meerdere domeinwijzigingen vastgesteld:

**Branchevereniging.** Het oude domein van de branchevereniging is niet meer geregistreerd (DNS-status: NXDOMAIN). Een nieuw domein is geactiveerd. Uit de WordPress-metadata van het nieuwe domein blijkt dat de website ten minste **16 maanden in voorbereiding** was — de eerste content dateert van november 2024.

De activering van het nieuwe domein volgde op het starten van een onderzoek door het Landelijk Kwaliteitsbureau CBM (26 maart) en een mediapakket aan 14 organisaties (26 maart).

**Eén kantoor.** Een kantoor heeft zijn website gemigreerd naar een nieuw domein met een volledig herontworpen website. Het oude domein is niet meer geregistreerd. De footer van de nieuwe website bevat een werkende link naar een specifieke ledenpagina op het nieuwe domein van de branchevereniging — wat erop duidt dat beide migraties vooraf waren afgestemd.

**Vijf secundaire domeinen** van andere kantoren zijn eveneens niet meer geregistreerd. De primaire websites van deze kantoren zijn nog bereikbaar op hun hoofddomein.

<p class="bron">DNS-query en WHOIS (publiek toegankelijk, 30 maart 2026)</p>

## 4. Aflopende domeinregistraties

Twee domeinen die direct gelieerd zijn aan Almass Bewindvoering verlopen binnenkort:

| Domein | Verloopdatum | Relatie |
|--------|-------------|---------|
| Persoonlijk domein gevolmachtigde | 10 april 2026 | Verwijst door naar Almass-website |
| Hoofddomein Almass | 14 mei 2026 | Primaire website Almass Bewindvoering |

<p class="bron">WHOIS (publiek toegankelijk, geraadpleegd 30 maart 2026)</p>

<div class="noot" markdown="1">
**Methodologische noot.** De monitoring betreft uitsluitend publiek toegankelijke webpagina's. Er is geen gebruik gemaakt van inloggegevens, beveiligde omgevingen, of technieken om beveiligingsmaatregelen te omzeilen. Alle metingen zijn geborgd met SHA-256 hashes en onafhankelijke tijdstempels (OpenTimestamps). Zie ook: [bronverantwoording](bronnen) en [hoe de kantoren verbonden zijn](netwerk).
</div>
