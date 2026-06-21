# GEZ-FREI.ONLINE

**YouTube ohne Rundfunkbeitrag.**

Ein Browser-Userscript, das Inhalte von GEZ-finanzierten Kanälen auf YouTube automatisch ausblendet.  
Dein Feed, deine Regeln.

**Website:** [gez-frei.online](https://gez-frei.online)

---

## Features

| Feature | Beschreibung |
| --- | --- |
| **Automatisches Ausblenden** | Videos und Empfehlungen von GEZ-finanzierten Kanälen werden automatisch aus deinem Feed entfernt |
| **Auto-Updates** | Das Script aktualisiert sich automatisch. Neue Kanäle werden erkannt, ohne dass du etwas tun musst |
| **Cloud-Kanalliste** | Die Kanalliste wird von GitHub geladen und täglich aktualisiert. Immer auf dem neuesten Stand |
| **Performance-optimiert** | Intelligentes Caching und Debouncing sorgen für minimale CPU-Last beim Browsen |
| **Umfassende Abdeckung** | Funktioniert auf der Startseite, in der Suche, in der Seitenleiste und im Endscreen von Videos |
| **Debug-Tools** | Eingebaute Konsolen-Befehle zum Debuggen, manuellen Updaten und Cache-Management |

---

## Installation

### 1. Userscript-Manager installieren

Je nach Browser empfehlen wir [ViolentMonkey](https://violentmonkey.github.io/) (Brave & Firefox) oder [Tampermonkey](https://www.tampermonkey.net/) (Chrome).

| Browser | Manager | Link |
| --- | --- | --- |
| Brave | ViolentMonkey | [Chrome Web Store](https://chromewebstore.google.com/detail/violentmonkey/jinjaccalgkegednnccohejagnlnfdag) |
| Chrome | Tampermonkey | [Chrome Web Store](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) |
| Firefox | ViolentMonkey | [Firefox Add-ons](https://addons.mozilla.org/firefox/addon/violentmonkey/) |

ViolentMonkey wird in Chrome wegen Manifest V3 nicht empfohlen — dort Tampermonkey nutzen.

### 2. Script installieren

**[Userscript installieren](https://raw.githubusercontent.com/finalish0/GEZ-Channels-Youtube/refs/heads/main/GEZ-frei.user.js)**

Alternativ die URL direkt im Userscript-Manager öffnen:

```
https://raw.githubusercontent.com/finalish0/GEZ-Channels-Youtube/refs/heads/main/GEZ-frei.user.js
```

### 3. Fertig

Öffne YouTube und genieße deinen bereinigten Feed. Das Script läuft ab sofort automatisch und aktualisiert sich selbst.

---

## Funktionsweise

1. **Kanalliste laden** — Beim Start lädt das Script die aktuelle Liste aller GEZ-Kanäle von GitHub und speichert sie lokal.
2. **Seite überwachen** — Ein MutationObserver beobachtet YouTube auf neue Inhalte, bei jedem Scroll und jeder Navigation.
3. **Kanäle ausblenden** — Jedes Video wird mit der Kanalliste verglichen. Treffer werden entfernt — du siehst nur noch Inhalte ohne Rundfunkbeitrag.

---

## Die Kanalliste

Die Liste der GEZ-finanzierten Kanäle wird zentral auf GitHub gepflegt und regelmäßig aktualisiert.

Du kannst selbst Kanäle zur Liste hinzufügen, indem du einen Pull Request erstellst oder ein Issue öffnest. Die Liste unterstützt Kommentare mit `#` und wird alle 24 Stunden automatisch synchronisiert.

- [Mitmachen (Issues)](https://github.com/finalish0/GEZ-Channels-Youtube/issues)
- [Kanalliste ansehen](https://github.com/finalish0/GEZ-Channels-Youtube/blob/main/GEZ-Channels.txt)

---

## Debug-Befehle (Konsole)

```js
window.gezDebug.getChannels()   // Zeigt alle geladenen Kanäle
window.gezDebug.forceUpdate()   // Sofortige Aktualisierung der Liste
window.gezDebug.clearCache()    // Cache löschen und neu laden
```

---

## Links

- [GitHub](https://github.com/finalish0/GEZ-Channels-Youtube)
- [Issues](https://github.com/finalish0/GEZ-Channels-Youtube/issues)
- [Lizenz](https://github.com/finalish0/GEZ-Channels-Youtube/blob/main/LICENSE)

GEZ-FREI.ONLINE — Open Source.