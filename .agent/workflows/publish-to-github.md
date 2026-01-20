---
description: Pubblica le modifiche su GitHub Pages
---

# Pubblica su GitHub

Questo workflow ti permette di pubblicare velocemente le modifiche su GitHub.

## Prima volta - Setup iniziale

1. Installa Git da https://git-scm.com/download/win
2. Riavvia il terminale/VS Code

3. Inizializza il repository:
// turbo
```
cd c:/Users/patte/Downloads/kikogen && git init
```

4. Collega al repository remoto:
```
git remote add origin https://github.com/xtpatte/kikogen.git
```

5. (Opzionale) Configura le credenziali:
```
git config --global user.email "tua@email.com"
git config --global user.name "Tuo Nome"
```

## Ogni volta che vuoi pubblicare

// turbo-all

1. Aggiungi le modifiche:
```
git add .
```

2. Crea un commit:
```
git commit -m "Aggiornamento"
```

3. Pusha su GitHub:
```
git push -u origin main
```

Se il branch si chiama "master" invece di "main", usa:
```
git push -u origin master
```

## Note
- La prima volta potrebbe chiederti di fare login con GitHub
- GitHub Pages si aggiorna automaticamente dopo il push (può richiedere 1-2 minuti)
