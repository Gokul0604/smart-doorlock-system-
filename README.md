Smart Door Lock System - Overview 
  1.A smart door lock system is an advanced security mechanism that allows users to lock and unlock doors electronically, often with enhanced features like remote control, 
  biometric authentication, and integration with smart home systems. Unlike traditional mechanical locks that require physical keys, smart door locks provide more convenient and secure methods of access,
  such as using passcodes, mobile apps, fingerprint scanners, or even voice commands. 
  2.Smart door lock systems offer enhanced security and convenience, replacing traditional keys with innovative digital access methods. They are increasingly popular in modern homes and businesses, 
  contributing to more secure and flexible access control.
Applications: 
  1.Homes: Homeowners use smart locks for convenience, security, and integration with smart home ecosystems. 
  2.Offices: Businesses use smart door locks for controlling access to secure areas, ensuring that only authorized personnel can enter. 
  3.Hotels: Many hotels have adopted smart door locks, allowing guests to access rooms with digital keycards or mobile apps.

Components Used and Pin Connections 
1.Arduino Board 
    The microcontroller used to run the program (e.g., Arduino Uno).

2.4x3 Matrix Keypad 
Used for password input. 
Connections: Rows: 
Row 0 → Digital Pin 1 
Row 1 → Digital Pin 2 
Row 2 → Digital Pin 3 
Row 3 → Digital Pin 4 
Columns: Column 0 → Digital Pin 5 
Column 1 → Digital Pin 6 
Column 2 → Digital Pin 7

3.16x2 LCD Display 
Used to display messages to the user. 
Connections: 
RS (Register Select) → Analog Pin A0 
Enable (E) → Analog Pin A1 
D4 → Analog Pin A2 
D5 → Analog Pin A3 
D6 → Analog Pin A4 
D7 → Analog Pin A5 
VSS → GND VDD → +5V V0 
(Contrast Adjustment) → Middle pin of a 10kΩ potentiometer; 
other two pins connected to +5V and GND.

4.Servo Motor 
Controls the locking and unlocking mechanism of the door. 
Connections: 
Control Signal Wire (usually white or yellow) → Digital Pin 9 
Power Wire (red) → +5V (may require an external power source if current draw is high) 
Ground Wire (black or brown) → GND

Code Flow:
  1.Startup: The servo motor closes the door, and the LCD shows a welcome message.
  2.Password Entry: The user enters the password via the keypad. The LCD shows each key press and press # key to verify the password.
  3.Password Validation: l) If the entered password matches the master password (090604), the servo opens the door. ll) If the password is incorrect, the LCD displays "Wrong Password", and the door remains closed.
  4.Closing the Door: Once the door is open, pressing the # key closes the door again by moving the servo to the locked position.
