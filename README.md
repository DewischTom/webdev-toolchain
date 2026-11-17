# Webdev-Toolchain mit npm, Sass, Bootstrap und BrowserSync

Die Testseite zeigt ein responsives Bootstrap-Grid, zwei Buttons und zwei Bootstrap Icons. Sass bindet die benötigten Bootstrap-Module ein und setzt die Primärfarbe über `$primary` in `src/scss/style.scss`.

## Voraussetzungen

- Git
- Node.js ab 20.19.0 mit npm. Getestet mit Node.js 22.14.0 und npm 10.9.2.

## Installation von GitHub

1. Auf der GitHub-Seite des Repositories unter **Code → HTTPS** die Clone-URL kopieren. `<HTTPS-URL>` und `<Repository-Name>` durch die passenden Werte ersetzen.

   ```sh
   git clone <HTTPS-URL>
   cd <Repository-Name>
   ```

2. Abhängigkeiten installieren und das Stylesheet erzeugen.

   ```sh
   npm install
   npm run scss:build
   ```

   Für eine Installation exakt aus der Lockdatei kann `npm ci` verwendet werden.

## Entwicklung

| Befehl | Funktion |
| --- | --- |
| `npm run scss:build` | Kompiliert `src/scss/style.scss` einmalig nach `dist/css/style.css`. |
| `npm run scss:watch` | Kompiliert das Stylesheet bei Sass-Änderungen automatisch neu. |
| `npm run serve` | Startet BrowserSync und überwacht `index.html` und das kompilierte CSS. |

1. Im ersten Terminal im Projektordner `npm run scss:watch` starten.
2. In einem zweiten Terminal im Projektordner `npm run serve` starten.
3. Die von BrowserSync ausgegebene lokale Adresse öffnen, standardmäßig `http://localhost:3000`.
4. Zum Testen die Primärfarbe in `src/scss/style.scss` oder einen Text in `index.html` ändern und speichern. BrowserSync übernimmt die Änderung automatisch.

Die Icon-Schriften kommen aus dem installierten Paket `bootstrap-icons`. Das erzeugte CSS liegt im Repository. `node_modules/` wird lokal über npm angelegt.
