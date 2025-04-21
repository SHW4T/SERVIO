# SERVIO: Door Security System with Telegram Alerts

This project is a smart door security system built using the ESP32-CAM module, PIR motion sensor, and ultrasonic sensor. It detects motion or nearby objects and automatically captures photos, sending them to a Telegram bot for real-time alerts.

---

## Features

- **Motion Detection:** Uses a PIR sensor to detect human movement near the door.
- **Object Detection:** Ultrasonic sensor detects objects within 10 cm range.
- **Instant Photo Capture:** ESP32-CAM captures images when motion or objects are detected.
- **Telegram Integration:** Sends captured images and alerts directly to a Telegram bot.
- **Flash LED Control:** Flash LED can be toggled via Telegram commands.
- **Command-Based Photo:** Users can request a photo via Telegram command `/photo`.
- **Secure Access:** Only authorized Telegram chat ID receives alerts and commands.

---

## Hardware Components

- ESP32-CAM Module (AI Thinker model)
- PIR Motion Sensor
- Ultrasonic Sensor (HC-SR04 or compatible)
- Flash LED (connected to GPIO 4)
- WiFi Network

---

## Software & Libraries

- Arduino IDE
- UniversalTelegramBot library
- ArduinoJson
- NewPing (for ultrasonic sensor)
- ESP32 Camera driver

---

## Setup Instructions

1. **Clone the repository:**
2. **Configure WiFi and Telegram Bot:**

- Replace `ssid` and `password` with your WiFi credentials.
- Replace `BOTtoken` with your Telegram bot token.
- Replace `CHAT_ID` with your Telegram chat ID.

3. **Connect the hardware:**

- Connect PIR sensor to GPIO 15.
- Connect ultrasonic sensor trigger and echo pins to GPIO 13 and 12 respectively.
- Connect flash LED to GPIO 4.
- Connect the ESP32-CAM module as per AI Thinker pin configuration.

4. **Upload the code:**

- Use Arduino IDE with ESP32 board support installed.
- Select the appropriate board and COM port.
- Upload the sketch.

5. **Use the Telegram bot:**

- Send `/start` to the bot to get welcome message.
- Use `/photo` to request a photo manually.
- Use `/flash` to toggle the flash LED.

---

## Notes

- The system sends alerts and photos only to the authorized Telegram chat ID.
- Photo capture and sending may experience delays depending on network quality.
- Ensure your ESP32-CAM has sufficient power and WiFi connectivity for reliable operation.

---

## Team Members

- SHASHWAT THAKUR (me)
- NEIL SHIRKE
- JAS SHROFF

---

## Demo Video

Watch the demo video on [LinkedIn](https://www.linkedin.com/posts/shwat_iot-esp32-homesecurity-activity-7319788802217025608-u4oi?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFheUKYBKwZZDEvvdUkR3gMmMJ6eP8me_zg) to see the system in action

*Note: The response in the video is slower than usual due to network issues during recording.*

---

## License

This project is licensed under the MIT License.

---

## Acknowledgements

- UniversalTelegramBot library by @witnessmenow
- NewPing library by Tim Eckel
- ESP32 Camera driver by Espressif



