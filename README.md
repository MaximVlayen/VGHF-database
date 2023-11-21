# Database Model voor het Video Game History Foundation (VGHF): Een Korte Bespreking

## Inleiding

Het Video Game History Foundation (VGHF), als non-profitorganisatie, heeft als missie het bewaren en het delen van videogames en aanverwante materialen. Een cruciaal instrument in het verwezenlijken van deze missie is een goed doordacht database model. In deze korte bespreking wordt het voorgestelde model voor het VGHF geanalyseerd met de nadruk op de verschillende entiteiten en hun attributen. Ook wordt besproken welk nut de onderlinge relaties tussen de verschillende entiteiten kunnen hebben voor de organisatie.

## Entiteiten en Attributen:

### 1. Game:
- **Attributen:** gameID, title, format, genre, platform, museumID, warehouseID, price.

De "Game" entiteit vormt het hart van de database en bevat alle informatie over individuele videogames. Door attributen zoals "museumID" en "warehouseID" toe te voegen, kan het VGHF gemakkelijk de huidige locatie van een game terugvinden, of deze nu tentoongesteld wordt in een museum of opgeslagen ligt in een magazijn. Het attribuut "format" geeft informatie over het formaat van de game in kwestie bijvoorbeeld "in cartridge", "CD" of "digitaal formaat". Het attribuut "prijs" verschaft informatie over de kosten van de game.

### 2. Collectible:
- **Attributen:** collectibleID, name, description, category, museumID, warehouseID, price.

De "Collectible" entiteit bevat details over de verschillende aanverwante materialen aan videogames. Ook hier zorgen de attributen "museumID", en "warehouseID" er voor dat het VGHF in staat is om de huidige locatie van een collectible makkelijk teerug te vinden. Het attribuut "category" van een collectible geeft aan onder welke categorie de collectible valt bijvoorbeeld "magazines", "props" of "guides".

### 3. Museum:
- **Attributen:** museumID, name, location, ticket, visitorAmount, revenue.

De "Museum" entiteit geeft informatie over de musea die door het VGHF worden beheerd. Op die manier wil het VGHF videogames en hun cultuur en geschiedenis tentoonstellen aan het publiek. De attributen "ticket", "visitorAmount" en "revenue" verschaffen respectievelijk inzicht in de toegangsprijs, het bezoekersaantal (op jaarlijkse basis) en de opbrengst (ook op jaarlijkse basis) van elk museum.

### 4. Warehouse:
- **Attributen:** warehouseID, location, capacity.

De "Warehouse" entiteit beheert de opslagplaatsen voor de games. Het attribuut "capacity" geeft aan hoeveel games en collectibles een magazijn maximaal kan bevatten. Het VGHF kan hier efficiënt gebruik van maken om bij te houden hoeveel plaats er nog vrij is in een opslagplaats.

### 5. Company:
- **Attributen:** companyID, name, email.

De "Bedrijf" entiteit vertegenwoordigt externe entiteiten die betrokken zijn bij het hergebruik van games. Het attribuut "Email" vergemakkelijkt communicatie met deze bedrijven en bevordert samenwerking.

### 6. GameAttribuut:
   - **Attributen:** GameID, AttribuutID.

   De "GameAttribuut" entiteit fungeert als een associatieve entiteit die de vele-op-vele-relatie tussen games en attributen mogelijk maakt. Hierdoor kunnen meerdere attributen aan een game worden gekoppeld en vice versa.

### 7. GameBedrijf:
   - **Attributen:** GameID, BedrijfID.

   De "GameBedrijf" entiteit is een associatieve entiteit die de vele-op-vele-relatie tussen games en bedrijven mogelijk maakt. Hierdoor kunnen meerdere bedrijven aan een game worden gekoppeld en vice versa.

## Nut van de Entiteiten en Relaties:

### 1. Traceerbaarheid van Games en Collectibles:
De relaties met "museumID" en "warehouseID" in de "Game" en "Collectible" entiteiten verschaffen de mogelijkheid om de locatie van elke individuele game of collectible eenvoudig te traceren. Dit vergemakkelijkt het beheer van uitleenstatussen, tentoonstellingsplanning en minimaliseert het risico op verlies.

### 2. Attributen van Games en Efficiënt Hergebruik:
De entiteit "Attribuut" maakt het mogelijk gedetailleerde kenmerken van games vast te leggen. Dit is cruciaal voor het categoriseren van games en het identificeren van specifieke eigenschappen die van belang kunnen zijn voor hergebruiksaanvragen van bedrijven.

### 3. Financieel Beheer van Musea:
   De entiteit "Museum" bevat cruciale financiële informatie zoals "Toegangsprijs", "Aantal Bezoekers" en "Opbrengst". Door deze gegevens bij te houden, kan het VGHF het financiële succes van elk museum evalueren en strategieën ontwikkelen om de opbrengst te maximaliseren.

### 4. Efficiënt Magazijnbeheer:
   Het attribuut "Capaciteit" in de "Magazijn" entiteit stelt het VGHF in staat om de beschikbare opslagruimte te beheren. Hierdoor kunnen ze anticiperen op toekomstige behoeften, tijdig uitbreiden indien nodig, en de algehele efficiëntie van het magazijnbeheer verbeteren.

### 5. Samenwerking met Bedrijven:
   Het toevoegen van "Email" aan de "Bedrijf" entiteit vergemakkelijkt effectieve communicatie met externe partijen die betrokken zijn bij het hergebruik van games. Dit is cruciaal voor het stroomlijnen van het hergebruiksproces en het bevorderen van samenwerking tussen het VGHF en bedrijven.

### 6. Flexibele Relaties tussen Games, Attributen en Bedrijven:
   De associatieve entiteiten "GameAttribuut" en "GameBedrijf" bieden flexibiliteit in het vastleggen van complexe relaties tussen games, attributen en bedrijven. Dit is van belang in een dynamische omgeving waarin games verschillende eigenschappen kunnen hebben en betrokkenheid van verschillende bedrijven vereist kan zijn.

## Conclusie:

Dit database model voor het Video Game History Foundation biedt een gestructureerde en uitgebreide benadering voor het beheer van videogamecollecties, musea en hergebruiksaanvragen. Door de juiste entiteiten en relaties op te nemen, kan het VGHF effectief de geschiedenis van videogames bewaren, delen en optimaliseren voor toekomstige generaties. Traceerbaarheid, gedetailleerd beheer van kenmerken, financiële inzichten, efficiënt magazijnbeheer en effectieve samenwerking met externe partijen dragen bij aan het succes van het VGHF in het behouden en delen van de rijke geschiedenis van videogames. Dit model biedt niet alleen een solide basis voor het huidige werk van het VGHF, maar ook de flexibiliteit om te evolueren met de voortdurend veranderende wereld van videogames.
