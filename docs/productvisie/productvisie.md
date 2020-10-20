## Uitgangspunten
- Alle ingredienten van Haal Centraal API's zijn herleidbaar naar een bij de API vermeld informatie model;
- Alle code, documenten en specificaties die ontstaan in dit traject wordt Open Source gepubliceerd onder de
[EUPL licentie](https://joinup.ec.europa.eu/collection/eupl/eupl-text-11-12);
- Voor de specificatie van API's wordt [OpenAPI Specification v3.x](https://www.forumstandaardisatie.nl/standaard/openapi-specification) 
gebruikt. Deze is door Forum Standaardisatie op de
["Pas toe of leg uit"-lijst](https://www.forumstandaardisatie.nl/lijst-open-standaarden/in_lijst/verplicht-pas-toe-leg-uit)
geplaatst;
- Waar mogelijk worden de
[API strategie](https://docs.geostandaarden.nl/api/API-Strategie/) en de [REST API Design Rules](https://docs.geostandaarden.nl/api/API-Designrules/) 
toegepast.

## Realisatie
We werken zoveel mogelijk Agile. Onderstaande activiteiten zijn onderdeel van een iteratief proces.
- we maken van iedere gemeentelijke informatiebehoefte die bij ons bekend is een user story. 
- user stories worden gemapt op een een Goals Canvas, waarmee we de basisfuncties en endpoints van API specificeren. 
- Voor de meest voorkomende stories maken we een definitie in OpenAPI (en als het nodig is features voor de provider). 
- een designer van VNG Realisatie definieert de API in OpenAPI i.s.m. de PO, een domeinexpert van de landelijke registratie, een tester, en een developer van VNG Realisatie. 
- iedere definitie is getoetst op DX, waaronder code generatie door onze eigen customer zero, een developer van VNG Realisatie. 
- de (concept)definitie wordt gerealiseerd door een landelijke partij
- de definitie wordt bijgesteld op basis van vragen en opmerkingen van provider en andere stakeholders, bijvoorbeeld n.a.v. een fieldlab
- testen worden primair uitgevoerd door de landelijke registratie, maar ook door minimaal 1 gemeente. 
- (versie van) API wordt in productie genomen en beheerd door Landelijke Registratie
- onboarding via de Landelijke registratie, documentatie via Haal Centraal Github.

