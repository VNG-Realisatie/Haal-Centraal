---
layout: landing-page
title: Productvisie Haal Centraal
---

# Security en privacy 

## Als je met API’s gaat werken, heb je andere security en privacyvoorzieningen nodig dan nu. Deze set voorzieningen is een belangrijke voorwaarde voor de transitie naar API’s. Hieronder lees je hoe je de security kunt inrichten om veilig te werken met Haal Centraal API’s.
{:.header}

&nbsp;   
## Veilig gebruik van vertrouwelijke gegevens
{:.header}
De kern van veilig gebruik van een Haal Centraal API met vertrouwelijke gegevens is:
* Dat uitsluitend geautoriseerde (gebruikers van) applicaties toegang krijgen tot gegevens.
* Dat gebruikers uitsluitend toegang krijgen tot gegevens waarvoor zij zijn geautoriseerd.
* Dat een (SaaS)applicatie uitsluitend toegang krijgt tot de gegevens namens een gebruiker van jouw gemeente, dus alleen als jouw medewerker achter de knoppen zit.

&nbsp;   
## Omgeving inrichten op veilig gebruik
{:.header}
Om veilig te kunnen werken met API’s heb je 3 onderdelen nodig.
1. (Toegangs)beveiliging, autorisatie en filtering.
2. IGA-systeem: beheren van identiteit, rollen en rechten.
3. Logging- en protocollering: controle achteraf en misbruik voorkomen.

Hieronder lees je een uitwerking van deze 3 onderdelen

&nbsp;   

### 1. (Toegangs)beveiliging, autorisatie en filtering
{:.header}
Gemeenten bieden een breed palet aan producten en diensten die allemaal een andere minimale set gegevens en functionaliteit nodig hebben. En die producten en diensten worden geleverd door veel verschillende medewerkers met verschillende rollen en rechten. 

Gemeenten moeten hiervoor zelf de toegangsbeveiliging en autorisatie organiseren. Gemeenten hebben daarvoor minimaal nodig:

* Identity Provider (IP): authenticeren van de eindgebruiker.
* Security Token Service (STS): beheren van security tokens en identificeren van een client (SaaS) applicatie.
* API Gateway: (toegangs)beveiliging van de API’s.
* Proxy of een ‘facade’: autorisatie op detailniveau.

In het kader [Uitwerking (Toegangs)beveiliging, autorisatie en filtering](https://vng-realisatie.github.io/Haal-Centraal/security#uitwerking-toegangsbeveiliging-autorisatie-en-filtering) lees je een uitwerking van deze onderdelen.

&nbsp;   
### 2. IGA-systeem: beheren van identiteit, rollen en rechten
{:.header}
Bij voorkeur wordt de Identity Provider gevoed door een  IGA-systeem (Identity Governance and Administration - voorheen IAM), waarmee je de rollen en rechten van jouw gebruikers voor verschillende systemen centraal kunt beheren. 

Een IGA oplossing: 
* automatiseert bijvoorbeeld het creëren, updaten en verwijderen van accounts; 
* behandelt aanvragen van gebruikers om toegang te krijgen tot een bepaald systeem; 
* beheert wachtwoorden, gebruikerstoegang en toegangscertificeringsprocessen. 

Je kunt het IGA-systeem koppelen aan het HR systeem, zodat een medewerker bijvoorbeeld automatisch alle rechten verliest op het gebruik van BRP gegevens als hij/zij voor een andere afdeling gaat werken.

Zo’n IGA voorziening is optioneel maar heel belangrijk, zeker als je in een wat grotere gemeente werkt. Het beheren van veel gebruikers met verschillende accounts in allerlei processystemen zoals nu in veel gemeenten gebruikelijk is, is een beveiligingsrisico.

&nbsp;   
### 3. Logging- en protocollering: controle achteraf en voorkomen misbruik
{:.header}
Een gemeente moet conform de wet BRP alle BRP bevragingen protocolleren. Dat gebeurt nu meestal in de diverse procesapplicaties. Het is beter om een centrale logging- of protocolleringsvoorziening in te richten, waarin API requests en evt. ook responses onweerlegbaar worden vastgelegd, samen met het token dat de identiteit en claims van de eindgebruiker bevat. 

Door de API Gateway te laten loggen en de toegangsbeveiliging voor nieuwe applicaties te baseren op eindgebruikercredentials hoef je straks in de meeste gevallen niet meer te protocolleren in de afnemende applicatie. Ook kun je burgerverzoeken in het kader van de AVG beter en sneller afhandelen door de logginggegevens te verrijken met de informatie uit je verwerkingsregister. 

Voor het verzamelen, opslaan en analyse van de logging kun je bijvoorbeeld gebruik maken van de ELK (Elastic search, Logstash en Kibana), Stack, Splunk, LogRhythm, Graylog, etc.

&nbsp;   
------------------------------
&nbsp;   

## Uitwerking (Toegangs)beveiliging, autorisatie en filtering
{:.landingpage-header}

Gemeenten kunnen met deze onderdelen zelf de toegangsbeveiliging en autorisatie organiseren.
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

### Identity Provider (IP)	
{:.landingpage-header}

Voor het authenticeren van de eindgebruiker waarin de claims voor het gebruik van de API van alle gebruikers van jouw gemeente centraal zijn vastgelegd. 
{:.landingpage-header}

Nadat de Identity provider heeft vastgesteld wie de ingelogde gebruiker is en welke applicatie de API namens de gebruiker wil bevragen, kunnen tokens (al dan niet met gebruikersclaims) aan client applicaties worden verstrekt. 
{:.landingpage-header}

Hiermee kan de client (SaaS)applicatie namens de gebruiker de API bevragen.
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

### Security Token Service (STS)	
{:.landingpage-header}

Voor het uitgeven, valideren, vernieuwen en beëindigen van security tokens en het veilig identificeren van een client (SaaS) applicatie. Hoort bij de Identity Provider.
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

### API Gateway	
{:.landingpage-header}

Voor de (toegangs)beveiliging van de API’s. Een API Gateway is vaak onderdeel van een product voor ‘full life cycle API Management’. 
{:.landingpage-header}

Een API Gateway bevat ondersteuning voor het design, publiceren, documenteren, beveiligen en analyseren van API’s. Zie [het overzicht van Gartner](https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/f2472e2d-30f2-45d0-86a5-0734bd42ff6f.png) voor productinspiratie. 
{:.landingpage-header}

Een API Gateway is een must have voor iedere gemeente die gevoelige API’s aan afnemers aanbiedt.
{:.landingpage-header}

&nbsp;
{:.landingpage-header}
