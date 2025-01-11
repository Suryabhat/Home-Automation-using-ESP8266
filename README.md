# Home-Automation-using-ESP8266
# Arduino IoT Cloud Control for 4 Relays using NodeMCU

## Overview
This project demonstrates how to control four relays connected to a NodeMCU ESP8266 using Arduino IoT Cloud. The relays can be controlled both manually via physical switches and remotely through the IoT Cloud dashboard. Additionally, the WiFi connection status is indicated by an LED.

---

## Features
- **Remote Control**: Manage 4 relays using the Arduino IoT Cloud dashboard.
- **Manual Control**: Toggle relays using physical push-button switches.
- **WiFi Status Indicator**: An LED shows the current WiFi connection status.
- **Arduino IoT Cloud Integration**: Easily control and monitor the relays via the cloud.

---

## Components Required
1. NodeMCU ESP8266
2. 4-Channel Relay Module
3. Push-Button Switches (4 units)
4. WiFi Indicator LED (optional)
5. Resistors (as needed)
6. Connecting wires
7. Breadboard or PCB for assembly

---

## Installation & Setup

### Step 1: Configure Arduino IDE
1. Open the Arduino IDE.
2. Go to **File > Preferences**.
3. Add the following URLs under **Additional Boards Manager URLs**:
   - `https://dl.espressif.com/dl/package_esp32_index.json`
   - `http://arduino.esp8266.com/stable/package_esp8266com_index.json`
4. Install the NodeMCU ESP8266 board:
   - Go to **Tools > Board > Boards Manager**.
   - Search for "ESP8266" and install the appropriate package.

### Step 2: Install Required Libraries
1. Install the **ArduinoIoTCloud** library and its dependencies.
   - Go to **Sketch > Include Library > Manage Libraries**.
   - Search for "ArduinoIoTCloud" and click "Install."

### Step 3: Add Your WiFi and Device Credentials
Update the following values in the code:
- `SECRET_SSID`: Your WiFi network name.
- `SECRET_PASS`: Your WiFi password.
- `SECRET_DEVICE_KEY`: The secret device key from your Arduino IoT Cloud setup.

### Step 4: Hardware Connections
| NodeMCU Pin | Component        | Description            |
|-------------|------------------|------------------------|
| D1 (GPIO5)  | Relay 1          | Control relay 1        |
| D2 (GPIO4)  | Relay 2          | Control relay 2        |
| D5 (GPIO14) | Relay 3          | Control relay 3        |
| D6 (GPIO12) | Relay 4          | Control relay 4        |
| SD3 (GPIO10)| Switch 1         | Manual toggle relay 1  |
| D3 (GPIO0)  | Switch 2         | Manual toggle relay 2  |
| D7 (GPIO13) | Switch 3         | Manual toggle relay 3  |
| RX (GPIO3)  | Switch 4         | Manual toggle relay 4  |
| D0 (GPIO16) | WiFi LED         | Indicates WiFi status  |

### Step 5: Upload the Code
1. Connect the NodeMCU to your computer via USB.
2. Select the correct board and port from **Tools > Board/Port**.
3. Upload the code to the NodeMCU.

---

## Usage Instructions
1. Power up the NodeMCU and ensure it connects to WiFi.
2. Access the Arduino IoT Cloud dashboard to control the relays remotely.
3. Use the physical push-button switches for manual relay control.
4. Observe the WiFi status LED for connection feedback:
   - ON: Connected to WiFi
   - OFF: Not connected to WiFi

---

## How It Works
1. **Cloud Integration**: The Arduino IoT Cloud interface is used to monitor and control the relays. Changes made on the dashboard trigger respective relay actions via the `onSwitchXChange()` functions.
2. **Manual Control**: Physical switches toggle the relays locally using the `manual_control()` function.
3. **WiFi Status Monitoring**: The `wifiLed` pin indicates the WiFi connection status.

---

## Links & Resources
- [YouTube Video Demonstration](https://youtu.be/UtReFcOLJx8)
- [Related Blog](https://iotcircuithub.com/esp8266-projects/)
- [ESP8266 Board Package](https://github.com/esp8266/Arduino)

---

## License
This project is provided "as-is" for educational purposes. For any commercial use, please contact the original author or contributor.

---

## Author
- **Tech StudyCell**  
For inquiries or further assistance, feel free to reach out or visit the linked resources above.

