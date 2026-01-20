# Guida Passo-Passo: Pubblicare la tua App su GitHub Pages

Segui questi passaggi per mettere online la tua app KikoGen in modo sicuro (HTTPS) e gratuito, così da far funzionare la telecamera su Android e iOS.

## 1. Crea una Repository su GitHub
1. Vai su [github.com](https://github.com) e accedi (o registrati se non hai un account).
2. In alto a destra, clicca sul simbolo **+** e seleziona **New repository**.
3. **Repository name**: Scrivi un nome, ad esempio `kikogen-app`.
4. **Public/Private**: Scegli **Public** (necessario per GitHub Pages gratuito).
5. Seleziona la casella **"Add a README file"** (opzionale, ma aiuta).
6. Clicca su **Create repository**.

## 2. Carica i File
1. Nella pagina della tua nuova repository, clicca sul pulsante **Add file** > **Upload files**.
2. Trascina i seguenti file dalla tua cartella `Antigravity` dentro l'area grigia del browser:
   - `index.html`
   - `kikogen_banner.png`
3. Aspetta che il caricamento finisca.
4. In basso, nel box "Commit changes", puoi scrivere "Caricamento iniziale" e cliccare sul pulsante verde **Commit changes**.

## 3. Attiva GitHub Pages
1. Nella tua repository, clicca sulla scheda **Settings** (l'ultima a destra, icona ingranaggio).
2. Nel menu a sinistra (sidebar), scorri giù fino alla sezione "Code and automation" e clicca su **Pages**.
3. Sotto **Build and deployment** > **Source**, assicurati sia selezionato "Deploy from a branch".
4. Sotto **Branch**, cambia "None" in **main** (o "master") e conferma con **Save**.

## 4. Fatto!
1. Aspetta circa 1-2 minuti. Aggiorna la pagina delle impostazioni Pages.
2. In alto apparirà un box con scritto: **"Your site is live at..."** seguito da un link (es. `https://tuo-nome.github.io/kikogen-app/`).
3. **Clicca quel link dal tuo telefono**.

### Nota Importante
D'ora in poi, quel link è la tua "App". Puoi salvarlo nella schermata home del telefono. La telecamera funzionerà perché il sito inizia con `https://`.
