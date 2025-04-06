# TSC-Proiect

**Schema Bloc**

![image](https://github.com/user-attachments/assets/04497d2d-6533-4110-9487-8374a65ec72b)

**Bill Of Materials**

| Parts                                 | Qty | CHECK_PRICE                                                                                                 | DATASHEET                                   |
|---------------------------------------|-----|--------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| CHG_LED                               | 1   |                                                                                                              |                                             |
| R1_PINH1, R2_PINH1                    | 2   |                                                                                                              |                                             |
| S1                                    | 1   |                                                                                                              |                                             |
| EPD_C5                                | 1   |                                                                                                              |                                             |
| R3                                    | 1   |                                                                                                              |                                             |
| R1_PWRUSB                             | 1   |                                                                                                              |                                             |
| C1, C2, C4_USB, C6, C8, C9, C10, C6_DELAY | 8 |                                                                                                              |                                             |
| C3                                    | 1   |                                                                                                              |                                             |
| R4-R10, R_BOOT, R_CHANGE, R_C1, R_RESET| 11  |                                                                                                              |                                             |
| C7                                    | 1   |                                                                                                              |                                             |
| J4                                    | 1   |                                                                                                              |                                             |
| R_CAPACITOR                           | 1   |                                                                                                              |                                             |
| C5                                    | 1   |                                                                                                              |                                             |
| EPD_C1–EPD_C12                         | 9   |                                                                                                              |                                             |
| R2                                    | 1   |                                                                                                              |                                             |
| R1_BAT                                | 1   |                                                                                                              |                                             |
| Q1, Q2                                | 2   |                                                                                                              |                                             |
| R2_BAT                                | 1   |                                                                                                              |                                             |
| C5_USB                                | 1   |                                                                                                              |                                             |
| C1_BAT, C2_BAT                        | 4   |                                                                                                              |                                             |
| C4                                    | 1   |                                                                                                              |                                             |
| R2-USB, R2-USB1                       | 2   |                                                                                                              |                                             |
| L1                                    | 1   |                                                                                                              |                                             |
| IC1                                   | 1   |                                                                                                              |                                             |
| BOOT_BUTTON, CHANGE_BUTTON, RESET_BUTTON | 3 |                                                                                                              |                                             |
| C10_SUPERCAP                          | 1   | [SnapEDA](https://www.snapeda.com/parts/PC5H225/Vishay/view-part/?ref=eda)                                   |                                             |
| U3                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda)                      |                                             |
| U2                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda)           |                                             |
| PFMF.050.1                            | 1   |                                                                                                              | [Datasheet](http://datasheets.avx.com/schottky.pdf) |
| D2, D7                                | 2   |                                                                                                              |                                             |
| SENSOR2                               | 1   |                                                                                                              |                                             |
| MCP73831                              | 1   |                                                                                                              |                                             |
| J1                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/MAX17048GT10/Analog+Devices/view-part/?ref=eda)                     |                                             |
| U4                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda)                                  |                                             |
| D3, D4, D5                            | 3   | [SnapEDA](https://www.snapeda.com/parts/PG81010603MR/Littelfuse/view-part/?ref=eda)                         |                                             |
| D6, D8–D12                            | 6   |                                                                                                              |                                             |
| J3                                    | 1   |                                                                                                              |                                             |
| J2                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/SI1308EDL-T1-GE3/Vishay+Siliconix/view-part/?ref=eda)               |                                             |
| Q3                                    | 1   |                                                                                                              |                                             |
| TP1–TP17                              | 17  |                                                                                                              |                                             |
| D1                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda)                 |                                             |
| U1                                    | 1   | [SnapEDA](https://www.snapeda.com/parts/W25Q512JV/Winbond+Electronics/view-part/?ref=eda)                   |                                             |
| IC4                                  |     |                                                                                                              |                                             |

**Specificații Hardware**

**🔹 1. Microcontroller – ESP32-C6-WROOM-1-N8**

**CPU:** RISC-V 32-bit, 160 MHz (single-core)

**Memorie:** 320KB SRAM, 512KB ROM, 8MB Flash SPI (W25Q512JVEIQ)

**Conectivitate:** Wi-Fi 6 (300 Mbps), Bluetooth 5 LE (Mesh), Zigbee 3.0

**Periferice:** 4×SPI, 2×I²C, 2×UART, USB 2.0 OTG

**Consum:** 80 mA activ, 1.5 mA sleep, 20 µA deep sleep

**Wake-up:** GPIO, RTC, UART, senzor BME680

**🔹 2. Alimentare**

**Încărcare:** MCP73831 (100–500 mA), LED stare (GPIO18)

**LDO:** BD5229G-TR (eficiență 92%, ripple <50mV)

**Fuel Gauge:** MAX17048 (±1% SOC, alertă critică, 7 µA consum)

**🔹 3. Senzori**

**BME680 (I²C, 0x76):** temp., umiditate, presiune, VOC/eCO₂

Algoritm IAQ (BSEC), compensare termică, calibrare din fabrică

**RTC – DS3231SN#:** ±2ppm, backup cu supercondensator, alarmă, square wave

**🔹 4. Afișaj E-Ink** – 7.5", 800×480 px

**Interfață:** SPI + CS/DC/RST/BUSY

**Consum:** 15–25 mA la refresh, 0 mA static

**Avantaj:** imagine persistentă fără consum

**🔹 5. Interfețe & Stocare**

**USB-C:** alimentare, serial console, DFU update (ESD + Polyfuse 500 mA)

**Qwiic I²C:** extensii senzori/modul

**MicroSD:** loguri/fișiere, SPI/SD

**Flash externă:** W25Q512JVEIQ (quad SPI, aplicații mari)

**🔹 6. Interacțiune**

**Butoane:** 3× tactile (navigare/selectare/back), debouncing HW/SW

**🔹 7. Interfețe Utilizate**

Interfață	Componente
SPI	E-Ink, Flash, SD Card
I²C	BME680, MAX17048, DS3231, Qwiic
GPIO	Butoane, control display
USB	Alimentare, date

## Alocarea pinilor pentru ESP32-C6

| Pin ESP32-C6 | Componentă / Semnal           | Descriere                                                                 |
|--------------|-------------------------------|---------------------------------------------------------------------------|
| GPIO1        | I²C SDA (BME680, MAX17048, DS3231, Qwiic) | Linie de date partajată pentru toți senzorii și RTC-ul conectați la magistrala I²C. |
| GPIO2        | I²C SCL (BME680, MAX17048, DS3231, Qwiic) | Linie de clock utilizată pentru sincronizarea comunicației I²C.          |
| GPIO5        | SPI MISO (E-Paper)            | Primește date de la afișajul E-Paper prin interfața SPI.                 |
| GPIO6        | SPI MOSI (E-Paper)            | Trimite date către afișajul E-Paper prin interfața SPI.                 |
| GPIO7        | SPI CLK (E-Paper)             | Semnal de clock pentru sincronizarea comunicației SPI cu afișajul.      |
| GPIO8        | SPI CS (E-Paper)              | Semnal Chip Select pentru activarea afișajului E-Paper.                 |
| GPIO9        | E-Paper DC (Data/Command)     | Selectează între trimiterea de date sau comenzi către afișaj.           |
| GPIO10       | E-Paper RST                   | Reset hardware pentru afișajul E-Paper.                                 |
| GPIO11       | E-Paper BUSY                  | Indică dacă afișajul este ocupat și nu poate primi comenzi.             |
| GPIO12       | Button #1                     | Buton de control, ex: „Pagina următoare”.                                |
| GPIO13       | Button #2                     | Buton de control, ex: „Pagina anterioară”.                               |
| GPIO14       | Button #3                     | Buton de control, ex: „Meniu” sau „Selectare”.                           |
| GPIO15       | MAX17048 ALERT (opțional)     | Semnal de alertă de la senzorul de baterie (ex: baterie descărcată).    |
| GPIO16       | USB D+ (intern la USB PHY)    | Linie de semnal diferențial pozitiv pentru conexiunea USB 2.0.          |
| GPIO17       | USB D- (intern la USB PHY)    | Linie de semnal diferențial negativ pentru conexiunea USB 2.0.          |
| GPIO18       | LED de status (opțional)      | LED pentru indicarea stărilor (Wi-Fi, încărcare etc.).                  |
| GPIO19       | SD Card CS (opțional)         | Semnal Chip Select pentru cardul microSD.                                |
| GPIO20       | SD Card MISO (opțional)       | Linie de recepție a datelor de la cardul microSD.                       |
| GPIO21       | SD Card MOSI (opțional)       | Linie de transmisie a datelor către cardul microSD.                     |
| GPIO4        | SD Card CLK (opțional)        | Semnal de clock pentru comunicația SPI cu cardul microSD.               |


