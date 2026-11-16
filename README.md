# TAZ Rechnung

Rechnungsformular der TAZ Stuttgart eG als installierbare Web-App (PWA).
Live: https://taz-rechnung-formular.netlify.app
Dateien: index.html (enthält jsPDF), manifest.webmanifest, sw.js, Icons.

## Container
```
docker run -d -p 8080:80 --name taz-rechnung ghcr.io/danis0953/rechnung:latest
```
oder `docker compose up -d`. Aufruf: http://localhost:8080
Hinweis: Für Installation als App, Teilen-Funktion und Offline-Betrieb muss die Seite über HTTPS (oder localhost) ausgeliefert werden – Reverse-Proxy mit Zertifikat davorschalten.
Das Image wird bei jedem Push auf `main` automatisch per GitHub Actions gebaut und nach ghcr.io veröffentlicht.
