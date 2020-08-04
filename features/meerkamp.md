---
status: work-in-progres
owner: Wouter
---

# Feature: Meerkamp

### Grote vragen
- Onderstaande deliveries beschrijven alleen meerkamp. Maar kunnen we ook stappen zetten om "generiek" toernooi systeem te ondersteunen? Zoals inschrijvingen, koppeling met scoreboard, wedstrijd resultaat in de zaal.
- Moeten de resultaten van de meerkampen bewaard worden in NAS?

### Personages in stories
- Wedstrijdcoordinator/Wedstrijdleider
- Speler
- Scheidsrechter
- Toeschouwer

## Delivery 1: Hulpmiddel voor wedstrijdcoordinator

### Scope
Zorgen voor een hulpmiddel waarmee wedstrijdcoordinator niet handmatig resultaten hoeven uit te rekenen. Het moet verder verkeerd ingevulde resultaten ontdekken.

### Out-of-scope 
Alles wat via de server moet verlopen of meerdere gebruikers betreft.

### Stories
- Als wedstrijdcoordinator kan ik een meerkamp aanmaken
- Als wedstrijdcoordinator kan ik spelers aan een meerkamp toevoegen
- Als wedstrijdcoordinator kan ik de onderlinge resultaten invullen
- Als wedstrijdcoordinator kan ik een meerkamp bewaren
- Als wedstrijdcoordinator kan ik na de laatste wedstrijd meteen zien wie op welke plaatst staat

### Openstaande vragen
- Hoe gaan we om met niet NTTB-spelers?
- Wat gebeurt er als spelers na aanvang toegevoegd/verwijderd worden?
- Wat gebeurt er als het aantal games wordt aangepast? Zeker bij kleine clubs en onervaren wedstrijdcoordinators kan het gebeuren.
- Wat gebeurt er als een wedstrijd niet ingevuld wordt? 
- Willen we ondersteuning hebben voor meerdere score systemen?
- Hoe gaan we om met het "tossen" van de winnaar?
- Hoe nummeren we de wedstrijden (zeker wanneer de organisatie meerdere meerkampen heeft, die ondersteuning moeten we hier al toevoegen)
- Hoe gaan we om met privacy van spelers? (Hier nog de verantwoordelijkheid van wedstrijdleiding, maar bij volgende delivery ook verantwoordelijkheid van NTTB)

## Delivery 2: Meerdere gebruikers

### Scope
 Zorgen dat spelers en scheidsrechter de resultaten kunnen invullen en dat zij zien wanneer zij wat moeten doen voor hun meerkamp.

### Out-of-scope 
Integratie scoreboard. Meerdere tafels, extra functionaliteit voor wedstrijdcoordinator/leider.

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

## Delivery 3: Meerdere tafels en speelvolgorde

### Scope 
Tijd bijhouden van een meerkamp (loopt men voor/achter op schema), volgorde van wedstrijden aanpassen, volgorde van rondes aanpassen, hoeveelheid tafels aanpassen.

### Out-of-scope
Rekening houden me totaal aantal tafels dat aanwezig is in de speelzaal, notificaties.

### Stories
- ... TODO ...

## Delivery 4: Toernooi met meerdere meerkampen

### Scope
Notificaties! Rating/handicap van spelers invullen, automatische meerkampen aanmaken op basis van rating/handicap. Rekening houden met aantal tafels in de zaal zodat het systeem automatisch de aantal tafels per meerkamp kan aanpassen. Start/stop tijden. Meerkamp over meerdere dagen.

### Out-of-scope
Externe systemen ter prestentatie. Finale

### Stories
- ... TODO ...