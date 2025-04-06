# TSC-Proiect

**SCHEMA BLOC**

![image](https://github.com/user-attachments/assets/04497d2d-6533-4110-9487-8374a65ec72b)

**Bill Of Materials**

![image](https://github.com/user-attachments/assets/06a7cd74-171f-486c-9443-e97a9c5d8095)

**Specificații Hardware**

**🔹 1. Microcontroller – ESP32-C6-WROOM-1-N8**
**CPU:** RISC-V 32-bit, 160 MHz (single-core)

**Memorie:** 320KB SRAM, 512KB ROM, 8MB Flash SPI (W25Q512JVEIQ)

**Conectivitate:** Wi-Fi 6 (300 Mbps), Bluetooth 5 LE (Mesh), Zigbee 3.0

**Periferice:** 4×SPI, 2×I²C, 2×UART, USB 2.0 OTG

**Consum:** 80 mA activ, 1.5 mA sleep, 20 µA deep sleep

**Wake-up:** GPIO, RTC, UART, senzor BME680

**🔹 2. Alimentare**
Încărcare: MCP73831 (100–500 mA), LED stare (GPIO18)

LDO: BD5229G-TR (eficiență 92%, ripple <50mV)

Fuel Gauge: MAX17048 (±1% SOC, alertă critică, 7 µA consum)

**🔹 3. Senzori**
BME680 (I²C, 0x76): temp., umiditate, presiune, VOC/eCO₂

Algoritm IAQ (BSEC), compensare termică, calibrare din fabrică

RTC – DS3231SN#: ±2ppm, backup cu supercondensator, alarmă, square wave

**🔹 4. Afișaj E-Ink** – 7.5", 800×480 px
Interfață: SPI + CS/DC/RST/BUSY

Consum: 15–25 mA la refresh, 0 mA static

Avantaj: imagine persistentă fără consum

**🔹 5. Interfețe & Stocare**
USB-C: alimentare, serial console, DFU update (ESD + Polyfuse 500 mA)

Qwiic I²C: extensii senzori/modul

MicroSD: loguri/fișiere, SPI/SD

Flash externă: W25Q512JVEIQ (quad SPI, aplicații mari)

**🔹 6. Interacțiune**
Butoane: 3× tactile (navigare/selectare/back), debouncing HW/SW

**🔹 7. Interfețe Utilizate**
Interfață	Componente
SPI	E-Ink, Flash, SD Card
I²C	BME680, MAX17048, DS3231, Qwiic
GPIO	Butoane, control display
USB	Alimentare, date

