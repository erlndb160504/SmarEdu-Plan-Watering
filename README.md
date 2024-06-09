# SmarEdu-Plan-Watering: Alat Edukasi Anak dengan Sistem Pengingat Otomatis untuk Melakukan Penyiraman Tanaman
SmartEdu Plant Watering adalah sebuah proyek embedded system yang dirancang untuk memantau dan mengelola kelembaban tanah pada tanaman potted plants, ditujukan sebagai alat edukasi kepada anak-anak. Proyek ini menggunakan sensor kelembaban tanah, OLED display, LCD I2C, relay, dan DFPlayer Mini untuk memberikan notifikasi dan pengelolaan otomatis. Proyek ini juga memanfaatkan FreeRTOS untuk mengelola multitasking pada ESP32.

## Daftar Isi
- [Fitur](#fitur)
- [Perangkat Keras yang Dibutuhkan](#perangkat-keras-yang-dibutuhkan)
- [Pemasangan](#pemasangan)
- [Penggunaan](#penggunaan)
  
## Fitur

- **Pemantauan Kelembaban Tanah:** Mengukur tingkat kelembaban tanah dan menampilkan hasilnya pada LCD dan OLED display.
- **Notifikasi Audio:** Memberikan notifikasi audio berdasarkan kondisi kelembaban tanah.
- **Pengelolaan Relay:** Mengaktifkan atau menonaktifkan relay berdasarkan input dari push button.
- **Tampilan OLED Dinamis:** Menampilkan animasi berdasarkan kondisi kelembaban tanah.
- **FreeRTOS:** Menggunakan FreeRTOS untuk mengelola tugas pemantauan sensor dan push button secara simultan.
- **Watchdog Timer:** Sistem akan di-reset jika kelembaban tanah menunjukkan nilai 100% lebih dari 5 detik untuk mencegah kerusakan pada sistem.

## Perangkat Keras yang Dibutuhkan

- ESP32
- Sensor Kelembaban Tanah (capacitive soil moisture 2.0)
- OLED Display (128x64)
- LCD I2C (16x2)
- Speaker
- Relay
- DFPlayer Mini
- Push Button
- LED Merah dan Hijau
- Kabel Jumper
- Breadboard atau PCB

## Pemasangan

1. **Kloning Repositori**
   ```sh
   git clone https://github.com/username/SmartEdu-Plant-Watering.git
   cd SmartEdu-Plant-Watering

2. **Instalasi Library**
  - `Adafruit GFX Library`
  - `Adafruit SSD1306`
  - `LiquidCrystal I2C`
  - `DFRobotDFPlayerMini`
  - `freeRTOS esp32`
  - `watchdog timer`

3. **Pemasangan Perangkat Keras**
  Sambungkan perangkat keras sesuai dengan skema berikut:
- Sensor Kelembaban Tanah: AOUT ke pin 34, VCC ke 3.3V, GND ke GND.
- OLED Display: SDA ke pin SDA (21), SCL ke pin SCL (22).
- LCD I2C: SDA ke pin SDA (21), SCL ke pin SCL (22).
- Relay: S ke pin 2, VCC ke 5V, GND ke GND.
- DFPlayer Mini: TX ke pin 26, RX ke pin 27, VCC ke 5V, GND ke GND.
- Push Button: Satu pin ke pin 4, pin lainnya ke GND.
- LED Merah: Positif ke pin 5, negatif ke GND.
- LED Hijau: Positif ke pin 13, negatif ke GND.

## Penggunaan
  - Tampilan Kelembaban: Kelembaban tanah akan ditampilkan pada LCD.
  - Notifikasi Audio: DFPlayer Mini akan memainkan suara notifikasi berdasarkan kondisi kelembaban tanah.
  - Pengelolaan Relay: Relay dapat diaktifkan atau dinonaktifkan menggunakan push button.
  - Animasi OLED: OLED akan menampilkan animasi yang sesuai dengan kondisi kelembaban tanah.
  - Watchdog Timer: Sistem akan di-reset secara otomatis jika kelembaban tanah 100% lebih dari 5 detik.
