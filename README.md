# WIFI-Deauther



## Overview
WiFi-Deauther is a custom-built project that allows you to perform deauthentication attacks, packet monitoring, and additional functionalities using an ESP8266 module.

![WiFi-Deauther Front View](image1_link_here)
![WiFi-Deauther Side View](image2_link_here)

> **Disclaimer:** This project is intended for educational and security testing purposes only. Use it responsibly and ensure you have permission before testing on any network.

## Features
- **Deauthentication Attacks**: Disconnect devices from a Wi-Fi network by sending deauth packets.
- **Packet Monitoring**: Sniff Wi-Fi packets for analysis.
- **Clock Display**: A real-time clock function.
- **OLED Display**: Shows status and menu options.
- **Button Controls**: Navigate and interact with the device.
- **External Antenna Support**: Enhances signal strength.

## Hardware Requirements
- **ESP8266 Development Board** (e.g., NodeMCU, Wemos D1 Mini)
- **OLED Display** (SSD1306 0.96" I2C)
- **Push Buttons** (4x tactile push buttons)
- **Antenna** (2.4GHz Wi-Fi SMA antenna)
- **Battery (Optional)** (Li-ion 3.7V for portable use)
- **Custom PCB (Optional)** for better integration

## Software Requirements
- **Arduino IDE** (Recommended for flashing firmware)
- **ESP8266 Board Package**
- **Required Libraries**:
  - ESP8266WiFi
  - Adafruit_GFX
  - Adafruit_SSD1306
  - ArduinoJSON

## Installation & Setup
### Step 1: Install ESP8266 Board Package
1. Open **Arduino IDE**.
2. Go to **File > Preferences**.
3. Add the following URL under "Additional Board Manager URLs":
   ```
   http://arduino.esp8266.com/stable/package_esp8266com_index.json
   ```
4. Go to **Tools > Board > Board Manager**.
5. Search for **ESP8266** and install the package.

### Step 2: Install Required Libraries
1. Open **Arduino IDE**.
2. Go to **Sketch > Include Library > Manage Libraries**.
3. Search and install the following:
   - Adafruit GFX
   - Adafruit SSD1306
   - ESP8266WiFi
   - ArduinoJSON

### Step 3: Flash the Firmware
1. Clone the project repository:
   ```sh
   git clone https://github.com/yourrepo/WiFi-Deauther.git
   cd WiFi-Deauther
   ```
2. Open the project in **Arduino IDE**.
3. Select the correct **Board** (e.g., NodeMCU 1.0 or Wemos D1 Mini).
4. Select the correct **Port**.
5. Click **Upload**.

### Step 4: Connect to the Device
1. After flashing, the ESP8266 will create a Wi-Fi network named `pwned` (default SSID).
2. Connect to `pwned` and open `http://192.168.4.1` in a web browser.
3. Use the web interface to control the device.

## Usage Guide
### 1. Using the OLED Display and Buttons
- **Navigation**: Use the buttons to navigate the menu.
- **Select Options**: Press the button to confirm.
- **Start Deauth Attack**: Select the target network and start the attack.
- **Packet Monitor**: View real-time Wi-Fi packets.
- **Clock Mode**: View time and battery status (if supported).

### 2. Using the Web Interface
- Connect to `pwned` Wi-Fi.
- Open `http://192.168.4.1` in a browser.
- Control deauthentication attacks and other features.

## Troubleshooting
### Problem: ESP8266 Not Showing Wi-Fi Network
- Ensure the firmware is correctly flashed.
- Check if the ESP8266 board is powered properly.
- Try resetting the device.

### Problem: Cannot Connect to `pwned`
- Restart your device and try again.
- Make sure you are not too far from the ESP8266.

### Problem: Deauth Attack Not Working
- Some routers have protection against deauthentication attacks.
- Try different Wi-Fi channels.

## Legal Notice
Deauthentication attacks are illegal in many countries if used without authorization. Use this tool only for educational purposes and security testing on networks you own or have explicit permission to test.

## Credits
- Developed using **ESP8266, Arduino IDE, and Adafruit libraries**.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

