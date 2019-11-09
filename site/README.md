# instructie_template_hugo


# Setup

Om dit project werkend te krijgen is het volgende nodig:

* Hugo [Hugo getting started](https://gohugo.io/getting-started/)


## Wil je de hugo getting started niet lezen?

Installatie:
### Macos
Zorg dat je `homebrew` hebt geinstalleerd, dit is het geval wanneer `brew` in de terminal werkt.
Installatie voor hugo : `brew install hugo`

## Windows
Heb je `Chocolatey` geinstalleerd?
`choco install hugo -confirm`

Heb je `Scoop` geinstalleerd?
`scoop install hugo`

Heb je deze package managers niet geinstalleerd? Installeer dan alsjeblieft een package manager. Het maakt je leven veel makkelijker en managed alles voor jou.
Wil je dit echt niet doen? Volg dan de uitgebreide instructie op de hugo website. [Windows installatie Hugo](https://gohugo.io/getting-started/installing/#windows).

### Linux
Heb je `snap` geinstalleerd?
`snap install hugo`

#### Debian/Ubuntu:
`sudo apt-get install hugo`

#### Arch linux
`sudo pacman -Syu hugo`

#### Fedora, Red Hat and CentOs
`sudo dnf install hugo`

# Structuur

-> [Hugo uitleg](https://gohugo.io/getting-started/directory-structure/)

De mappenstructuur ziet er als volgt uit:
```

├── README.md
└── instructie_site
    ├── archetypes
    │   └── default.md
    ├── config.toml
    ├── content
    │   └── instructies
    │       └── Instructies-voor-mentoren.md
    │       └── mBot.md
    │       └── ....
    ├── public
    │   ├── categories
    │   ├── css
    │   ├── index.html
    │   ├── index.xml
    │   ├── instructies
    │   ├── sitemap.xml
    │   └── tags
    └── themes
        └── coderdojo-nijmegen

```

Ons eigen theme is te vinden onder de folder 'themes', hierin worden alle specifieke templates gedefinieerd die vervolgens door `hugo` gebruikt worden om onze website te genereren.

## Nieuwe instructie   

Om een nieuwe instructie toe te voegen kan de instructie worden gevolgd die in `content/instructies/instructies-voor-mentoren.md` is te vinden.
Dit is te lezen door het bestand zelf te openen, maar kan natuurlijk ook door hugo worden 'gerenderd' om het vervolgens als HTML-pagina te lezen.

* Ga naar het bestand, lees de markdown
* Of, zorg dat je `hugo` hebt geinstalleerd en type `hugo server` in deze folder. Navigeer vervolgens via de browser naar `localhost:1313`
