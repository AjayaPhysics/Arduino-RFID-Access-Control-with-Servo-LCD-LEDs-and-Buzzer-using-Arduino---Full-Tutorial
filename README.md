# Arduino-RFID-Access-Control-with-Servo-LCD-LEDs-and-Buzzer-using-Arduino---Full-Tutorial
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
