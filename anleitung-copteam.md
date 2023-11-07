Die TIB Hannover, die auch für den Suchindex OERSI verantwortlich ist, hat ein Tutorial erstellt: Create and publish OER with GitHub https://liascript.github.io/course/?https://raw.githubusercontent.com/TIBHannover/oer-github-tutorial/main/tutorial.md#1
Damit kann man in nur ein paar Minuten OER schreiben und veröffentlichen auf OERSI, wenn man das Template der TIB benutzt. Das Template ist das hier: https://github.com/TIBHannover/markdown-documents-template
Mann kann sich das Template kopieren (so hab ich es gemacht) und damit weiter arbeiten indem man neue .md-Dateien hinzufügt und die 4 vorhandenen löscht.
Diese vier Chapter im template erklären übrigens, wie man in Markdown Bilder einfügt, Formeln benutzt, Videos einbettet (aus Youtube oder dem twillo/TIB-AV-Portal) und H5P-Bausteine einbettet: https://github.com/TIBHannover/markdown-documents-template

# 1 Kurzeinführung Markdown Monster (MM)
Wir nutzen die Software Markdown Monster um die HTML-Texte aus der CoP per copy und paste in Markdown zu konvertieren. Das geht nicht auf github selber. Da kann man auch Markdown schreiben, aber muss dann alle URL-Links etc selbst setzen
Es gibt auch andere Markdown-Editoren. Auf dieser Seite gibt es Empfehlungen: https://github.com/mundimark/awesome-markdown-editors

## Vorarbeiten
1. Markdown Monster installieren
2. File > New (Crtl + N)
3. im schwarzen Feld ist ein neuer Tab aufgegangen: "untitled"
4. Taste F12: zwischen dem Vorschaufenster (Preview Window: ist komplett schwarz und hat eine ovale Rahmenlinie in hellgrau in der 1.ten Zeile)) und dem Schreibeditor (das hat ganz oben eine leicht hellgrauere Zeile in die ich tippen darf) hin und herwechseln.
5. Taste F11: blendet die linke Dateinavigation aus oder ein (dort kann man seine ganzen letzten Dateien gelistet sehen).

* Copy und Paste aus einem CoP-Beitrag:
- Humhub aufrufen - Artikel in der CoP suchen
- CoP-Beitrag markieren (ohne die Tags und ohne die Box "Persönliche Unterstützung und Beratung zu OER finden Sie bei der Netzwerkstelle ORCA.nrw an Ihrer Hochschule."
und kopieren (Strg. C)
- im MM mit F12 in den Schreibmodus wechseln. Cursor blinkt in der ersten Zeile:  "Paste HTML as Markdown"-Befehl ausführen mit STRG+Shift+V
[sollte MM meckern, dass man eine Lizenz für diese Funktion kaufen soll: einfach ignorieren und den Tsatenbefehl nochmal absetzen]
- alle Sonderzeichen (wie z.B. das kleine blaue Dreicksymbol vor unseren Links) oder Emojies löschen. Auch die hellgrauen Trennlinien, die man auf humhub nutzen kann, müssen gelöscht werden. Die kann Markdown nicht interpretieren.
- unser einheitliches Ende hinzufügen.... Das sind diese Zeilen hier:
    __________________________________________________
    ## Weiterlesen
    Hier geht es direkt zum <a href="https://lizenzhinweisgenerator.de/" target="_blank">irgendwas</a>

    ## Bildnachweise
    xx

    ## Tags
    xx

    ## Lizenznachweis
    n.n. für das <a href="http://www.orca.nrw/ueber-uns/netzwerk" target="_blank">Netzwerk Landesportal ORCA.nrw</a>, veröffentlicht in der Community of Practice ORCA.nrw am DATUM, <a href="https://creativecommons.org/licenses/by/4.0/" target="_blank">CC BY 4.0</a>
    ________________________________________________
... und ausfüllen. 
Nicht alle Artikel haben was zum WEITERLESEN oder BILDNACHWEISE (dann diese Zeilen löschen),  
aber alle haben TAGS bekommen (nämlich die humhub-"Themen", die wir ausgewählt haben als Tags): die bitte einsetzen (Komma getrennt)
und jeder Artikel wurde von einer Person aus dem Redaktionsteam geschrieben und an einem Datum in der CoP veröffentlicht.

ACHTUNG: im MarkdownMonster kümmern wir uns noch nicht um die Bilder aus den CoP-Artikeln. Das dort ein Bild vewendet wurde, sieht man in der Markdown-Datei im Editiermodus zwar, das ist eine Zeile die so aussieht:
    ___________________
    ![](https://community.orca.nrw/file/file/download?guid=34ac12d6-393c-4692-8f9f-f3d61843c0d7 "school_calculator_1.png")
    ___________________
Aber da das Bild auf dem Communityserver bei humhub liegt und nicht öffentlich ist, muss das Bild direkt auf github hochgeladen werden, um angezeigt werden zu können. Das machen wir im zweiten Schritt direkt auf github.

- File Save as: Dateiname setzt sich zusammmen aus dem Veröffentlichungsdatum auf humhub (YYYYMMDD) nem Unterstrich _ und dann 2-3 Wörter als Kurztitel. ACHTUNG: keine Leerstellen und keine Umlaute oder das "ß" benutzen.

# 2 Datei ins Github bringen
- https://github.com/lindahalm-hsbi/infOERmiert/tree/main öffnen
- Add file > Upload File: .md. Datei von Festplatte auswählen (choose) und hochladen.
- Auf COMMIT klicken (grüner Button)
- ca. 2 Minuten warten: Im Hintergrund wird die neue -md-Datei verarbeitet. Unter ACTIONS könnt ihr nachschauen, ob alles reibungslos klappt. Beim ersten mal wird das schief gehen (Rotes X), weil ein Link zu einer Bilddateidrin steht, den es nicht gibt (nämlich den humhub-Link).

# 3 Datei finalisieren (Bilder einbetten)
- Code-Übersicht: die letzte Datei anklicken
- mit dem Bleistift in den Editiermodus gehen
- von Preview in Code wechseln
- Cursor dahin setzen, woe das Bild hinsoll
- ganz unten unter dem Editorbereich gibt eine graue Leiste: "Attach files by ...... " - da drauf klicken.
- Bilddatei von Festplatte auswhählen (dafür aus dem COP-Artikel das Bild anklicken und dann in der Großansicht mit Rechtsklick auf die eigene Festplatte speichern) und das hochladen aktivieren.
- Preview aufrufen: ist es an der richtigen Stelle? Wenn nicht dann zurück in Editiermods und die Zeile verschieben.
- die alte Zeile mit dem Link auf humhub löschen.
- in der Preview nochmal prüfen ob alles richtig ist
- Emojies oder blaue Pfeilchen oder Trennlinien aus humhub müssen entfernt sein!
- auf grünen Button COMMIT CHANGES klicken und bestägigen.

# 4  Landing page prüfen
Nach ein paar Minuten ist die ACTION psoitiv durchgelaufen (grüner Haken dran) und die Landing Page ist erstelt worden. Auf der Code-Übersichtsseite könnt ihr im Teil README auf "LANDNING PAGE" klciek und das Ergebniss überprüfen.
Ist die Action nicht grün, sondern rot, dann hat die -md-Datei noch Fehler und ihr müsst auf die Suche gehen.

# 5 Warum möchte ich meine Materialien in Github produzieren und nicht in PowerPoint oder Word?
* Ich kann mit mehreren Personen gleichzeitg auf Github schreiben und mir die Arbeit teilen. 
* Wenn ich mit dem OER-template der TIB Hannover arbeite, ist das Erstellen vom OER ganz einfach. Also perfekt für den Start in die Github-Welt. 
* Github kann aus meinen Texten Webseiten und Texte produzieren. Und die Webseiten werden dann auf Github gehostet. Ich brauche also kein eigenes Wordpress und keinen Webserver.Das Output ist eine PDF-Datei oder eine Webseite oder beides. Schreiben muss ich aber nur reinen Text und ums Layout kümmere ich mich nicht mehr. 
* Das Output wird automatisch in OERSI veröffentlicht und indiziert und ist über www.oersi.org für jeden auffindbar. 
* Github speist alle öffenlichen Repositorien (egal ob Softwarecode oder Textseite) in die Google-Suche ein. Das erhöht meine Reichweite enorm. 
* Die automatische Generierung übernimmt meinen Inhalt (genauer: alles in den Markdown-Dateien, also die Dateien, die mit .md enden) und generiert verschiedene Ausgabeformate. Dazu gehören beispielsweise eine Webseite und eine PDF- Version meiner OER und die sind öffentlich zugänglich. Diese Generierung erfolgt jedes Mal, wenn ich etwas an meinem Repository ändere, sodass mein Inhalt immer auf dem neuesten Stand ist.