# 🫁 Calcolo Volumi da FiO2 (Medical O2 Mixer)

Un'applicazione web progressiva (PWA) progettata per il personale sanitario, utile per calcolare rapidamente i flussi di **Aria** e **Ossigeno** necessari per ottenere una specifica **FiO2** (Frazione inspirata di Ossigeno) attraverso un miscelatore o raccordi a Y.

> **Versione attuale:** v1.2
> **Stato:** 🟢 Attivo & Offline-Ready

## 🚀 Funzionalità Principali

* **📱 PWA (Progressive Web App):** Può essere installata su smartphone (Android/iOS) e PC come una vera applicazione.
* **📴 Funziona Offline:** Una volta caricata la prima volta, l'app funziona perfettamente anche in assenza di connessione internet (es. in sale operatorie o seminterrati).
* **💻 Layout Adattivo:** Interfaccia ottimizzata per l'uso rapido su mobile (verticale) e Dashboard completa su PC/Tablet (>600px).
* **⚡ Calcolo Istantaneo:** Zero latenza, calcoli eseguiti direttamente dal dispositivo (Client-side).

## 🧮 La Matematica (Formula di Entrainment)

L'applicazione utilizza la formula standard per la miscelazione di due gas (Aria ambiente al 21% e Ossigeno puro al 100%):

$$
V_{O2} = \frac{V_{Tot} \times (FiO_2 - 21)}{79}
$$

Dove:
* **V_O2**: Litri/min di Ossigeno da impostare.
* **V_Tot**: Flusso totale desiderato (Lt/min).
* **FiO2**: Percentuale di ossigeno desiderata (da 21 a 100).
* **79**: Costante derivata dalla differenza tra O2 puro (100) e Aria (21).
* **V_Aria**: Si ottiene per differenza ($V_{Tot} - V_{O2}$).

## ⚙️ Limiti e Parametri

* **Range FiO2:** 21% - 100%
* **Range Flusso Totale:** 1 - 60 Lt/min (Setup realistico per Alti Flussi/CPAP su colonnine ospedaliere standard).
* **Massimali:** Il sistema considera i limiti fisici delle erogazioni a muro (Max 30 Lt/min O2 + Max 40 Lt/min Aria ≈ 70 Lt Totali teorici, limitati a 60 per sicurezza clinica).

## 📥 Come Installare

### Su Android / Chrome PC
1.  Apri il link del sito.
2.  Clicca sui tre puntini in alto a destra o sulla barra degli indirizzi.
3.  Seleziona **"Installa App"** o **"Aggiungi a schermata Home"**.

### Su iPhone (iOS)
1.  Apri il sito con **Safari**.
2.  Premi il tasto **Condividi** (quadrato con freccia in alto).
3.  Scorri e seleziona **"Aggiungi alla schermata Home"**.

---

## ⚠️ Disclaimer Medico

**ATTENZIONE:** Questo software è uno strumento di supporto al calcolo e **NON** sostituisce il giudizio clinico professionale né i protocolli ospedalieri ufficiali.
L'autore non si assume responsabilità per errori di somministrazione derivanti dall'uso di questo calcolatore. Verificare sempre i flussi impostati con le tabelle di riferimento del proprio reparto o con analizzatori di ossigeno calibrati.

---

### 👨‍💻 Crediti
Ideato e Sviluppato da **Ivan D.**
*Open Source per la comunità sanitaria.*
