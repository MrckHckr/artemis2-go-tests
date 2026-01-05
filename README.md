# Core Stage RS‑25 – Integrated Test Dashboard (Artemis 2)

Questo notebook Python/Colab realizza una **dashboard interattiva** per il monitoraggio dei test principali del Core Stage RS‑25 del razzo SLS, come parte della preparazione del **GO / NO-GO** di Artemis 2.

La dashboard utilizza **Plotly** per creare grafici interattivi e indicatori (gauge) in stile **NASA Mission Control**.

---

## 📌 Funzionalità principali

### 1. Hot Fire Test (Green Run)
- Simulazione della pressione del motore RS‑25 in funzione del tempo.
- Evidenzia le bande operative tra 4.5 e 5.5 bar (GO/NO-GO).
- Rilevazione visiva di **anomalia (spike)**.

### 2. Vibrazioni strutturali
- (Non implementato in questo notebook, integrabile come estensione futura)
- Possibilità di integrare FFT e risonanze con decisione GO/NO-GO.

### 3. Thermal Cycling
- Simulazione della temperatura del Core Stage tra 800 e 900 K.
- Bande operative evidenziate in verde.
- Rilevazione anomalie visive (spike o fuori soglia).

### 4. Decisioni GO / NO-GO
- **Pressione**: se tutti i valori sono entro soglia → GO, altrimenti WARNING/NO-GO.
- **Temperatura**: stesso criterio della pressione.
- **Semaforo finale**: combinazione dei dati di pressione e temperatura:
  - 🟢 GO: entrambi nominali
  - 🟡 WARNING: solo uno nominale
  - 🔴 NO-GO: nessuno nominale

### 5. Dashboard interattiva Plotly
- Grafico **Pressione vs Tempo** con banda operativa verde.
- Grafico **Temperatura vs Tempo** con banda operativa verde.
- Gauge separati per **Pressione** e **Temperatura**, indicanti GO/NO-GO.
- **Semaforo finale** (gauge) combinato.
- **FINAL DECISION** come oggetto separato sotto il grafico, leggibile e chiaro.

### 6. Anomalie
- Spike artificiali inseriti per dimostrazione: pressione[180], temperatura[220].
- Evidenziati visivamente nei grafici.
- Possibile estensione futura con **Anomaly Detection ML** (Isolation Forest o altri algoritmi).

---

## 🛠️ Tecnologie utilizzate

- **Python 3**
- **Google Colab**
- **Plotly** (grafici interattivi, gauge, annotation)
- **NumPy** e **Pandas** (simulazione dati e gestione dataframe)

---

## 📈 Come funziona

1. Simula i dati di **Pressione** e **Temperatura** con rumore casuale e anomalie.
2. Controlla i valori rispetto alle soglie operative per determinare **GO / WARNING / NO-GO**.
3. Crea grafici interattivi per pressione e temperatura.
4. Visualizza gauge separati per pressione, temperatura e semaforo finale.
5. Aggiunge **FINAL DECISION** come testo separato, chiaro e leggibile.

---

## 🚀 Obiettivo

Fornire un **dashboard completo e professionale** per supportare le decisioni **GO / NO-GO** per il Core Stage RS‑25, come simulazione dei controlli mission-critical della NASA.

---

