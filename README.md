# Hugo template for Netlify CMS with Netlify Identity

This is a small business template built with [Victor Hugo](https://github.com/netlify/victor-hugo) and [Netlify CMS](https://github.com/netlify/netlify-cms), designed and developed by [Darin Dimitroff](http://www.darindimitroff.com/), [spacefarm.digital](https://www.spacefarm.digital).

## Getting started

Use our deploy button to get your own copy of the repository. 

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/netlify-templates/one-click-hugo-cms&stack=cms)

This will setup everything needed for running the CMS:

* A new repository in your GitHub account with the code
* Full Continuous Deployment to Netlify's global CDN network
* Control users and access with Netlify Identity
* Manage content with Netlify CMS

Once the initial build finishes, you can invite yourself as a user. Go to the Identity tab in your new site, click "Invite" and send yourself an invite.

Now you're all set, and you can start editing content!

## Local Development

Clone this repository, and run `yarn` or `npm install` from the new folder to install all required dependencies.

Then start the development server with `yarn start` or `npm start`.

## Layouts

The template is based on small, content-agnostic partials that can be mixed and matched. The pre-built pages showcase just a few of the possible combinations. Refer to the `site/layouts/partials` folder for all available partials.

Use Hugo’s `dict` functionality to feed content into partials and avoid repeating yourself and creating discrepancies.

## CSS

The template uses a custom fork of Tachyons and PostCSS with cssnext and cssnano. To customize the template for your brand, refer to `src/css/imports/_variables.css` where most of the important global variables like colors and spacing are stored.

## SVG

All SVG icons stored in `site/static/img/icons` are automatically optimized with SVGO (gulp-svgmin) and concatenated into a single SVG sprite stored as a a partial called `svg.html`. Make sure you use consistent icons in terms of viewport and art direction for optimal results. Refer to an SVG via the `<use>` tag like so:

```
<svg width="16px" height="16px" class="db">
  <use xlink:href="#SVG-ID"></use>
</svg>
```

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
