# NLS Splitscreen Viewer

Single-File Webanwendung um bis zu 7 YouTube-Streams gleichzeitig zu schauen - mit integriertem Live-Timing fuer die ADAC RAVENOL Nuerburgring Langstrecken-Serie (NLS) und das 24h Rennen.

## Features

- **7 Layouts**: 2x2, 1x4, 4x1, 1+3, 1+4, 1+5, 1+6
- **Live Timing**: Natives Leaderboard und Race Messages via WebSocket
- **Konfigurierbare Spalten** im Leaderboard
- **Stream-Presets** fuer NLS / 24h Rennen Onboards
- **Fullscreen-Modus** mit auto-versteckter UI
- **Persistenz**: Layout, Streams und Einstellungen via localStorage

## Nutzung

Lokal mit Webserver starten (YouTube blockiert `file://`):

```
python3 -m http.server 8080
```

Dann `http://localhost:8080` im Browser oeffnen.

## Disclaimer

Dieses Projekt ist ein **Community-Projekt** und steht in **keinerlei Verbindung** zum ADAC, der NLS, dem 24h Rennen Nuerburgring, deren Veranstaltern, Teams oder Streaming-Partnern. Alle YouTube-Streams und Live-Timing-Daten werden direkt von den offiziellen oeffentlichen Quellen geladen. Keine Daten werden gespeichert oder weitergeleitet.
