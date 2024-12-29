# Arduino-RFID-Access-Control-with-Servo-LCD-LEDs-and-Buzzer-using-Arduino---Full-Tutorial
# Arduino RFID Access Control System

## Overview
This project demonstrates how to build an RFID-based access control system using Arduino. The system integrates an RFID reader, servo motor, 16x2 LCD (I2C), three LEDs (Red, Yellow, Green), and a piezo buzzer to provide visual and auditory feedback.

---

## Components
| **Component**         | **Quantity** | **Description**                                           |
|------------------------|--------------|-----------------------------------------------------------|
| Arduino Uno            | 1            | Microcontroller for controlling the project              |
| RFID Reader (RC522)    | 1            | Reads RFID card/tag for access control                   |
| Servo Motor (SG90)     | 1            | Acts as a lock (opens and closes based on access)        |
| 16x2 LCD (I2C)         | 1            | Displays access messages                                 |
| LEDs                   | 3            | Red, Yellow, and Green to indicate status                |
| Piezo Buzzer (2-pin)   | 1            | Provides auditory feedback                               |
| Resistors (220Ω)       | 3            | Used with LEDs to limit current                          |
| Breadboard             | 1            | For organizing connections                               |
| Jumper Wires           | Several      | For connecting components to the Arduino                |

---

## Connections
| **Component**        | **Pin**        | **Arduino Pin** |
|-----------------------|----------------|------------------|
| **RFID Module (RC522)** | SDA            | D10              |
|                       | SCK            | D13              |
|                       | MOSI           | D11              |
|                       | MISO           | D12              |
|                       | IRQ            | Not Connected    |
|                       | GND            | GND              |
|                       | RST            | D9               |
|                       | 3.3V           | 3.3V             |
| **Servo Motor (SG90)** | Signal         | D6               |
|                       | VCC            | 5V               |
|                       | GND            | GND              |
| **LCD (I2C)**         | VCC            | 5V               |
|                       | GND            | GND              |
|                       | SDA            | A4               |
|                       | SCL            | A5               |
| **LEDs**              | Red LED        | D3               |
|                       | Yellow LED     | D4               |
|                       | Green LED      | D5               |
|                       | GND            | GND via 220Ω Resistor |
| **Piezo Buzzer**      | Positive       | D7               |
|                       | Negative       | GND              |

---

## Functionality
1. **RFID Module**: Reads the UID from an RFID tag/card.
   - If the UID matches the authorized UID, access is granted.
2. **Servo Motor**: Unlocks for 3 seconds when access is granted, then locks again.
3. **LEDs**:
   - **Green LED**: Lights up for successful access.
   - **Red LED**: Lights up for denied access.
   - **Yellow LED**: Indicates system status.
4. **LCD**: Displays messages ("Access Granted" or "Access Denied").
5. **Buzzer**: 
   - Short beep for granted access.
   - Long beep for denied access.

---

## Steps to Build
1. **Connect Components**:
   - Use the connection table to wire all components to the Arduino.
2. **Install Libraries**:
   - Install the following libraries in the Arduino IDE:
     - `MFRC522` for the RFID module.
     - `Servo` for controlling the servo motor.
     - `LiquidCrystal_I2C` for the LCD.
3. **Upload Code**:
   - Replace the placeholder UID in the code with the UID of your RFID card/tag.
   - Upload the code using the Arduino IDE.
4. **Test the System**:
   - Scan RFID cards/tags to verify the system functionality.

---

## Notes
- Ensure the RFID tag/card UID matches the authorized UID in the code.
- Use the potentiometer on the I2C LCD module to adjust the display contrast.

---

## License
This project is open-source and can be freely used for educational purposes.

I demonstrate how to build an RFID-based access control system using Arduino! This project integrates an RFID reader (RC522), servo motor, 16x2 I2C LCD, three LEDs (Red, Yellow, Green), and a 2-pin piezo buzzer.
Here’s a project that integrates an RFID reader, a servo motor, an LCD, 3 LEDs, and a 2-pin piezo buzzer with Arduino. This setup can be used to create an access control system where the RFID reader identifies a card/tag, the servo motor acts as a lock, the LEDs indicate status, and the buzzer sounds feedback.

Components Required:
Arduino Uno
RFID Reader (RC522)
Servo Motor (SG90 or similar)
16x2 LCD (I2C or parallel interface)
3 LEDs (Red, Yellow, Green)
Piezo Buzzer (2 pins)
Resistors (220Ω for LEDs)
Jumper wires
Breadboard
Wiring Diagram
1. RFID Module (RC522):
RFID Pin	Arduino Pin
SDA	D10
SCK	D13
MOSI	D11
MISO	D12
IRQ	Not Connected
GND	GND
RST	D9
3.3V	3.3V
2. Servo Motor:
Servo Pin	Arduino Pin
Signal	D6
VCC	5V
GND	GND
3. LCD (I2C):
LCD Pin	Arduino Pin
VCC	5V
GND	GND
SDA	A4
SCL	A5
4. LEDs:
LED	Arduino Pin
Red LED	D3
Yellow LED	D4
Green LED	D5
(Place a 220Ω resistor between each LED and GND.)

5. Piezo Buzzer (2-pin):
Buzzer Pin	Arduino Pin
Positive	D7
Negative	GND
Explanation:
RFID Reader: The code reads the UID from the RFID card. If the UID matches the authorized UID, it grants access.
Servo Motor: If the card is authorized, the servo moves to the unlock position (90°) for 3 seconds and then locks again.
LEDs: The green LED indicates successful access, while the red LED indicates failure.
LCD: Displays messages such as "Access Granted" or "Access Denied."
Buzzer: Gives auditory feedback, with a short beep for granted access and a longer one for denied access.
Make sure to:
Install the necessary libraries (MFRC522, Servo, LiquidCrystal_I2C).
Test with your RFID tag UID by replacing the UID in the code.
Let me know if you need further adjustments!
