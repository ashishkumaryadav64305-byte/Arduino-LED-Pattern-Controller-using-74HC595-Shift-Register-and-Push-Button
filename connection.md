Connections

This document explains all hardware connections used in the Arduino LED Pattern Controller using the 74HC595 Shift Register and Push Button.

---

1. Arduino to 74HC595 Connections

Arduino Uno Pin| 74HC595 Pin| Pin Number| Purpose
D11| DS| 14| Serial Data Input
D12| SH_CP| 11| Shift Clock
D8| ST_CP| 12| Latch Clock
5V| VCC| 16| Power Supply
GND| GND| 8| Ground
GND| OE| 13| Enable Outputs (Active LOW)
5V| MR| 10| Disable Reset (Active HIGH)

---

2. 74HC595 to LED Connections

74HC595 Output| Pin Number| Connected To
Q0| 15| LED 1
Q1| 1| LED 2
Q2| 2| LED 3
Q3| 3| LED 4
Q4| 4| LED 5
Q5| 5| LED 6
Q6| 6| LED 7
Q7| 7| LED 8

Each LED connection is:

74HC595 Output → 220 Ω Resistor → LED Anode (Long Leg)

LED Cathode (Short Leg) → GND

---

3. Push Button Connection

Push Button Terminal| Connected To
Terminal 1| Arduino D2
Terminal 2| GND

The Arduino uses:

pinMode(buttonPin, INPUT_PULLUP);

This means:

- Button released → Arduino reads HIGH
- Button pressed → Arduino reads LOW

No external pull-up resistor is required.

---

4. Power Connections

Source| Destination
Arduino 5V| Pin 16 (VCC)
Arduino 5V| Pin 10 (MR)
Arduino GND| Pin 8 (GND)
Arduino GND| Pin 13 (OE)

---

5. Data Flow

1. Arduino creates the LED pattern.
2. Data is sent to DS (Pin 14).
3. SH_CP (Pin 11) shifts the data into the register.
4. ST_CP (Pin 12) updates all LED outputs together.
5. The LEDs display the selected pattern.
6. Pressing the push button changes the active pattern.

---

Important Notes

- Always connect Pin 13 (OE) to GND to enable the outputs.
- Always connect Pin 10 (MR) to 5V to prevent unwanted resets.
- Use a 220 Ω resistor with every LED.
- Ensure the 74HC595 is inserted in the correct orientation before powering the circuit.
- Disconnect power immediately if the IC becomes unusually hot and check the wiring.

---

Connection Summary

- D11 → DS (Pin 14)
- D12 → SH_CP (Pin 11)
- D8 → ST_CP (Pin 12)
- D2 → Push Button
- 5V → VCC (Pin 16)
- 5V → MR (Pin 10)
- GND → GND (Pin 8)
- GND → OE (Pin 13)
- Q0–Q7 → 220 Ω Resistors → LEDs → GND
