# Den Grønne Avis API

## API Guide og Setup

Dette API er udviklet som en del af Webudvikler svendeprøven "Den Grønne Avis". API´et er beregnet til at køre lokalt på brugerens maskine med node.js som servergrundlag. Alle routes i dette API kan tilgås på:
`http://localhost:4242/`

## Opsætning:

For at starte API´et skal det først hentes ned. Start derfor med at klone API´et med `git clone`.

### Node version

Dette api kræver at du henter den seneste version af Node JS.
Du kan altid tjekke hvilken version af node du kører med:

```
node -v
```

Hvis ikke du allerede har den seneste version af Node kan denne hentes her:
[Link til Node JS download](https://nodejs.org/en/download)

### MySQL setup

Api´et kræver at du har sat en database op i MySQL. Åben derfor det program du bruger til at styre MySQL. Her skal du oprette en ny database med følgende navn: **DGA**

### .env setup

Før du kan starte api´et skal du have forbundet API´et med din database.
Når du har hentet api´et ned og oprettet en database, navigerer du til rod mappen og opretter en ny .env fil.
Det er vigtigt at .env filen ligger i roden. Det vil sige; ved siden af index.js filen. Denne .env fil skal indeholde følgende:

```
PORT = 4242
DBHOST = localhost
DBNAME = DGA
DBUSER = root
DBPASSWD = password
TOKEN_ACCESS_KEY = myprivatekey
TOKEN_ACCESS_EXPIRATION_SECS = 36000
TOKEN_REFRESH_KEY = myprivaterefreshkey
TOKEN_REFRESH_EXPIRATION_SECS = 864000
```

**DBUSER** skal ændres til det brugernavn du logger ind i MySQL med. Default er "root".
Ligeledes skal **DBPASSWD** ændres til det password du logger ind med.
Det er vigtigt at du placerer denne .env fil roden af projektet. Det vil sige ved siden af index.js filen.

### Start API´et

Når du har oprettet og ændret i din .env fil åbner du en ny terminal og navigerer til roden af projektet. Skriv herefter:

`npm install`

efterfulgt af:

`nodemon`

### Seeding

For at fylde databasen op med "default" data kan du åbne din browser eller bruge postman til at navigere til følgende route:

http://localhost:4242/seedfromcsv

Nu skulle du gerne modtage en "seeding complete" besked og du kan gå i gang med at bruge API´et.

## API Dokumentation

Dokumentationen til API´et kan findes på følgende addresse:

https://documenter.getpostman.com/view/31531123/2sAYdbND6z
