# C1 Lernkarten Deutsch

Lernkarten für Deutsch C1 als Web-App: Wortschatz, Nomen-Verb-Verbindungen, Passiv und Präpositionen.
312 Karten, jede in drei Übungsarten: Schreiben, Satz ordnen, Auswählen.

Die App besteht nur aus statischen Dateien. Sie braucht keinen Server und keinen Build-Schritt.

## Mit GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, zum Beispiel `c1-lernkarten`.
2. Alle Dateien aus diesem Ordner in das Repository hochladen (auch `.nojekyll` und den Ordner `icons`).
   Im Browser: **Add file → Upload files**, dann **Commit changes**.
3. Im Repository **Settings → Pages** öffnen.
4. Unter **Build and deployment** als Source **Deploy from a branch** wählen, Branch **main**, Ordner **/ (root)**, dann **Save**.
5. Nach ein bis zwei Minuten ist die App unter `https://DEIN-BENUTZERNAME.github.io/c1-lernkarten/` erreichbar.

Mit der Kommandozeile:

```bash
git init
git add .
git commit -m "C1 Lernkarten"
git branch -M main
git remote add origin https://github.com/DEIN-BENUTZERNAME/c1-lernkarten.git
git push -u origin main
```

## Als App installieren

- **Android / Chrome:** Seite öffnen, Menü → **App installieren** oder **Zum Startbildschirm hinzufügen**.
- **iPhone / Safari:** Seite öffnen, **Teilen → Zum Home-Bildschirm**.
- **Computer / Chrome oder Edge:** Symbol **Installieren** in der Adressleiste.

Nach dem ersten Besuch funktioniert die App auch ohne Internet. Der Fortschritt wird im Browser des jeweiligen Geräts gespeichert und nicht zwischen Geräten übertragen.

## Karten ändern oder ergänzen

Alle Karten stehen in `index.html` in der Liste `DECKS`.

- `V("Satz mit [Lösung].", ["falsch 1", "falsch 2"], {n: "Hinweis"})` für Wortschatz, Nomen-Verb-Verbindungen und Präpositionen
- `G("Satz mit [Hilfsverb] und [Partizip].", "Infinitiv", "falsches Partizip")` für Passiv-Lücken
- `T("Aktivsatz.", "Passivsatz.", "falsches Partizip")` für Umformungen
- `N("der Artikel, Pl. die Artikel", "Artikel")` für ein Nomen mit Artikel

Nach einer Änderung in `sw.js` die Versionsnummer in `CACHE` erhöhen (zum Beispiel `c1-lernkarten-v2`), damit alle Geräte die neue Fassung laden.

## Hinweis zu den Inhalten

Ein Teil der Sätze stammt aus Kursmaterial, unter anderem aus Arbeitsblättern von mein-deutschbuch.de, die als urheberrechtlich geschützt gekennzeichnet sind. Eine GitHub-Pages-Seite ist öffentlich im Internet sichtbar. Kläre vor einer öffentlichen Veröffentlichung, ob du diese Sätze weitergeben darfst, oder nutze die App nur privat.

Die Lösungen der Kartensätze ohne Schlüssel (Passiv Präteritum Aufgabe 2 und 3, Passiv Perfekt, Bonn, Nomen-Verb-Verbindungen, Präpositionen) wurden von Claude erstellt und sind nicht offiziell geprüft.
