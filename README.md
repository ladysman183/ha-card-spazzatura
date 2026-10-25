# 🗑️ Dashboard Waste Collection Card per Home Assistant

Una card moderna per la gestione della raccolta differenziata in **Home Assistant**, completa di icone dinamiche, immagini dei bidoni per ritiri singoli/doppi e notifica serale automatica.

---

## 📋 Guida all'Installazione

### 📄 Passaggio 1: Caricare le Immagini dei Bidoni
Scarica i file `.png` presenti in questo repository e inseriscili nella cartella `www/` di Home Assistant (accessibili tramite `/local/`).

---

### 🧩 Passaggio 2: Creare il Template Sensor
1. Vai su **Impostazioni** > **Dispositivi e Servizi** > **Aiutanti**.
2. Clicca su **Crea Aiutante** > **Template** > **Modella un sensore**.
3. Imposta **Nome:** `Spazzatura Domani` ed **Icona:** `mdi:recycle`.
4. Nel campo **Modello di stato**, incolla il codice presente nel file:
   👉 **[Apri sensor.yaml](./sensor.yaml)**

---

### 🔘 Passaggio 3: Creare l'Aiutante Booleano
1. Vai su **Impostazioni** > **Dispositivi e Servizi** > **Aiutanti**.
2. Clicca su **Crea Aiutante** > **Input Booleano** (Interruttore).
3. Nome: `Spazzatura da Portare Fuori` (entità: `input_boolean.spazzatura_da_portare_fuori`).

---

### 🔔 Passaggio 4: Creare l'Automazione Notifica
1. Vai su **Impostazioni** > **Automazioni e Scene** > **Crea Automazione**.
2. Passa alla vista **Modifica in YAML** (tre pallini in alto a destra).
3. Incolla il codice presente nel file:
   👉 **[Apri automation.yaml](./automation.yaml)**

---

### 🎨 Passaggio 5: Aggiungere la Custom Card
> **Prerequisito:** Richiede la scheda [`custom:button-card`](https://github.com/custom-cards/button-card) installata via HACS.

1. Nella tua Dashboard Lovelace, clicca sui tre pallini > **Modifica Dashboard**.
2. Clicca su **Aggiungi Scheda** e seleziona **Manuale** (YAML).
3. Incolla il codice presente nel file:
   👉 **[Apri card.yaml](./card.yaml)**
