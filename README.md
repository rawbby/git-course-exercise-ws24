**Grundlagen von Git**

### Einführung
Git ist ein leistungsfähiges Versionskontrollsystem, das speziell zur Nachverfolgung von Textdateien wie Quellcode entwickelt wurde. Es erlaubt Entwicklern, Änderungen an Dateien effizient zu speichern und zu verwalten. Git ist weniger für Binärdateien geeignet.

### Bedienung
Git wird hauptsächlich über die Kommandozeile bedient, wobei es auch GUIs wie **Sourcetree** gibt, die die Nutzung vereinfachen.

### Grundkonfiguration
Um Git personalisiert und optimal zu nutzen, sollten einige Einstellungen global konfiguriert werden:

- **Benutzernamen setzen:**  
  `git config --global user.name "<Dein Name>"`

- **E-Mail-Adresse setzen:**  
  `git config --global user.email "<Deine E-Mail-Adresse>"`

- **Standardbranch definieren:**  
  `git config --global init.defaultBranch <Branch-Name>` (z.B. `main`)

- **Zeilenumbrüche (AutoCRLF):**
    - Für Linux: `git config --global core.autocrlf input`
    - Für Windows: `git config --global core.autocrlf true`

### Grundlegende Kommandos

1. **Repository initialisieren**  
   `git init` erstellt ein neues Git-Repository im aktuellen Verzeichnis.

2. **Dateien zur Versionskontrolle hinzufügen**
    - `git add <Datei/Ordner>` fügt spezifische Dateien hinzu.
    - `git add .` fügt alle geänderten Dateien zur Staging Area hinzu.

3. **Status der Dateien prüfen**  
   `git status` zeigt den aktuellen Status des Arbeitsverzeichnisses und der Staging Area an, inklusive ungestagter und gestagter Änderungen.

4. **Änderungen anzeigen**  
   `git diff` zeigt die genauen Änderungen zwischen dem Arbeitsverzeichnis und der Staging Area an. Dies ist nützlich, um zu sehen, was sich konkret verändert hat, bevor man die Änderungen committed.

5. **Dateien zurücksetzen (Restore)**  
   `git restore <Datei>` stellt den ursprünglichen Zustand einer Datei im Arbeitsverzeichnis wieder her, bevor sie zu Git hinzugefügt oder committed wurde. Dieser Befehl wird verwendet, um Änderungen zu verwerfen und die Datei in ihren zuletzt commiteten Zustand zurückzusetzen.

6. **Änderungen festschreiben**  
   `git commit -m "Beschreibung der Änderung"` speichert die Änderungen dauerhaft im Repository und versieht sie mit einer Nachricht zur besseren Nachverfolgbarkeit.

7. **Branches verwalten**
    - **Branch anzeigen und erstellen:**  
      `git branch` zeigt die vorhandenen Branches im Repository an und markiert den aktuell aktiven Branch.  
      `git branch <Branch-Name>` erstellt einen neuen Branch. Branches werden verwendet, um separate Entwicklungsstränge für neue Features oder Bugfixes zu verwalten, ohne den Hauptcode zu beeinträchtigen.

    - **Zwischen Branches wechseln:**  
      `git switch <Branch-Name>` wechselt zu einem bestehenden Branch. Dieser Befehl wird verwendet, um den Kontext zwischen verschiedenen Entwicklungszweigen zu ändern und z.B. zwischen Feature-Branches und dem Haupt-Branch zu navigieren.
