# 🌿 Excel Advanced: Analisi Turismo Sostenibile & Segmentazione Utenti

## 📌 Panoramica del Progetto
Questo repository raccoglie l'elaborato finale sviluppato per il modulo **Excel Advanced**. 

L'analisi si inserisce nel contesto strategico di una multinazionale del settore turistico (gestione e affitto di appartamenti su scala globale) focalizzata sulla sostenibilità ambientale. L'obiettivo dell'elaborato è trasformare i dati grezzi delle prenotazioni in **Business Intelligence** per:
1. Individuare le destinazioni turistiche con il maggior gradimento ecologico e la miglior valutazione degli alloggi.
2. Analizzare i comportamenti di mobilità degli ospiti, valutando l'efficacia dell'incentivazione di mezzi a basso impatto ambientale (biciclette e monopattini elettrici).
3. Profilare il pubblico di riferimento (demografia, dimensione dei nuclei familiari e modelli di spesa) per ottimizzare le future campagne di marketing.

---

## 📁 Struttura del Repository e della Cartella di Lavoro

Il progetto è basato sul file `Progetto_Excel_Advanced_di_Lorenzo_DAngeli.xlsx`, articolato su 7 fogli di lavoro interconnessi:

| Foglio di Lavoro | Descrizione e Contenuto |
| :--- | :--- |
| **`RawData`** | Dataset di origine contenente 300 record relativi alle prenotazioni degli utenti, comprensivo di dati demografici, durata del soggiorno, costi a notte, valutazione degli appartamenti, punteggi di attenzione ambientale della città e mezzi noleggiati. |
| **`Test`** | Foglio di sintesi del test contenente le 15 domande di analisi, le risposte calcolate, le formule applicate e una breve descrizione metodologica per ciascun passaggio. |
| **`Pivot domanda 6`** | Tabella Pivot per l'aggregazione e il filtraggio degli utenti con spesa totale sostenuta superiore a 300 €. |
| **`Pivot domanda 7`** | Tabella Pivot per la classificazione dei costi totali e l'identificazione dell'utente con la spesa complessiva minore. |
| **`Pivot domanda 9`** | Tabella Pivot per la profilazione anagrafica e il conteggio degli utenti con età superiore a 30 anni. |
| **`Pivot domanda 11`** | Tabella di contingenza Pivot per verificare il noleggio combinato di auto e monopattini. |
| **`Pivot domanda 14`** | Tabella Pivot e calcolo aggregato della spesa media pro-capite per singolo membro del gruppo familiare. |

---

## 📊 Sintesi delle Analisi Svolte e Risultati Key

### 1. Profilazione Demografica e Data Cleaning
* **Conteggio e Volumi**: Analizzati 300 record utente (`COUNTA`). È stata identificata la moda della dimensione del gruppo familiare, risultata pari a **4 membri** (`MODE`).
* **Data Cleaning**: Identificato e segnalato un errore di digitazione nella colonna dei Paesi alla riga 89 (`Germny` invece di `Germany`).
* **Calcolo Età Esatta**: Utilizzando la funzione `DATEDIF` sulla data di nascita aggiornata alla data corrente, è emerso che **289 utenti su 300** hanno un'età superiore ai 30 anni.

### 2. Mobilità e Impatto Ambientale
* **Mezzi Più Affittati**: Le **Auto** e le **Biciclette** figurano a pari merito come i mezzi più noleggiati in assoluto (146 preferenze ciascuno).
* **Comportamento nelle Città "Green"**: Nelle città con una valutazione di attenzione all'ambiente >= 6, l'uso combinato dei **mezzi a basso impatto ambientale** (117 totali: 60 biciclette e 57 monopattini) supera nettamente il noleggio di auto tradizionali (67).
* **Noleggio Combinato**: 74 utenti hanno affittato contemporaneamente un'auto e un monopattino elettrico (`COUNTIFS`).

### 3. Analisi Economica e Top Destinations
* **Spesa Media Pro-Capite**: La spesa media totale sostenuta per singolo membro del nucleo familiare è pari a 331,09€ (`AVERAGE` applicato sui dati aggregati Pivot).
* **Destinazioni Eccellenti**: Applicando la funzione array dinamica `FILTER` combinata con `MAX`, sono state individuate le sole 4 città che hanno raggiunto contemporaneamente il punteggio massimo di attenzione ambientale (10/10) e la valutazione massima dell'alloggio (5/5): **Tarma**, **PÄarbaÅŸÄ**, **Denpasar** e **Thabazimbi**.

---

## 🛠️ Competenze Tecniche e Funzioni Excel Utilizzate

* **Funzioni Statistiche e Conteggio Condizionale**: `COUNTA`, `COUNTIF`, `COUNTIFS`, `MODE`, `AVERAGE`.
* **Funzioni Matematiche e Array Dinamici**: `MAX`, `SUM`, `UNIQUE`, `FILTER`.
* **Calcolo Date**: `DATEDIF` per il calcolo preciso dell'età anagrafica.
* **Tabelle Pivot**: Modellazione e aggregazione dati multi-variabile, tabelle di contingenza, filtri di campo e campi calcolati.
