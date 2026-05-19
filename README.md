# Jellyfin TrailerForge V8.5

**Der beste lokale deutsche Trailer-Downloader für Jellyfin**

---

### Warum dieses Tool?

Jellyfin kann bereits von Haus aus Trailer abspielen und viele Nutzer sind mit dem **Media Bar** Plugin (oder Media Bar Enhanced) sehr zufrieden. 

**TrailerForge ist die perfekte Ergänzung dazu.**

Während Media Bar Trailer live aus dem Internet holt, erstellt TrailerForge **hochwertige, saubere und komplett lokale Trailer**, die du einmalig herunterlädst und dann dauerhaft in deiner Mediathek nutzen kannst.

### Die Vorteile der lokalen Lösung:

- **Zukunftssicher**: YouTube erschwert zunehmend das automatische Abrufen von Trailern. Lokale Trailer funktionieren immer.
- **Höchste Qualität**: Bis 4K statt oft nur HD bei Online-Lösungen
- **Saubere Trailer**: Keine nervigen Kanal-Intros, Outros, Werbung oder Logo-Schleifen mehr dank intelligentem Auto-Trimming
- **Offline-fähig**: Trailer sind lokal verfügbar – auch ohne Internet
- **Optimale Jellyfin-Kompatibilität**: Durch automatische AAC-Audio-Normalisierung

---

### Warum AAC-Umwandlung?

Das Tool lädt bewusst die **beste verfügbare Quelle/Qualität** herunter (oft mit Opus-Audio).  
Opus führt jedoch in Jellyfin häufig zu Problemen mit **Direct Play** und verursacht Transcoding oder Abspielprobleme auf verschiedenen Geräten.  

Deshalb konvertiert TrailerForge das Audio automatisch auf **AAC (192 kbit/s)** – die beste und kompatibelste Lösung für Jellyfin. Das Video bleibt dabei in voller Originalqualität erhalten.

---

### ✨ Highlights V8.5

- **Smart Sync Modus** – Erkennt automatisch bereits vorhandene Trailer und lädt nur Fehlende herunter
- **Erweiterte Trailer-Erkennung** (verschiedene Dateinamen)
- **Intelligentes Auto-Trim V8.3** – Entfernt Intro und Outro per Silence- und Blackframe-Erkennung
- Vollautomatisches Setup (venv + smarte FFmpeg-Suche)
- Stabiler Node.js-Support für yt-dlp
- Logging in Datei + Abbruch-Button

---

### Hauptfunktionen

- Starke Studio- und **Deutsche Priorität**
- **NFO-Support** (TMDB-ID wird bevorzugt)
- **Intelligentes Smart-Matching** als zuverlässiger Fallback, falls keine NFO-Datei vorhanden ist (inkl. Jahres-Erkennung aus Ordnernamen)
- Download in bester verfügbarer Qualität (bis 2160p)
- Automatische AAC-Audio-Normalisierung
- Gespiegelte Ordnerstruktur (exakt wie deine Mediathek)

---

### Funktionsweise

1. Scannt deine Medienbibliothek (Filme oder Serien getrennt empfohlen)
2. Prüft, ob bereits ein passender Trailer existiert
3. Liest zuerst die `.nfo`-Datei aus (bevorzugt)
4. Bei fehlender oder unvollständiger NFO führt es **intelligentes TMDB-Smart-Matching** durch (inkl. Jahres-Erkennung)
5. Sucht den besten deutschen Trailer (TMDB → YouTube Fallback)
6. Download + intelligentes Trimmen von Intro & Outro
7. Automatische AAC-Konvertierung
8. Speichert die Trailer in **exakt gespiegelter Ordnerstruktur**

---

### Ausgabe-Struktur (Drag & Drop ready)

Das Tool legt im Output-Ordner **exakt dieselbe Ordnerstruktur** wie deine Mediathek an:
