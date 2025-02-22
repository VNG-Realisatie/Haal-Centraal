---
layout: landing-page
title: Productvisie Haal Centraal
---

# Transitieplan

## In dit hoofdstuk lees je hoe je de transitie maakt naar het werken met Haal Centraal API’s in jouw gemeente en het uitfaseren van administratieve gegevensmagazijnen en veel lokale kopieën.  
{:.header}

&nbsp;  
## Lees eerst de Startgids Haal Centraal
{:.header}
Dit stappenplan is onderdeel van de Startgids Haal Centraal. In de startgids adviseren we om op 2 sporen te starten met Haal Centraal. Het stappenplan is een uitwerking van spoor 2 uit de startgids. Lees eerst [de Startgids Haal Centraal](https://vng-realisatie.github.io/Haal-Centraal/starten-met-haal-centraal) als je die nog niet gelezen hebt.

&nbsp;   

## Stap 1 -  Maak een transitieplan  
{:.header}
De transitie begint met het bepalen van de transitiestrategie voor jouw gemeente. Wij onderscheiden 2 strategieën, die eventueel in combinatie kunnen worden toegepast:  
* Strategie A - het actief uitfaseren van het administratief gegevensmagazijn. In deze strategie sluit je alle afnemers van het gegevensmagazijn actief aan op de API’s binnen een korte periode. 
* Strategie B - een sterfhuisconstructie, waarbij je een nieuwe infrastructuur naast de oude opbouwt en de oude situatie onveranderd laat totdat deze applicaties allemaal opnieuw zijn aanbesteed.

Welke van de twee strategieën je kiest, hangt af van de situatie in jouw gemeente en de kosten die je moet maken. Vergelijk de kosten van strategie A en B en probeer hierin een optimum te vinden. Breng in kaart:

* jaarlijkse kosten voor beheer en onderhoud van het administratief gegevensmagazijn;
* hoeveel afnemers zijn er op aangesloten;
* wanneer de aangesloten applicaties aan vervanging toe zijn;
* wat de kosten en mogelijkheden zijn voor een afnemende applicatie om naar naar API’s te migreren, al dan niet met een ‘vertaler’.

&nbsp;   

## Stap 2 – gefaseerd security opschalen  
{:.header}
Als je meer API’s gaat aansluiten, ga je ook de security opschalen. Concreet beweeg je van alle security in de applicatie naar security in centrale gemeentelijke voorzieningen. 

De professionalisering van beveiliging gaat in fases. Als je start met 1 privacygevoelige API, heb je alleen een API gateway nodig. Ga je opschalen? Dan volgt ook een proxy voor autorisatie, een Identity Provider, een protocolleringsvoorziening en IGA-systeem (Identity Governance and Administration - voorheen IAM).

In het onderstaande kader staan 3 fases beschreven voor het opschalen van de security. Hoe je de fases doorloopt, hangt samen met de transitiestrategie die je kiest.  
* Kies je voor actief uitfaseren (strategie A): dan kun je de onderstaande fases a, b en c doorlopen.
* Kies je voor een sterfhuisconstructie (strategie B), dan moet je eerst de voorzieningen uit de onderstaande fase a en b aanschaffen en inrichten. Daarna kun je de fases doorlopen.

&nbsp;   

## 3 fases voor opschalen security
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

### Fase a: afnemers gegevensmagazijn aansluiten op API’s
{:.landingpage-header}

Haal Centraal maakt aansluiten goedkoper en vermindert het aantal lokale kopieën, te beginnen bij het gegevensmagazijn/distributiesysteem. Wil je deze besparing op korte termijn inboeken? Dan moet je alle afnemers van het administratieve gegevensmagazijn aansluiten op de API’s, ook de legacy applicaties.  
{:.landingpage-header}

Totdat je opnieuw aanbesteedt, kun je voor deze applicaties een machine to machine koppeling maken (met een passende autorisatie), en eventueel een ‘vertaler’ gebruiken die de API requests en responses omzetten in de oude formaten. Gebruikersbeheer, autorisatie en logging op gebruikersniveau blijft dan onveranderd. Zij blijven onderdeel van de legacy applicatie.  
{:.landingpage-header}

Om deze stap te kunnen zetten heb je alleen een API Gateway nodig en een proxy voor autorisatie op detailniveau (evt. via een API Gateway framework). Met deze voorziening(en) kun je dus al van start met de transitie.
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

### Fase b: identity provider en logging & protocollering
{:.landingpage-header}

De tweede fase is het introduceren van een Identity provider/STS, en tegelijkertijd een start maken met een centrale logging- en protocolleringsvoorziening. 
Het juiste moment hiervoor is:
{:.landingpage-header}

* Als je een applicatie opnieuw gaat aanbesteden die past in de Common Ground visie
{:.landingpage-header}

* Als je een moderne SaaS oplossing gaat gebruiken die gebruik maakt van Haal Centraal API’s, bijvoorbeeld een generieke viewer voor alle medewerkers van de gemeente. 
{:.landingpage-header}

Begin met het aansluiten van 1 applicatie, en breid dit langzaam uit voor alle nieuwe (opnieuw aanbestede) applicaties. Zo kun je al doende leren en verbeteren, en jouw organisatie in eigen tempo verder professionaliseren.
{:.landingpage-header}

Lees meer over logging & protocollering in [het onderdeel security](https://vng-realisatie.github.io/Haal-Centraal/security).

{:.landingpage-header}

&nbsp;   
{:.landingpage-header}

### Fase c: IGA-systeem voor beheer rollen en rechten 
{:.landingpage-header}

De derde fase is het centraal beheren van rollen en rechten in een IGA-systeem (Identity Governance and Administration - voorheen IAM). 
{:.landingpage-header}

Dat wordt belangrijker naarmate het landschap meer applicaties bevat die gebruikmaken van rollen en rechten in een Identity Provider. Daarbij speelt ook de grootte van jouw gemeente een rol.
{:.landingpage-header}

Stel jezelf de vraag wanneer de provisioning van jouw Identity Provider niet meer goed lukt via een formulier of een beheerder. Bij hoeveel aangesloten applicaties en bij welke aangesloten applicaties is het belangrijk dat de Identity Provider is aangesloten op het medewerker life cycle management van jouw organisatie?
{:.landingpage-header}

Houd er rekening mee dat een IGA project 30% techniek, en 70% cultuur is. Begrip van de noodzaak en draagvlak van management en HR afdeling is een absolute voorwaarde voor succes. Start daarmee op tijd.
{:.landingpage-header}

Lees meer over IGA-systemen in [het onderdeel security](https://vng-realisatie.github.io/Haal-Centraal/security).
{:.landingpage-header}

&nbsp;   
{:.landingpage-header}
