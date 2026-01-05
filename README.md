# Core Stage RS‑25 – Integrated Test Dashboard (Artemis 2)

This Python/Colab notebook creates an **interactive dashboard** to monitor the main tests of the RS‑25 Core Stage of the SLS rocket, as part of the **GO / NO-GO decision** for Artemis 2.

The dashboard uses **Plotly** to create interactive charts and indicators (gauges) in **NASA Mission Control style**.

---

## 📌 Main Features

### 1. Hot Fire Test (Green Run)
- Simulates the RS‑25 engine pressure over time.
- Highlights the operational range between 4.5 and 5.5 bar (GO/NO-GO).
- Visual detection of **anomalies (spikes)**.

### 2. Structural Vibrations
- (Not implemented in this notebook, can be added in future extensions)
- Possibility to integrate FFT and resonance detection with GO/NO-GO decision.

### 3. Thermal Cycling
- Simulates the Core Stage temperature between 800 and 900 K.
- Operational ranges highlighted in green.
- Visual detection of anomalies (spikes or out-of-range values).

### 4. GO / NO-GO Decisions
- **Pressure**: if all values are within range → GO, otherwise WARNING/NO-GO.
- **Temperature**: same criterion as pressure.
- **Final Traffic Light**: combination of pressure and temperature:
  - 🟢 GO: both nominal
  - 🟡 WARNING: only one nominal
  - 🔴 NO-GO: none nominal

### 5. Interactive Plotly Dashboard
- **Pressure vs Time** chart with green operational band.
- **Temperature vs Time** chart with green operational band.
- Separate gauges for **Pressure** and **Temperature**, indicating GO/NO-GO.
- Combined **final traffic light** gauge.
- **FINAL DECISION** displayed as a separate object below the chart, clear and readable.

### 6. Anomalies
- Artificial spikes inserted for demonstration: pressure[180], temperature[220].
- Visually highlighted in charts.
- Future extension possible with **ML Anomaly Detection** (Isolation Forest or other algorithms).

---

## 🛠️ Technologies Used

- **Python 3**
- **Google Colab**
- **Plotly** (interactive charts, gauges, annotations)
- **NumPy** and **Pandas** (data simulation and dataframe management)

---

## 📈 How It Works

1. Simulates **Pressure** and **Temperature** data with random noise and anomalies.
2. Checks values against operational thresholds to determine **GO / WARNING / NO-GO**.
3. Creates interactive charts for pressure and temperature.
4. Displays separate gauges for pressure, temperature, and the final traffic light.
5. Adds **FINAL DECISION** as a separate, clear, readable text object.

---

## 🚀 Objective

Provide a **complete and professional dashboard** to support **GO / NO-GO decisions** for the RS‑25 Core Stage, simulating NASA mission-critical checks.

---

## 📂 File Structure

