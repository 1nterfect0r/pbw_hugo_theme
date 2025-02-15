# PbW Hugo Theme


### 1. Programme installieren (unter Windows)
- Optional: VS Code installieren: https://code.visualstudio.com/download
- Node.js (npm): https://nodejs.org/en/download/  
- Git: https://git-scm.com/downloads/win
- Hugo https://github.com/gohugoio/hugo/releases/latest
  - Download the archive for the desired edition, operating system, and architecture
    - "extended/deploy edition" nutzen!
    - Bspw: "hugo_extended_withdeploy_0.143.0_windows-amd64.zip"
  - Extract the archive
  - Move the executable to the desired directory (bspw. unter Programme einen neuen Ordner "hugo" erstellen)
  - Add this directory to the PATH environment variable


### 2. Repo initial aufsetzen
- Ordner öffnen, in dem das Websiteprojekt angelgegt werden soll (dafür wird automatisch ein neuer Ordner erstellt) 
- git bash im Ordner ausführen  (Rechtsklick -> "Git Bash Here")
  - ```hugo new site example_site``` (eigenen Namen vergeben! Dies erstellt einen neuen Ordner mit diesem Namen, bspw. "example_site")
  - ```cd example_site/``` (hier den Namen von oben angeben)
  - ```git init```
  - ```git submodule add https://github.com/1nterfect0r/pbw_hugo_theme.git themes/pbw_hugo_theme```
  - ```cd themes/pbw_hugo_theme/```
  - ```npm install``` (das kann ein paar Minauten dauern)
  - ```cd ../../```
  - ```printf "/public\n/resources\n.hugo_build.lock\n" >> .gitignore```
  - ```cp themes/pbw_hugo_theme/exampleSite/hugo.toml hugo.toml```
  - ```cp themes/pbw_hugo_theme/exampleSite/_index.md content/_index.md```
- bei 3. weiter machen (die git bash ist bereits passend geöffnet)


### 3. Lokales entwickeln
- im Projekt Ordner git bash ausführen (Rechtsklick -> "Git Bash Here")   
```hugo server```
  - über die die dort ausgegbene Webadresse kann die Website angeschaut werden (bspw. http://localhost:1313/). Dafür muss das git bash fenster geöffnet bleiben.
  - es kann jederzeit mit Strg+C der server gestopt werden um weitere kommandos einzugeben. (per ```hugo server``` kann dann wieder der Server gestartet werden)
- Für komfortables bearbeiten der Website eignet sich VS Code (siehe Programme), es kann alternativ auch mit einem beliebigen Textbearbeitungsprogramm (Windows Editor, Notepad++, etc.) genutzt werden
- Um eine neue Version zu speichern ```git commit -a```

### 4. Deployen
tbd

### 5. Updaten
- Hugo
  - ```hugo version``` zeigt die aktuelle Verison an (bspw. "hugo v0.142.0-1f746a872..." enstrpicht Version 0.142.0)
  - um eine neuere Version zu nutzen, wie oben unter "Programme installieren" erklärt, die neuste Version herunterladen und die alter Datei (Executable) ersetzen.
- pbw_hugo_theme
  - ```git submodule update --remote```

