# Final_Project_Data_Analytics
# 🚗 ISTAT Traffic Analysis — Progetto Finale (Data Analytics)
Questo è il mio progetto finale del Master in Data Analytics.  
L’obiettivo è analizzare i dati ISTAT sugli incidenti stradali nei comuni italiani, integrarli con dati territoriali (popolazione e superficie) e costruire:
- un **dataset arricchito**
- un’**analisi esplorativa**
- un **modello statistico/ML**
- una **dashboard Power BI**

---

## 📁 Project Structure

Final_Project_Data_Analytics/
│
├── data/
│   ├── istat_raw.csv
│   ├── situas_raw.csv
│   └── dataset_final.csv
│
├── notebooks/
│   ├── 01_fetch_istat.ipynb
│   ├── 02_clean_merge.ipynb
│   ├── 03_eda_analysis.ipynb
│   └── 04_ml_clustering_regression.ipynb
│
├── powerbi/
│   └── dashboard.pbix
│
├── slides/
│   └── capstone_presentation.pdf
│
└── README.md

---

## 🎯 Obiettivo del progetto

La mia azienda opera nel settore della **gestione del traffico e prevenzione del rischio**.  
Serve identificare **i comuni italiani con il più alto tasso di incidenti**, valutando:
- incidenti totali  
- incidenti pro capite  
- densità di incidenti per km²  
- trend temporali  
- cluster di comuni ad alto rischio
  
---

## 📊 Dataset utilizzati

### **1. ISTAT — Incidenti stradali**
Endpoint API:  
`https://esploradati.istat.it/SDMXWS/rest/data/41_983`

Contiene:
- `REF_AREA` → codice ISTAT del comune  
- `TIME_PERIOD` → anno  
- `DATA_TYPE` → tipo di misura  
- `OBS_VALUE` → valore osservato  

I dati vengono scaricati automaticamente tramite Python.

---

### **2. SITUAS — Popolazione e superficie**
Fonte: https://situas.istat.it  
Contiene:
- popolazione residente  
- superficie in km²  
- codici territoriali  

Il file viene scaricato una volta e salvato in `/data/situas_raw.csv`.

---

## 🔍 Descrizione dei dati

### 1. Dati ISTAT (incidenti)
Scaricati tramite API:  
`https://esploradati.istat.it/SDMXWS/rest/data/41_983`

Contengono:
- codice ISTAT del comune  
- anno  
- tipo di dato (incidenti, feriti, ecc.)  
- valore osservato  

### 2. Dati SITUAS (popolazione e superficie)
Scaricati dal sito SITUAS.  
Contengono:
- popolazione residente  
- superficie in km²  
- codici territoriali  

---

## 🔧 Fasi del progetto

1. **Raccolta dati**  
   - download automatico dei dati ISTAT  
   - import del CSV SITUAS  

2. **Pulizia dati**  
   - controllo codici comuni  
   - rimozione valori anomali  
   - selezione degli anni utili  

3. **Creazione dataset finale**  
   - incidenti pro capite  
   - incidenti per km²  
   - altre colonne utili  

4. **Analisi esplorativa (EDA)**  
   - grafici  
   - distribuzioni  
   - comuni con più incidenti  

5. **Analisi statistica / ML**  
   - clustering dei comuni  
   - regressione semplice  
   - eventuali test statistici  

6. **Dashboard Power BI**  
   - mappa  
   - KPI  
   - ranking comuni  

7. **Presentazione finale**  
   - spiegazione del lavoro svolto  
   - risultati ottenuti
   - 
---

## ▶️ Come eseguire il progetto

1. Clonare il repository  
2. Installare le dipendenze Python  
3. Eseguire i notebook in ordine numerico  
4. Aprire la dashboard Power BI  
5. Consultare le slide finali  

---

## 👤 Autore

**Simone Certomà**  
Master in Data Analytics — Boolean Careers  
2026
