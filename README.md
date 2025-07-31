# Temp Smart Fan Project 🌡️🌀

The **Temp Smart Fan** is an automated temperature-controlled system that adjusts fan activity based on room temperature. Using a TMP36 temperature sensor, the Arduino reads the current temperature and activates a DC fan when it gets too warm—just like a real smart cooling system. It also includes a push button for manual control and an LED indicator to show system status.

---

## 📦 Components

- Arduino Uno (or compatible)
- Breadboard
- TMP36 temperature sensor
- DC fan (5V or 9V)
- TIP120 transistor (for switching fan)
- 1N4001 diode (for flyback protection)
- 9V battery + battery connector
- LED (status indicator)
- Push button (manual control)
- Resistors:
  - 220Ω (for LED)
  - 10kΩ (pull-down for button)
- Jumper wires
- USB cable (for programming)

---

## 🔧 Installation & Setup

1. **Build the circuit:**
   - Connect the **TMP36** sensor to 5V, GND, and an analog input (e.g., A0).
   - Connect the **TIP120** transistor:
     - Base → Arduino digital pin (through a 1kΩ resistor, if needed)
     - Collector → negative wire of the fan
     - Emitter → GND
   - Connect the **fan's positive lead** to the **9V battery’s positive terminal**.
   - Place the **1N4001 diode** across the fan terminals (cathode to +) for flyback protection.
   - Wire the **push button** to a digital input with a 10kΩ pull-down resistor.
   - Connect the **LED** to a digital pin (e.g., pin 13) with a 220Ω resistor.

2. **Upload the code:**
   - Open the Arduino IDE.
   - Write or paste the sketch that reads temperature, controls the fan, and handles button input.
   - Select your board and port.
   - Click **Upload** to program your Arduino.

---

## 💡 How It Works

- The **TMP36** sensor reads the ambient temperature and sends an analog voltage to the Arduino.
- The Arduino converts this voltage to Celsius and checks if the temperature exceeds a set threshold (e.g., 25°C).
- If the temperature is too high:
  - The **TIP120** transistor switches on, powering the fan from the 9V battery.
  - The **LED** turns on to indicate active cooling.
- If the temperature drops below the threshold, the fan and LED turn off.
- A **push button** can manually override or toggle the fan state, depending on the code logic.

---

## 🖼️ Images / Videos

> *(Insert your project media here to show it in action.)*  
Examples:
- `images/temp-smart-fan-setup.jpg`
- `videos/temp-smart-fan-demo.mp4`

---

## 🔗 Simulation Links

- [Tinkercad Simulation (if available)](https://www.tinkercad.com/)  
> *Paste your link here if you built a virtual version of the project.*

---

## 🙌 Credits

**Created by:** Zahara BG  
Inspired by home automation and real-world HVAC control systems.  
Special thanks to online Arduino communities for tutorials on sensor reading and transistor switching.

---

> *To upgrade this project, consider adding an LCD display to show real-time temperature or using a relay for larger fans.*
