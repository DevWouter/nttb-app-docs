---
status: work-in-progres
owner: Wouter
---

# Feature: Meerkamp
## Epic requirements
<!-- Dit zijn de eisen die we helder hebben -->
- Ondersteun meerkamp met 3 t/m 11 spelers
- Gegevens moeten in NAS gestopt kunnen worden
- Moet ook knock-out toernooi ondersteunen
- Spelers moeten automatisch ingedeeld worden op basis van algoritme
- Toernooi coordinators moeten spelers kunnen verplaatsen vooraf gaand aan het toernooi

### Epic questions
<!-- Dit zijn vragen die nog niet helder zijn -->
- **Moeten** de resultaten van de meerkampen bewaard worden in NAS? Aka: Is het mogelijk om een meerkamp buiteren het toernooi te houden?
- **Welke** externe systemen moeten we ondersteunen? En **hoe** koppelen we externe systemen? 
- Hebben alle meerkampen dezelfde weergave? Een meerkamp van 3 spelers hoeft (in theorie) niet dezelfde hoeveelheid ruimte nodig als een meerkamp van 11 spelers. *Grootste uitdaging* is de tabel weergave van de behaalde scores 
- Hoe zorgen we dat aanpassingen van schema (score, speler aanpassingen, et cetera) betrouwbaar verspreid worden aan alle devices? Wat als een device offline is? Denk hierbij aan tafels die omgewisseld worden en de persoon heeft geen internet
- Moet alles via de mobiel of is er ook een desktop website? Zeker bij grote complexe toernooien is dat handig. Niet iedereen wilt de NTTB-app installeren of heeft een device die er geschikt voor is.
- Kan een toernooi coordinator halverwege het toernooi spelers herindelen of meerkampen samenvoegen?
- Welke gegevens moeten we uit NAS halen als we zoeken op basis van NTTB?

### Epic Todo's
<!-- Dit zijn taken die helder zijn maar nog uitzoek werk nodig hebben -->
- [ ] Uitzoeken en documenteren algoritmes voor indelen enkele en meerdere meerkampen
- [ ] Uitzoeken en documenteren algoritmes voor knock-out toernooi's. Denk hier bij ook aan "seeding" en ongebalanceerde trees.

### Personages in stories
- Toernooi coordinator (ook wel "coordinator" genoemd)
- Speler
- Scheidsrechter
- Toeschouwer

## Delivery 1: Hulpmiddel voor toernooi coordinator

De eerste oplevering is bedoeld om de kleinste meerwaarde aan de app toe te voegen en beschikbaar te maken voor de gebruikers.
Aangezien het gebruik van de app altijd begint bij de toernooi coordinator is dat de enige personage die we gaan ondersteunen. 
In basis moet de app het meerkamp formulier vervangen na deze delivery.

### Scope
Zorgen voor een hulpmiddel waarmee toernooi coordinator niet handmatig resultaten hoeven uit te rekenen. Het moet verder verkeerd ingevulde resultaten ontdekken.

### Out-of-scope 
- Alles wat via de server moet verlopen of meerdere gebruikers betreft. 
- De verdeling in de zaal
- Tijd

### Stories
- Als toernooi coordinator kan ik een toernooi aanmaken
- Als toernooi coordinator kan ik spelers aan een toernooi toevoegen die **geen** lid zijn van de NTTB
- Als toernooi coordinator kan ik spelers aan een toernooi toevoegen op basis van NTTB bondsnummer
- Als toernooi coordinator kan ik spelers zoeken in de NAS op basis van club en naam zodat ik ze kan toevoegen 
- Als toernooi coordinator kan ik meerdere spelers van dezelfde club toevoegen zodat ik ze aan het toernooi kan toevoegen
- Als toernooi coordinator kan ik de rating, licentie en klasse van spelers ophalen uit NAS
- Als toernooi coordinator kan ik het aantal meerkamps en de configuratie van de meerkamps (grote van de pool, wedstrijdvorm) bepalen
- Als toernooi coordinator kan ik de spelers automatisch laten verdelen over de meerkampen in het toernooi
- Als toernooi coordinator kan ik de spelers handmatig verdelen over de meerkampen in het toernooi
- Als toernooi coordinator kan ik spelers tussen meerkampen verplaatsen binnen het toernooi
- Als toernooi coordinator kan ik de wedstrijd resultaten invullen
- Als toernooi coordinator kan ik het toernooi bewaren zodat ik het later kan aanpassen
- Als gebruiker zie ik altijd de score en positie van een speler zien

### Openstaande vragen
- [ ] Welke configureerbare eigenschappen heeft een meerkamp naast tijd, games, best-of-x en tafels?
- [-] Wat gebeurt er als spelers na aanvang toegevoegd/verwijderd worden?
    - [ ] Het standaard regelement voorziet hier in antwoord. Uitzoeken wat het regelement zegt, kijken of het gecodeficeerd kan worden en denk na over eventuele afwijking
- [ ] Wat gebeurt er als het aantal games wordt aangepast? Zeker bij kleine clubs en onervaren toernooi coordinators kan het gebeuren.
- [ ] Wat gebeurt er als een wedstrijd niet ingevuld wordt?
    - [X] Moet altijd ingevuld worden. Dat of de toernooi coordinator moet de poul aanpassen.
    - [ ] Is dit ook van toepassing als speler uitvalt bij blessure
    - [ ] Hoe gaan we om met "valsspelers"?
- Willen we ondersteuning hebben voor meerdere score systemen?
- Hoe gaan we om met het "tossen" van de winnaar?
- Hoe nummeren we de wedstrijden (zeker wanneer de organisatie meerdere meerkampen heeft, die ondersteuning moeten we hier al toevoegen)
    - [X] Normale meerkamp volgt numerieke oplopende nummers, maar wedstrijdformulier voorziet 
- Privacy/AVG (Nu is alles nog lokaal, maar later kommen de gegevens ook centraal terecht)
    - Wat als een speler zijn naam niet zichtbaar wilt hebben?
    - <del>Hoe lang worden gegevens bewaard?</del> Wanneer worden gegevens verwijderd?
    - Hoe kan een persoon zijn gegevens laten verwijderen?

## Delivery 2: Meerdere gebruikers

De tweede delivery moet een de kleinste aanpassing zijn waarbij er meerwaarde wordt gecreeerd voor spelers en scheidsrechters.
We willen hierbij de hoeveelheid werk voor de toernooi coordinator reduceren. Het doel is dan ook dat deze niet meer zelf de wedstrijden hoeft in te vullen.

### Scope
 Zorgen dat spelers en scheidsrechter de resultaten kunnen invullen en dat zij zien wanneer zij wat moeten doen voor hun meerkamp.

### Out-of-scope 
Integratie scoreboard. Meerdere tafels, extra functionaliteit voor toernooi coordinator/leider.

### Stories
- Als coordinator kan ik de meerkamp "openbaar" maken
- Als speler kan ik de stand van de meerkamp zien
- Als speler kan ik per wedstrijd zien tegen wie ik moet spelen
- Als persoon kan ik zien bij welke wedstrijd ik de scheidsrechter ben
- Als scheidsrechter kan ik scores invullen van de wedstrijd waar ik scheidsrechter ben
- Als speler kan ik de scores invullen van de wedstrijd waar geen scheidsrechter aanwezig is
- Als speler kan ik een verkeerd ingevoerde score "aanvechten" zodat het bekend is bij de wedstrijdleiding
- Als speler/scheidsrechter kan ik aangeven dat mijn tegenstander afwezig is.
- Als gebruiker/toeschouwer/speler/scheidsrechter zie ik in de app de resultaten bijgewerkt worden.

### Openstaande vragen
- (advice) Alvast nadenken over hoe we het scoreboard systeem willen integreren. We willen hier geen aparte implementatie. Denk ook aan aantekeningen maken
- Hoe weten de spelers bij welke wedstrijd zij moeten kijken?
- Hoe krijgen niet NTTB leden toegang tot hun wedstrijd
- Hoe doen we authenticatie van niet NTTB leden (wachtwoord?)
- Willen we ondersteuning voor het uitprinten van schema's? (want niet iedereen is digitaal)

## Delivery 3: Meerdere tafels en speelvolgorde

Deze delivery is bedoeld om handige functies toe te voegen die vaak gevraagd worden: Zoals op welke tafel speel ik? En mag ik effe uitrusten? En kunnen we op meerdere tafels spelen, want ik moet op tijd naar huis?

### Scope 
Tijd bijhouden van een meerkamp (loopt men voor/achter op schema), volgorde van wedstrijden aanpassen, volgorde van rondes aanpassen, hoeveelheid tafels aanpassen.

### Out-of-scope
Rekening houden me totaal aantal tafels dat aanwezig is in de speelzaal, notificaties.

### Stories
- ... TODO ...

## Delivery 4: Toernooi met meerdere meerkampen

Deze delivery is bedoeld om meerdere meerkampen op een locatie te coordineren. 
Tevens willen we niet dat de gebruiker continue op zijn telefoon kijkt (want tafeltennis kijken is leuker) dus introduceren we notificaties zodat men reactief met hun mobiel om hoeven te gaan.

### Scope
Notificaties! Rating/handicap van spelers invullen, automatische meerkampen aanmaken op basis van rating/handicap. Rekening houden met aantal tafels in de zaal zodat het systeem automatisch de aantal tafels per meerkamp kan aanpassen. Start/stop tijden. Meerkamp over meerdere dagen.

### Out-of-scope
Externe systemen ter prestentatie. Finale

### Stories
- ... TODO ...