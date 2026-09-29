LumiCarX 🚗💨

Smart Bluetooth Car with Dual Mode Control and 360° Awareness

https://img.shields.io/badge/status-active-brightgreen
https://img.shields.io/badge/Arduino-Uno-blue
https://img.shields.io/badge/license-MIT-green

---

📖 Maelezo

LumiCarX ni gari la roboti lenye uwezo wa kuendeshwa kwa njia mbili:

· Controlling Mode — kuendeshwa kwa simu kwa Bluetooth
· Automotive Mode — kujiendesha yenyewe na kukwepa vikwazo

Gari lina sensorer mbili za ultrasonic (mbele na nyuma), buzzer ya tahadhari, LED tatu za hali, na button ya kubadilisha mode.

---

✨ Features

Controlling Mode (Kijani 🟢)

· Kuendeshwa kwa simu kwa Bluetooth (Dabble app)
· Kusonga mbele, nyuma, kushoto, kulia
· Kusonga kwa diagonal (mbele-kushoto, mbele-kulia, nyuma-kushoto, nyuma-kulia)
· Kuzuia kugonga mbele (10cm) na nyuma (5cm)
· Buzzer inalia kikwazo kikionekana
· LED ya Njano inawaka kama Bluetooth haija-connect

Automotive Mode (Bluu 🔵)

· Kujiendesha yenyewe bila mtu
· Kukwepa vikwazo automatic
· Kurudi nyuma, kugeuka kushoto/kulia, kisha kuendelea
· Kuzuia kugonga mbele na nyuma
· Bluetooth inazimwa

Zinazofanana kwa Modes Zote

· Kuzuia kugonga mbele (10cm) na nyuma (5cm)
· Buzzer ya tahadhari inayozidi kwa kasi
· LED indicator ya mode
· Double press button kubadilisha mode

---

🧩 Vifaa (Hardware)

Controller

· Arduino Uno × 1

Motor Driver

· Adafruit Motor Shield V2 × 1

Motors

· DC Gear Motor × 4
· Wheel × 4
· Robot Car Chassis × 1
· Caster Wheel × 1

Bluetooth

· HC-05 Bluetooth Module × 1

Sensorer

· HC-SR04 Ultrasonic Sensor × 2

Sauti

· Active Buzzer × 1

LED

· LED Bluu × 1
· LED Kijani × 1
· LED Njano × 1

Resistor

· Resistor 220Ω × 3
· Resistor 1kΩ × 1
· Resistor 2kΩ × 1

Button

· Push Button × 1

Power

· Betri 7.4V–12V × 1
· Betri Holder × 1
· Switch ya Power × 1

Ziada

· Jumper Wires (M-M na M-F)
· Breadboard ndogo
· Screwdriver
· Double-sided Tape
· Cable Ties

---

🔌 Wiring

Arduino Uno + Adafruit Motor Shield V2

```
Arduino Uno + Adafruit Motor Shield V2
┌─────────────────────┐       ┌─────────────────────┐
│ Motor Shield        │──────►│ Arduino Uno         │  Imeunganishwa
│ (juu ya Uno)        │       │ (I2C: A4/A5)        │  moja kwa moja
└─────────────────────┘       └─────────────────────┘
```

Motors

```
Motor ya Mbele Kushoto (FL)   Motor Shield M1       Wire Color
┌─────────────┐       ┌─────────────┐
│ Terminal +  │──────►│ M1 +        │  Nyekundu
│ Terminal −  │──────►│ M1 −        │  Nyeusi
└─────────────┘       └─────────────┘

Motor ya Mbele Kulia (FR)     Motor Shield M2       Wire Color
┌─────────────┐       ┌─────────────┐
│ Terminal +  │──────►│ M2 +        │  Nyekundu
│ Terminal −  │──────►│ M2 −        │  Nyeusi
└─────────────┘       └─────────────┘

Motor ya Nyuma Kushoto (BL)   Motor Shield M3       Wire Color
┌─────────────┐       ┌─────────────┐
│ Terminal +  │──────►│ M3 +        │  Nyekundu
│ Terminal −  │──────►│ M3 −        │  Nyeusi
└─────────────┘       └─────────────┘

Motor ya Nyuma Kulia (BR)     Motor Shield M4       Wire Color
┌─────────────┐       ┌─────────────┐
│ Terminal +  │──────►│ M4 +        │  Nyekundu
│ Terminal −  │──────►│ M4 −        │  Nyeusi
└─────────────┘       └─────────────┘
```

Power

```
Betri (7.4V–12V)              Motor Shield EXT_PWR  Wire Color
┌─────────────┐       ┌─────────────┐
│ Positive +  │──────►│ EXT_PWR +   │  Nyekundu
│ Negative −  │──────►│ EXT_PWR −   │  Nyeusi
└─────────────┘       └─────────────┘
```

HC-05 Bluetooth

```
HC-05 Bluetooth              Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ VCC         │──────►│ 5V          │  Nyekundu
│ GND         │──────►│ GND         │  Nyeusi
│ TX          │──────►│ D10         │  Njano
│ RX          │──[1kΩ]┤ D11         │  Kijani
│             │──[2kΩ]┤ GND         │  Nyeusi
└─────────────┘       └─────────────┘
```

HC-SR04 Mbele

```
HC-SR04 Mbele                Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ VCC         │──────►│ 5V          │  Nyekundu
│ GND         │──────►│ GND         │  Nyeusi
│ Trig        │──────►│ D2          │  Njano
│ Echo        │──────►│ D3          │  Kijani
└─────────────┘       └─────────────┘
```

HC-SR04 Nyuma

```
HC-SR04 Nyuma                Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ VCC         │──────►│ 5V          │  Nyekundu
│ GND         │──────►│ GND         │  Nyeusi
│ Trig        │──────►│ D4          │  Njano
│ Echo        │──────►│ D5          │  Kijani
└─────────────┘       └─────────────┘
```

Buzzer

```
Buzzer (Active)              Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ Positive +  │──────►│ D6          │  Nyekundu
│ Negative −  │──────►│ GND         │  Nyeusi
└─────────────┘       └─────────────┘
```

LED Bluu (Automotive)

```
LED Bluu (Automotive)        Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ Anode (+)   │──────►│ D7          │  Bluu
│ Cathode (−) │──220Ω─►│ GND         │  Nyeusi
└─────────────┘       └─────────────┘
```

LED Kijani (Controlling)

```
LED Kijani (Controlling)     Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ Anode (+)   │──────►│ D8          │  Kijani
│ Cathode (−) │──220Ω─►│ GND         │  Nyeusi
└─────────────┘       └─────────────┘
```

LED Njano (Haija-connect)

```
LED Njano (Haija-connect)    Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ Anode (+)   │──────►│ D9          │  Njano
│ Cathode (−) │──220Ω─►│ GND         │  Nyeusi
└─────────────┘       └─────────────┘
```

Mode Button

```
Mode Button (Double Press)   Arduino Uno           Wire Color
┌─────────────┐       ┌─────────────┐
│ Mguu 1      │──────►│ D12         │  Njano
│ Mguu 2      │──────►│ GND         │  Nyeusi
└─────────────┘       └─────────────┘
```

---

📌 Muhtasari wa Pini

Pini Kifaa
D2 HC-SR04 Mbele — Trig
D3 HC-SR04 Mbele — Echo
D4 HC-SR04 Nyuma — Trig
D5 HC-SR04 Nyuma — Echo
D6 Buzzer (+)
D7 LED Bluu (+)
D8 LED Kijani (+)
D9 LED Njano (+)
D10 HC-05 TX
D11 HC-05 RX (voltage divider)
D12 Mode Button → GND
A4 Motor Shield (SDA)
A5 Motor Shield (SCL)
5V HC-05, HC-SR04 ×2
GND Vifaa vyote

---

📚 Maktaba Zinazohitajika

Maktaba Kutoka
Adafruit Motor Shield V2 Library Manager → tafuta "Adafruit Motor Shield V2"
SoftwareSerial Built-in

---

⚙️ Installation

1. Clone Repository

```bash
git clone https://github.com/luminexa-creator/LumiCarX.git
cd LumiCarX
```

2. Fungua Arduino IDE

· Install Adafruit Motor Shield V2 kutoka Library Manager
· Fungua faili LumiCarX.ino

3. Paki Code

· Chagua Board: Arduino Uno
· Chagua Port sahihi
· Bonyeza Upload

4. Weka Jina la Bluetooth

```
AT
AT+NAME=LumiCarX
AT+PSWD=1234
AT+UART=9600,0,0
```

5. Unganisha Betri

· Weka betri kwenye EXT_PWR ya motor shield
· Washa switch

---

🎮 Jinsi ya Kutumia

Controlling Mode (Kijani 🟢)

1. Washa gari — Kijani inawaka
2. Fungua Dabble app kwenye simu
3. Connect na LumiCarX
4. Njano inazima, Buzzer inanyamaza
5. Endesha gari kwa Dabble

Automotive Mode (Bluu 🔵)

1. Bonyeza button mara 2 → Bluu inawaka
2. Gari linaanza kujiendesha yenyewe
3. Linakwepa vikwazo automatic
4. Bonyeza button mara 2 tena → Kijani inawaka (kurudi Controlling)

---

📱 Bluetooth Commands (Dabble)

Herufi Kazi
F Mbele
B Nyuma
L Geuka Kushoto
R Geuka Kulia
G Mbele-Kushoto
I Mbele-Kulia
H Nyuma-Kushoto
J Nyuma-Kulia
S Simama

---

🚦 LED Indicators

Rangi Maana
🔵 Bluu Automotive Mode
🟢 Kijani Controlling Mode
🟡 Njano Bluetooth haija-connect

---

🔔 Buzzer Behavior

Hali Sauti
Haija-connect BT Beep polepole (500ms)
Mbele 10–7cm Beep taratibu (400ms)
Mbele 7–4cm Beep ya kati (200ms)
Mbele < 4cm Beep kali (80ms)
Nyuma 5–3cm Beep ya kati (200ms)
Nyuma < 3cm Beep kali (80ms)

---

📏 Umbali wa Kuzuia

Sensor Umbali Tabia
Mbele 10 cm Inarudi, inageuka, inaendelea
Nyuma 5 cm Inasimamisha kurudi

---

⚡ Kasi

Mode Kasi
Controlling 150
Automotive 130

---

🛠️ Troubleshooting

Tatizo Suluhisho
Motor haizunguki Angalia EXT_PWR ya shield (betri)
Bluetooth haiconnect Angalia voltage divider kwenye D11
Sensor inasoma vibaya Angalia VCC = 5V, Trig/Echo
LED haiwaki Angalia polarity (mguu mrefu = +)
Button haifanyi kazi Angalia D12 → GND
Gari linaenda kinyume Badilisha FORWARD/BACKWARD kwenye code

---

📄 License

MIT License — huru kutumia, kubadilisha, na kusambaza.

---

👨‍💻 Author

LumiCarX Project

· GitHub: luminexa-creator
· Project Link: https://github.com/luminexa-creator/LumiCarX

---

🙏 Shukrani

· Adafruit kwa Motor Shield V2 library
· Arduino Community
· Dabble app kwa Bluetooth control

---

LumiCarX — Smart Bluetooth Car with 360° Awareness 🚗💨
