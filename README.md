# Temp Smart Fan Project 🌡️🌀

The Temp Smart Fan is an automated, temperature-controlled system that adjusts fan activity based on room temperature. Using a TMP36 temperature sensor, the Arduino reads current conditions and activates a DC fan when it gets too warm—just like a basic smart cooling system. A push button allows for manual override, and an LED indicator shows system status.

---

## 📦 Components

- Arduino Uno (or compatible)
- Breadboard
- TMP36 temperature sensor
- DC fan (5V or 9V)
- TIP120 transistor (for switching the fan)
- 1N4001 diode (flyback protection)
- 9V battery + connector
- LED (status indicator)
- Push button (manual control)
- Resistors:
  - 220Ω (for LED)
  - 10kΩ (pull-down for button)
- Jumper wires
- USB cable (for power/programming)

---

## 🔧 Installation & Setup

### 1. Build the Circuit

**Temperature Sensor (TMP36):**
- VCC → 5V  
- GND → GND  
- OUT → Analog pin A0  

**Fan Control (with TIP120):**
- Base → Digital pin (e.g., pin 9) through a 1kΩ resistor  
- Collector → Fan negative lead  
- Emitter → GND  
- Fan positive lead → 9V battery positive  
- 1N4001 diode across fan terminals (cathode to +)  

**LED (Status Indicator):**
- Anode → Digital pin (e.g., pin 13) through a 220Ω resistor  
- Cathode → GND  

**Push Button (Manual Control):**
- One leg → Digital input pin (e.g., pin 2)  
- Other leg → GND  
- 10kΩ pull-down resistor on input pin  

### 2. Upload the Code

- Open the Arduino IDE.
- Paste or write your sketch (temperature reading, fan logic, manual control).
- Select your board and port.
- Upload the code.

---

## 💡 How It Works

1. The TMP36 reads ambient temperature and sends analog voltage to the Arduino.
2. The Arduino calculates the temperature in Celsius.
3. If the temperature exceeds a set threshold (e.g., 25°C):
   - The transistor activates and powers the fan.
   - The LED turns on to show the fan is active.
4. When the temperature drops below the threshold:
   - The fan and LED turn off.
5. The push button can be used to override automatic control (depends on your code logic).

---

## 🖼️ Circuit Overview

*Include a diagram or photo of your breadboard setup here.*

![Smart Fan Circuit](./your-image-name.png)

---

## 🔗 Simulation Links

- [Tinkercad Simulation](https://www.tinkercad.com/)  
*(Paste your exact link here if available.)*

---

## 🙌 Credits

**Created by:** Zahara BG  
A mini cooling system with both brains and a button.
