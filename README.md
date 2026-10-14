# Kinoabend – iPhone-App ohne Browser-Leisten

Installierbare Web-App (PWA). Vom Home-Bildschirm gestartet läuft sie im Vollbild – ohne Safari- und ohne Claude-Leiste, angepasst an iPhone 17 Pro (Dynamic Island, Home-Indikator).

## Online stellen (kostenlos, HTTPS) – GitHub Pages
1. Auf github.com ein neues Repository anlegen, z. B. `kinoabend` (Public).
2. „Add file → Upload files“ → den **Inhalt** dieses Ordners hochladen (index.html, sw.js, manifest.webmanifest, Ordner icons) → Commit.
3. Settings → Pages → Source: „Deploy from a branch“, Branch `main`, Ordner `/ (root)` → Save.
4. Nach ca. 1 Minute ist die App unter `https://<dein-name>.github.io/kinoabend/` erreichbar.

## Aufs iPhone
Adresse in **Safari** öffnen → Teilen → **Zum Home-Bildschirm** → Hinzufügen.
Dann über das Kinoabend-Symbol starten (nicht über Safari).

## Lokal testen (Windows-PC)
Im Ordner: `python -m http.server 8080` → am PC `http://localhost:8080`.
Hinweis: Vom iPhone über `http://<PC-IP>:8080` geht der Vollbildmodus, Offline-Cache aber nur mit HTTPS.

## Ändern
Daten stehen in `index.html` (`const DATA = …`). Nach Änderungen in `sw.js` die `CACHE`-Version erhöhen, damit iPhones die neue Version laden.
