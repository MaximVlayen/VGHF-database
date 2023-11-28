# Database Model voor het Video Game History Foundation (VGHF): Een Korte Bespreking

## Inleiding

Het Video Game History Foundation (VGHF), als non-profitorganisatie, heeft als missie het bewaren en het delen van videogames en aanverwante materialen. Een cruciaal instrument in het verwezenlijken van deze missie is een goed doordacht database model. In deze korte bespreking wordt het voorgestelde model voor het VGHF geanalyseerd met de nadruk op de verschillende entiteiten en hun attributen. Ook wordt besproken welk nut de onderlinge relaties tussen de verschillende entiteiten kunnen hebben voor de organisatie.

## Entiteiten en Attributen:

### 1. Game:
- **Attributen:** gameID, title, format, genre, platform, museumID, warehouseID, price.

De "Game" entiteit vormt het hart van de database en bevat alle informatie over individuele videogames. Door attributen zoals "museumID" en "warehouseID" toe te voegen, kan het VGHF gemakkelijk de huidige locatie van een game terugvinden, of deze nu tentoongesteld wordt in een museum of opgeslagen ligt in een magazijn. Het attribuut "format" geeft informatie over het formaat van de game in kwestie bijvoorbeeld "in cartridge", "CD" of "digitaal formaat". Het attribuut "prijs" verschaft informatie over de kosten van de game.

### 2. Collectible:
- **Attributen:** collectibleID, name, description, category, museumID, warehouseID, price.

De "Collectible" entiteit bevat details over de verschillende aanverwante materialen aan videogames. Ook hier zorgen de attributen "museumID", en "warehouseID" er voor dat het VGHF in staat is om de huidige locatie van een collectible makkelijk terug te vinden. Het attribuut "category" van een collectible geeft aan onder welke categorie de collectible valt bijvoorbeeld "magazines", "props" of "guides".

### 3. Museum:
- **Attributen:** museumID, name, location, ticket, visitorAmount, revenue.

De "Museum" entiteit geeft informatie over de musea die door het VGHF worden beheerd. Op die manier wil het VGHF videogames en hun cultuur en geschiedenis tentoonstellen aan het publiek. De attributen "ticket", "visitorAmount" en "revenue" verschaffen respectievelijk inzicht in de toegangsprijs, het bezoekersaantal (op jaarlijkse basis) en de opbrengst (ook op jaarlijkse basis) van elk museum. Door deze gegevens bij te houden, kan het VGHF het financiële succes van elk museum evalueren en strategieën ontwikkelen om de opbrengst te maximaliseren.

### 4. Warehouse:
- **Attributen:** warehouseID, location, capacity.

De "Warehouse" entiteit beheert de opslagplaatsen voor de games. Het attribuut "capacity" geeft aan hoeveel games en collectibles een magazijn maximaal kan bevatten. Het VGHF kan hier efficiënt gebruik van maken om bij te houden hoeveel plaats er nog vrij is in een opslagplaats. Dit stelt het VGHF in staat om de beschikbare opslagruimte te beheren. Hierdoor kunnen ze anticiperen op toekomstige behoeften, tijdig uitbreiden indien nodig, en de algehele efficiëntie van het magazijnbeheer verbeteren.

### 5. Company:
- **Attributen:** companyID, name, email.

De "Company" entiteit vertegenwoordigt alle bedrijven die betrokken zijn bij het VGHF o.a. door het hergebruiken en restaureren van games. Het attribuut "Email" vergemakkelijkt communicatie met deze bedrijven en bevordert samenwerking.

### 6. GameAttribuut:
   - **Attributen:** GameID, AttribuutID.

   De "GameAttribuut" entiteit fungeert als een associatieve entiteit die de vele-op-vele-relatie tussen games en attributen mogelijk maakt. Hierdoor kunnen meerdere attributen aan een game worden gekoppeld en vice versa.

### 7. GameBedrijf:
   - **Attributen:** GameID, BedrijfID.

   De "GameBedrijf" entiteit is een associatieve entiteit die de vele-op-vele-relatie tussen games en bedrijven mogelijk maakt. Hierdoor kunnen meerdere bedrijven aan een game worden gekoppeld en vice versa.

## Nut van de Relaties tussen Entiteiten:

### 1. Traceerbaarheid van Games en Collectibles:
De relaties met "museumID" en "warehouseID" in de "Game" en "Collectible" entiteiten verschaffen de mogelijkheid om de locatie van elke individuele game of collectible eenvoudig te traceren. Dit vergemakkelijkt het beheer van uitleenstatussen, tentoonstellingsplanning en minimaliseert het risico op verlies. Deze relaties zijn één-op-veel relaties aangezien een game/collectible slechts op één plaats tegelijk kan zijn. 

### 2. Games met collectibles verbinden:
De relatie tussen de entiteiten "Games" en "Collectibles" vergemakkelijkt het overzicht tussen beide. Op die manier kan het VGHF eenvoudig bijhouden welke games met welk videogame gerelateerd materiaal verbonden zijn en omgekeerd. Deze relatie is een veel-op-veel relatie. Immers één game kan bijvoorbeeld in meerdere magazines besproken worden en één magazine kan meerdere games bespreken.

### 3. Samenwerking met Bedrijven:
Door een verbintenis te leggen tussen de "Company" en "Games" entiteiten is het VGHF in staat om onder andere bij te houden welke externe partijen het meest gebruik maken van hun collectie om zo vervolgens goede relaties op te bouwen met hun. Het gaat hier om een veel-op-veel relatie omdat meerdere bedrijven meerdere keren gebruik kunnen maken van de collectie van het VGHF. Het toevoegen van het "email" attribuut aan de "Company" entiteit zorgt bovendien voor en meer effectieve communicatie met externe partijen die betrokken zijn bij het hergebruik van games. Dit is cruciaal om de (oude) video game cultuur levende te houden en het bevordert eveneens de samenwerking tussen het VGHF en de betrokken bedrijven.

## Conclusie:

Dit database model voor het Video Game History Foundation biedt een gestructureerde en uitgebreide benadering voor het beheer van videogamecollecties, musea en hergebruiksaanvragen. Door de juiste entiteiten en relaties op te nemen, kan het VGHF effectief de geschiedenis van videogames bewaren, delen en optimaliseren voor toekomstige generaties. Traceerbaarheid, gedetailleerd beheer van kenmerken, financiële inzichten, efficiënt magazijnbeheer en effectieve samenwerking met externe partijen dragen bij aan het succes van het VGHF in het behouden en delen van de rijke geschiedenis van videogames. Dit model biedt niet alleen een basis voor het huidige werk van het VGHF, maar ook de flexibiliteit om te evolueren met de voortdurend veranderende wereld van videogames.
