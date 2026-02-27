# 🗺️ Piano di Sviluppo KikoGen - v4.0

Aggiornato: 2026-02-25

---

## ✅ Punto 1 – Migliorare il Riconoscimento OCR (Scanner)

**Problema:** L'OCR non riesce quasi mai a leggere i numeri sul display perché:
- Il filtro colore è troppo rigido (solo giallo/ambra specifico)
- L'algoritmo è sensibile all'inclinazione del telefono
- Il template matching fallisce se i numeri hanno dimensioni leggermente diverse

**Soluzione implementata:**
- [x] Sostituire il filtro colore rigido con rilevamento basato su **luminosità** (pixel chiari su sfondo scuro)
- [x] Aggiungere uno **slider di contrasto/soglia** nell'interfaccia della camera
- [x] Mostrare la **maschera di debug** (anteprima di ciò che vede il software) in tempo reale
- [x] Abbassare la soglia minima di match quality dal 50% al 40% per maggior tolleranza
- [ ] Aggiungere fallback: se OCR custom fallisce, tentare l'estrazione di numeri tramite pattern semplice sul testo grezzo

**Stato:** ✅ COMPLETATO (2026-02-25)

---

## ✅ Punto 2 – Stampa Corretta (CSS @media print)

**Problema:** Manca un foglio di stile per la stampa, quindi stampare la pagina includerebbe tutta l'interfaccia (bottoni, sfondi, ecc.)

**Soluzione implementata:**
- [x] Aggiungere `@media print` CSS che nasconde tutto tranne l'etichetta `.label-content`
- [x] Garantire che le dimensioni stampate rispettino i mm impostati dall'utente
- [x] Aggiungere un pulsante "🖨️ Stampa" che esegue `window.print()`

**Stato:** ✅ COMPLETATO (2026-02-27)

---

## ✅ Punto 3 – Rinominare/Chiarire il Pulsante Bluetooth

**Problema:** Il pulsante "Bluetooth" usa in realtà `navigator.share()` (menu condivisione OS), creando false aspettative

**Soluzione implementata:**
- [x] Rinominare il pulsante in "📤 Condividi" e aggiornare l'icona
- [x] Aggiornare il testo del dialog di errore per essere più chiaro
- [x] (Opzionale) Aggiungere nota informativa su come condividere a stampante termica via RawBT

**Stato:** ✅ COMPLETATO (2026-02-27)

---

## ✅ Punto 4 – Refactoring Codice Sorgente

**Problema:** Il file `index.html` è monolitico (1535 righe), mescola HTML/CSS/JS, con logica OCR molto lunga e difficile da mantenere

**Soluzione implementata:**
- [x] Separare il CSS in un file `styles.css`
- [x] Separare la logica OCR in un file `ocr-engine.js`
- [x] Separare la logica di export (PDF, immagine, stampa, condivisione) in `export-utils.js`
- [x] Mantenere `digit-templates.js` separato (già ok)
- [x] Pulire `index.html` lasciando solo struttura HTML e logica di orchestrazione
- [x] Aggiornare `GUIDA_GITHUB.md` con la lista dei nuovi file da caricare su GitHub Pages

**Stato:** ✅ COMPLETATO (2026-02-27)

---

## 📝 Note

- Ogni punto viene sviluppato e testato separatamente prima di procedere al successivo
- Alla fine di ogni punto, fare commit su GitHub con messaggio descrittivo
- Versione corrente: **3.4** → versione target dopo tutti i punti: **4.0**
