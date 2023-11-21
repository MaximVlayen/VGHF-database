# Database Model voor het Video Game History Foundation (VGHF): Een Korte Bespreking

Het Video Game History Foundation (VGHF), als non-profitorganisatie, heeft als missie het bewaren en het delen van videogames en aanverwante materialen. Een cruciaal instrument in het verwezenlijken van deze missie is een goed doordacht database model. In deze korte bespreking wordt het voorgestelde model voor het VGHF geanalyseerd met de nadruk op de verschillende entiteiten en hun attributen. Ook wordt besproken welk nut de onderlinge relaties tussen de verschillende entiteiten kunnen hebben voor de organisatie.

## Entiteiten en Attributen:

### 1. Game:
- **Attributen:** gameID, title, format, genre, platform, museumID, warehouseID, price.

De "Game" entiteit vormt het hart van de database en bevat cruciale informatie over individuele videogames. Door attributen zoals "MuseumID" en "MagazijnID" toe te voegen, kan het VGHF gemakkelijk de huidige locatie van een game traceren, of deze nu tentoongesteld wordt in een museum of opgeslagen in een magazijn. Het attribuut "Prijs" verschaft informatie over de kosten van de game.

### 2. Attribuut:
   - **Attributen:** AttribuutID, Naam, Categorie, MuseumID, MagazijnID, Prijs, Beschrijving.

   De "Attribuut" entiteit bevat details over de diverse kenmerken van games. De toevoeging van attributen zoals "Naam", "Categorie", "MuseumID", en "MagazijnID" stelt het VGHF in staat om gedetailleerde informatie over games vast te leggen. Het attribuut "Prijs" biedt informatie over de kosten van het attribuut, terwijl "Beschrijving" aanvullende details verschaft.

### 3. Museum:
   - **Attributen:** MuseumID, Naam, Locatie, Toegangsprijs, Aantal Bezoekers (jaarlijks), Opbrengst (jaarlijks).

   De "Museum" entiteit biedt informatie over de musea die door het VGHF worden beheerd. Attributen zoals "Toegangsprijs", "Aantal Bezoekers" en "Opbrengst" verschaffen inzicht in de financiële en bezoekersgegevens van elk museum.

### 4. Magazijn:
   - **Attributen:** MagazijnID, Locatie, Capaciteit.

   De "Magazijn" entiteit beheert de opslagplaatsen voor de games. Het attribuut "Capaciteit" geeft aan hoeveel games een magazijn kan bevatten. Dit is essentieel voor het efficiënt beheren van de opslagruimte.

### 5. Bedrijf:
   - **Attributen:** BedrijfID, Naam, Email.

   De "Bedrijf" entiteit vertegenwoordigt externe entiteiten die betrokken zijn bij het hergebruik van games. Het attribuut "Email" vergemakkelijkt communicatie met deze bedrijven en bevordert samenwerking.

### 6. GameAttribuut:
   - **Attributen:** GameID, AttribuutID.

   De "GameAttribuut" entiteit fungeert als een associatieve entiteit die de vele-op-vele-relatie tussen games en attributen mogelijk maakt. Hierdoor kunnen meerdere attributen aan een game worden gekoppeld en vice versa.

### 7. GameBedrijf:
   - **Attributen:** GameID, BedrijfID.

   De "GameBedrijf" entiteit is een associatieve entiteit die de vele-op-vele-relatie tussen games en bedrijven mogelijk maakt. Hierdoor kunnen meerdere bedrijven aan een game worden gekoppeld en vice versa.

## Nut van de Entiteiten en Relaties:

### 1. Traceerbaarheid van Games:
   De relaties met "MuseumID" en "MagazijnID" in de "Game" entiteit verschaffen de mogelijkheid om de locatie van elke individuele game eenvoudig te traceren. Dit vergemakkelijkt het beheer van uitleenstatussen, tentoonstellingsplanning en minimaliseert het risico op verlies of diefstal.

### 2. Attributen van Games en Efficiënt Hergebruik:
   De entiteit "Attribuut" maakt het mogelijk gedetailleerde kenmerken van games vast te leggen. Dit is cruciaal voor het categoriseren van games en het identificeren van specifieke eigenschappen die van belang kunnen zijn voor hergebruiksaanvragen van bedrijven.

### 3. Financieel Beheer van Musea:
   De entiteit "Museum" bevat cruciale financiële informatie zoals "Toegangsprijs", "Aantal Bezoekers" en "Opbrengst". Door deze gegevens bij te houden, kan het VGHF het financiële succes van elk museum evalueren en strategieën ontw

ikkelen om de opbrengst te maximaliseren.

### 4. Efficiënt Magazijnbeheer:
   Het attribuut "Capaciteit" in de "Magazijn" entiteit stelt het VGHF in staat om de beschikbare opslagruimte te beheren. Hierdoor kunnen ze anticiperen op toekomstige behoeften, tijdig uitbreiden indien nodig, en de algehele efficiëntie van het magazijnbeheer verbeteren.

### 5. Samenwerking met Bedrijven:
   Het toevoegen van "Email" aan de "Bedrijf" entiteit vergemakkelijkt effectieve communicatie met externe partijen die betrokken zijn bij het hergebruik van games. Dit is cruciaal voor het stroomlijnen van het hergebruiksproces en het bevorderen van samenwerking tussen het VGHF en bedrijven.

### 6. Flexibele Relaties tussen Games, Attributen en Bedrijven:
   De associatieve entiteiten "GameAttribuut" en "GameBedrijf" bieden flexibiliteit in het vastleggen van complexe relaties tussen games, attributen en bedrijven. Dit is van belang in een dynamische omgeving waarin games verschillende eigenschappen kunnen hebben en betrokkenheid van verschillende bedrijven vereist kan zijn.

## Conclusie:

Dit database model voor het Video Game History Foundation biedt een gestructureerde en uitgebreide benadering voor het beheer van videogamecollecties, musea en hergebruiksaanvragen. Door de juiste entiteiten en relaties op te nemen, kan het VGHF effectief de geschiedenis van videogames bewaren, delen en optimaliseren voor toekomstige generaties. Traceerbaarheid, gedetailleerd beheer van kenmerken, financiële inzichten, efficiënt magazijnbeheer en effectieve samenwerking met externe partijen dragen bij aan het succes van het VGHF in het behouden en delen van de rijke geschiedenis van videogames. Dit model biedt niet alleen een solide basis voor het huidige werk van het VGHF, maar ook de flexibiliteit om te evolueren met de voortdurend veranderende wereld van videogames.
