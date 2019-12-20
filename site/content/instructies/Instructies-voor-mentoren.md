---
titel: Instructies-voor-mentoren
date: 2019-12-20T13:22:50.091Z
---

Om een nieuwe mooie instructie toe te voegen, kunnen verschillende methodes worden toegepast:

- [Gebruik hugo](#gebruik-hugo)
- [Handmatig, zonder andere programma's](#handmatig-zonder-andere-programmas)
- [Instructie schrijven](#instructie-schrijven)


## Gebruik hugo

`hugo` is het programma wat wij gebruiken om uiteindelijk de HTML voor instructies en andere pagina's te genereren.
Voor het toevoegen van een instructie is (gelukkig!) het niet nodig om uitgebreide kennis van `hugo` te hebben.

Om een nieuwe instructie toe te voegen bied het programma `hugo` zelf wel een makkelijke manier, dit gaat als volgt:
`hugo new instructies/{instructie-naam}`

Hugo gebruikt hiervoor een definitie in het thema, wat wij van te voren hebben opgezet, om zo een nieuw bestand `instructie-naam` aan te maken in de `instructies` map.

## Handmatig, zonder andere programma's

Als je het `hugo` programma niet wilt installeren, of niet de mogelijkheid hebt om dit te doen, dan is dat geen probleem.
Je moet nu echter rekening houden met hoe `hugo` 'werkt'.

Hugo genereert bestanden aan de hand van een thema (Dat wij hebben gedefinieerd), en kijkt naar de locatie van het bestand om te weten wat het moet gebruiken.

Onze structuur ziet er als volgt uit:

```
- archetypes
- content
    - instructies
        -   mBot.md
        -   micro-bit.md
        -   ...
        -   ...
        -   wordpress.md
- data
- layouts
- resources
- static
- themes
```

Om een nieuwe instructies toe te voegen dient een bestand te worden toegevoegd aan de `content` folder. De naam van het bestand is vervolgens een deel van het uiteindelijke pad op de website.
Het pad wordt als volgt bepaald: `coderdojonijmegen.github.io/{folder}/{bestandsnaam}`.


## Instructie schrijven

Instructies bevatten een een `front-matters` blok bovenaan de pagina. Dit ziet er nu als volgt uit:

```
---
titel: "Instructies-voor-mentoren"
niveau: "Beginner"
Vereiste software: ""
---
```

Dit wordt door `hugo` en ons template gebruikt om verschillende zaken af te handelen. Wanneer handmatig een nieuwe instructie wordt toegevoegd dan moet dit blok zelf er in worden gezet.

Om de instructies nu te schrijven is het enige wat gedaan hoeft te worden nieuwe content schrijven in het bestand. Dit wordt gedaan met Markdown, maar kan ook HTML bevatten.
Verschillende bronnen om Markdown onder de knie te krijgen:

* [markdown guide](https://www.markdownguide.org)
* [markdown tutorial](https://www.markdowntutorial.com/)
* [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [markdown ontwikkelaar blogpost](https://daringfireball.net/projects/markdown/)
