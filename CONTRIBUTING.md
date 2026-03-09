# Hinweise zur Zusammenarbeit

## Git-Konfiguration (einmalig!)

Stellen Sie sicher, dass Ihre HAW-Kiel-E-Mail konfiguriert ist:

```bash
git config --global user.name "Vorname Nachname"
git config --global user.email "vorname.nachname@stud.haw-kiel.de"
```

**Nur Commits mit HAW-E-Mail können Ihnen zugeordnet werden!**

Prüfen Sie nach dem ersten Push auf GitHub, ob Ihr Commit korrekt angezeigt wird.

## Commit-Messages

Verwenden Sie aussagekräftige Commit-Messages. Empfohlenes Format:

```
typ: Kurze Beschreibung

Optionale ausführlichere Erklärung.
```

**Typen:**
- `feat:` – Neue Funktionalität (z.B. `feat: Add enemy spawning`)
- `fix:` – Bugfix (z.B. `fix: Ball bounces correctly at screen edge`)
- `refactor:` – Code-Umstrukturierung ohne neue Funktion (z.B. `refactor: Extract Enemy base class`)
- `docs:` – Dokumentation (z.B. `docs: Update README with game instructions`)
- `test:` – Tests (z.B. `test: Add unit tests for collision detection`)
- `style:` – Formatierung, keine Code-Änderung (z.B. `style: Fix indentation in game.py`)

## Branching (empfohlen)

```bash
# Neuen Feature-Branch erstellen
git checkout -b feature/enemy-types

# Arbeiten, committen...
git add .
git commit -m "feat: Add different enemy types with inheritance"

# Zurück zu main und mergen
git checkout main
git pull
git merge feature/enemy-types
git push
```

## GenAI-Kennzeichnung

Wenn Sie GenAI-Tools verwenden, kennzeichnen Sie dies in der Commit-Message:

```
feat: Add particle effects [GenAI: Claude, "pygame particle system with gravity"]
```

## Refactoring-Commits (ab Woche 6)

Refactoring-Commits sind besonders wichtig für Ihre Bewertung. Schreiben Sie klar, was Sie umgebaut haben und warum:

```
refactor: Introduce State Pattern for game states

Vorher: Game states were managed with if/elif chains in the main loop.
Nachher: Each state (Menu, Playing, Paused, GameOver) is a separate class
implementing a GameState interface with enter(), update(), draw() methods.
```
