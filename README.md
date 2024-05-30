# RFID Card Reader with OLED Display and Servo Motor Control

This project demonstrates an RFID card reader system using an Arduino microcontroller, an OLED display (SSD1306), an RFID module (MFRC522), and a servo motor. When an RFID card is scanned, the system reads the card's unique identifier (UID), matches it with pre-stored card data, displays a personalized greeting message on the OLED screen, and rotates a servo motor accordingly.

## Components Used
- Arduino board (e.g., Arduino Uno)
- OLED display (128x64 pixels, I2C interface)
- RFID module (MFRC522)
- Servo motor
- Jumper wires

## Setup Instructions
1. Connect the components as per the circuit diagram.
2. Upload the provided Arduino sketch to your Arduino board.
3. Ensure that necessary libraries are installed: Adafruit GFX, Adafruit SSD1306, MFRC522, and Servo.

## Code Overview
The Arduino sketch consists of the following main components:

### Libraries and Constants
- Includes necessary libraries for OLED display, RFID module, and servo control.
- Defines constants for pin configurations and screen dimensions.

### RFID Card Structure
- Defines a structure to hold RFID card data, including UID and cardholder name.

### Stored RFID Card Data
- Stores RFID card data (UID and name) in an array.

### Servo Initialization
- Initializes the servo motor.

### Setup Function
- Initializes serial communication, I2C, OLED display, SPI, RFID module, and servo motor.
- Prints a setup message to the serial monitor.

### Loop Function
- Continuously checks for the presence of a new RFID card.
- Reads the serial number of the card and matches it with stored card data.
- Displays a personalized greeting message on the OLED display.
- Rotates the servo motor accordingly.
- Halt communication with the RFID card after processing.

## Usage
1. Power on the Arduino system.
2. Place an RFID card near the RFID module.
3. The OLED display will show a personalized greeting message.
4. The servo motor will rotate momentarily as per the predefined action.
5. The system will wait for the next RFID card scan.

## Contributing
Contributions are welcome! For major changes, please open an issue first to discuss the proposed changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
