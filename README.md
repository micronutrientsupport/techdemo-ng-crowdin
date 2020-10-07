# Angular 9 & Crowdin Tech Demo

## Adding new content


1. Add your content to HTML pages with i18n tags

`<h2 i18n="Page subheading | Short sentence welcoming to the page">Hello World!</h2>`

2. Create a master source translation file

`ng xi18n --out-file src/locale/messages.xlf `


Test locally using selected language

```bash
ng serve --configuration=de --port 4201
ng serve --configuration=fr --port 4202
```

## Adding a new language

Update `angular.json` file:

```json
"i18n": {
        "sourceLocale": "en",
        "locales": {
          "de": "src/locale/de/messages.xlf",
          "fr": "src/locale/fr/messages.xlf"
        }
```

```json
"configurations": {
            "de": {
              "localize": ["de"],
              "aot": true
            },
            "en": {
              "localize": ["en"],
              "aot": true
            },
            "fr": {
              "localize": ["fr"],
              "aot": true
            },
```

```json
"configurations": {
            "production": {
              "browserTarget": "angular-localization-demo:build:production"
            },
            "de": {
              "browserTarget": "angular-localization-demo:build:de"
            },
            "en": {
              "browserTarget": "angular-localization-demo:build:en"
            },
            "fr": {
              "browserTarget": "angular-localization-demo:build:fr"
            }
```