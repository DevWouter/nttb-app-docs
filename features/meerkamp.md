---
status: work-in-progres
owner: Wouter
---

# Feature: Meerkamp

### Grote vragen
- Onderstaande deliveries beschrijven alleen meerkamp. Maar kunnen we ook stappen zetten om "generiek" toernooi systeem te ondersteunen? Zoals inschrijvingen, koppeling met scoreboard, wedstrijd resultaat in de zaal.
- Moeten de resultaten van de meerkampen bewaard worden in NAS?
- Hoe koppelen we externe systemen?
- Hoe gaan we om met de weergave van een extreem grote meerkamp? Zo hoeven we alleen 4 t/m 8 spelers per meerkamp te ondersteunen, maar wat als we een theoretisch 99 spelers hebben?
- Hoe zorgen we dat updates betrouwbaar verspreid worden?
- Moet alles via de mobiel of is er ook een desktop website? Zeker bij grote complexe toernooien is dat handig.

### Personages in stories
- Toernooi coordinator (ook wel "coordinator" genoemd)
- Speler
- Scheidsrechter
- Toeschouwer

## Delivery 1: Hulpmiddel voor toernooi coordinator

De eerste oplevering is bedoeld om de kleinste meerwaarde aan de app toe te voegen en beschikbaar te maken voor de gebruikers.
Aangezien het gebruik van de app altijd begint bij de toernooi coordinator is dat de enige personage die we gaan ondersteunen. 

### Scope
Zorgen voor een hulpmiddel waarmee toernooi coordinator niet handmatig resultaten hoeven uit te rekenen. Het moet verder verkeerd ingevulde resultaten ontdekken.

### Out-of-scope 
Alles wat via de server moet verlopen of meerdere gebruikers betreft.

### Stories
- Als toernooi coordinator kan ik een meerkamp aanmaken
- Als toernooi coordinator kan ik spelers aan een meerkamp toevoegen
- Als toernooi coordinator kan ik de onderlinge resultaten invullen
- Als toernooi coordinator kan ik een meerkamp bewaren
- Als toernooi coordinator kan ik na de laatste wedstrijd meteen zien wie op welke plaatst staat

### Openstaande vragen
- Hoe gaan we om met niet NTTB-spelers? (Buitenlandse spelers of scholentoernooi)
- Wat gebeurt er als spelers na aanvang toegevoegd/verwijderd worden?
- Wat gebeurt er als het aantal games wordt aangepast? Zeker bij kleine clubs en onervaren toernooi coordinators kan het gebeuren.
- Wat gebeurt er als een wedstrijd niet ingevuld wordt? 
- Willen we ondersteuning hebben voor meerdere score systemen?
- Hoe gaan we om met het "tossen" van de winnaar?
- Hoe nummeren we de wedstrijden (zeker wanneer de organisatie meerdere meerkampen heeft, die ondersteuning moeten we hier al toevoegen)
- Hoe gaan we om met privacy van spelers? (Hier nog de verantwoordelijkheid van wedstrijdleiding, maar bij volgende delivery ook verantwoordelijkheid van NTTB)

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