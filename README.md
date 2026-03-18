# Arduino LED Animation Modes (Timer1 CTC)

This project demonstrates multiple LED animation patterns using Arduino with **Timer1 in CTC mode** and a **button for mode switching**.

## 🚀 Features

* 3 LED animation modes:

  * **Mode 1:** Sequential (one LED at a time)
  * **Mode 2:** Ping-Pong (back and forth movement)
  * **Mode 3:** Pyramid (accumulating LEDs)
* Button-based mode switching (edge detection)
* Accurate timing using **Timer1 (CTC mode)**
* Clean and simple embedded logic

---

## 🔧 Hardware Requirements

* Arduino (Uno/Nano)
* 4 LEDs
* 4 resistors (220Ω recommended)
* 1 push button
* Breadboard & jumper wires

---

## ⚙️ Pin Configuration

| Component | Pin |
| --------- | --- |
| LED 1     | 2   |
| LED 2     | 3   |
| LED 3     | 4   |
| LED 4     | 5   |
| Button    | 7   |

---

## 🧠 How It Works

* Timer1 generates a **1-second interrupt**
* Each tick updates animation step
* Button uses **edge detection** to switch modes
* Logic is based on:

  * `i == step` → single LED
  * `i < step` → pyramid effect
  * `direction` → ping-pong movement

---

## 🎮 Modes Preview

### Mode 1: Sequential

```
[1 0 0 0]
[0 1 0 0]
[0 0 1 0]
[0 0 0 1]
```

### Mode 2: Ping-Pong

```
1 → 2 → 3 → 4 → 3 → 2 → 1
```

### Mode 3: Pyramid

```
1
1 2
1 2 3
1 2 3 4
1 2 3
1 2
1
```

---

## 📌 Concepts Used

* Timer1 (CTC mode)
* Interrupts (ISR)
* Edge Detection
* State-based logic
* LED animation patterns

---

## 💡 Author

Created by **Bekmurod360**

---

## ⭐️ Notes

This project is great for learning:

* Embedded systems basics
* Real-time programming
* Hardware control with Arduino

Feel free to improve and expand 🚀
