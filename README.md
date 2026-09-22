Arduino LED Pattern Controller using 74HC595 Shift Register and Push Button

📌 Project Overview

This project demonstrates how to control 8 LEDs using only three Arduino digital pins with the help of the 74HC595 Shift Register IC. A push button is used to switch between multiple LED patterns, making the project interactive while reducing the number of Arduino output pins required.

The project introduces the concepts of serial-to-parallel communication, GPIO expansion, and embedded systems programming using Arduino.

---

🎯 Objective

- Learn how a 74HC595 Shift Register works.
- Control 8 LEDs using only 3 Arduino pins.
- Interface a push button with Arduino.
- Create multiple LED animation patterns.
- Understand serial communication using the "shiftOut()" function.

---

🛠 Components Used

- Arduino Uno (ATmega328P)
- 74HC595 Shift Register IC
- 8 × LEDs
- 8 × 220 Ω Resistors
- Push Button
- Breadboard
- Jumper Wires
- USB Cable

---

🔌 Pin Connections

Arduino → 74HC595

Arduino| 74HC595
D11| DS (Pin 14)
D12| SH_CP (Pin 11)
D8| ST_CP (Pin 12)
5V| VCC (Pin 16)
5V| MR (Pin 10)
GND| GND (Pin 8)
GND| OE (Pin 13)

Push Button

- One terminal → Arduino D2
- Other terminal → GND
- Configured using "INPUT_PULLUP"

LED Connections

- Q0 (Pin 15) → LED1
- Q1 (Pin 1) → LED2
- Q2 (Pin 2) → LED3
- Q3 (Pin 3) → LED4
- Q4 (Pin 4) → LED5
- Q5 (Pin 5) → LED6
- Q6 (Pin 6) → LED7
- Q7 (Pin 7) → LED8

Each LED is connected through a 220 Ω resistor.

---

⚙ Features

- Control 8 LEDs using only 3 Arduino pins.
- Interactive push button control.
- Multiple LED animation modes.
- Uses Arduino "shiftOut()" function.
- Easy to expand by cascading more 74HC595 ICs.

---

💡 Working Principle

The Arduino sends serial data to the 74HC595 through the Data (DS) pin. The Clock (SH_CP) shifts each bit into the register, and the Latch (ST_CP) updates all outputs simultaneously. The push button changes the animation mode, and the LEDs display the selected pattern.

---

▶ LED Patterns

- Running LED (Left → Right)
- Running LED (Right → Left)
- Blink All LEDs
- Alternate LEDs

---

🚀 Applications

- LED Display Systems
- Digital Counters
- Industrial Indicators
- Embedded Systems
- Educational Electronics Projects
- GPIO Expansion

---

📚 Skills Learned

- Arduino Programming
- Embedded Systems
- Digital Electronics
- Shift Registers
- Push Button Interfacing
- Breadboard Prototyping
- Circuit Debugging

---

🔍 Troubleshooting

- Verify Pin 16 is connected to 5V.
- Verify Pin 8 is connected to GND.
- Connect Pin 13 (OE) to GND.
- Connect Pin 10 (MR) to 5V.
- Use a 220 Ω resistor with every LED.
- Check IC orientation before powering the circuit.
- If the IC becomes hot, disconnect power immediately and inspect the wiring.

---

📈 Future Improvements

- Add an OLED/LCD display.
- Add a buzzer for sound effects.
- Control LEDs using Bluetooth or Wi-Fi.
- Cascade multiple 74HC595 ICs to control more LEDs.
- Add IoT monitoring using an ESP32.

---

👨‍💻 Author

Ashish Yadav

Electrical & Electronics Engineering (EEE)

Arka Jain University

---

⭐ If you found this project useful, consider giving it a star on GitHub.
