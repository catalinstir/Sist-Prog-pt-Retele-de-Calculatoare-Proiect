# **Proiectarea și optimizarea unui robot autonom folosind algoritmi de fuziune a datelor multi-senzor pentru predicția traiectoriei în timp real.**

**Platforma: Vehicul Autonom Bazat pe NXP RDDRONE-FMUK66**

Acest proiect extinde capabilitatile unui vehicul autonom existent de urmarire a liniei prin implementarea integrarii avansate de senzori, capabilitati de depanare wireless si functii de control manual. Focusul principal sta in optimizarea performantei vehiculului prin telemetrie in timp real si imbunatatirea fluxului de dezvoltare prin protocoale de comunicatie robuste.

## Obiective Principale

### 1. **Integrarea Senzorului Optic RPM**
Implementarea monitorizarii vitezei rotilor prin encodere optice pentru a permite controlul in bucla inchisa al motorului. Datele acestui senzor vor interfata cu placa FMUK66 prin intreruperi GPIO, furnizand feedback rotational in timp real pentru reglarea precisa a vitezei si detectarea alunecarii.

### 2. **Sistem Adaptiv de Management al Puterii**
Dezvoltarea unui algoritm inteligent de compensare a debitului motorului care coreleaza datele RPM cu metricile de consum de putere. Acest sistem va ajusta dinamic semnalele PWM pentru a mentine performanta constanta a vehiculului in ciuda caderii de tensiune a bateriei, asigurand operare stabila pe toata durata ciclului de descarcare.

### 3. **Interfata Wireless de Depanare**
Stabilirea unei legaturi de comunicatie wireless (prin modul UART-to-WiFi sau Bluetooth) pentru depanare la distanta si monitorizare telemetrica in timp real. Aceasta interfata va permite ajustarea parametrilor controllerului PID in timp real, vizualizarea starilor FSM si transmiterea datelor de la senzori fara constrangeri de conexiune fizica.

### 4. **Interfata de Control cu Joystick**
Integrarea unui controller wireless de tip gamepad/joystick pentru capabilitati de control manual si testare. Semnalele de control vor fi transmise printr-un protocol wireless dedicat (RF 2.4GHz sau Bluetooth), permitand comutarea fluida intre modurile de operare autonom si manual.

### 5. **Arhitectura Imbunatatita de Comunicatie Multi-Protocol**
Optimizarea framework-ului de comunicatie existent care gestioneaza:
- Protocol **I2C** pentru datele de viziune de la camera Pixy2 la 400kHz
- Intreruperi **GPIO** pentru masuratori de distanta de la senzorul ultrasonic si numararea pulsurilor senzorului RPM
- Generarea de semnale **PWM** pentru controlul directiei cu servo si reglarea vitezei motorului
- **UART/SPI** pentru integrarea modulului wireless

### 6. **Dashboard de Telemetrie in Timp Real**
Dezvoltarea unui sistem de monitorizare care agregheaza datele senzorilor de pe toate canalele de comunicatie (deviatia urmaririi camerei, distanta ultrasonica, RPM roti, tensiunea bateriei) si le transmite prin interfata wireless pentru analiza comprehensiva a starii vehiculului.
