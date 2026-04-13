from weasyprint import HTML

# Content for the README.md in a text format
readme_content = """# NeuroGlove: EEG-Powered Pneumatic Hand Rehabilitation System

![Project Header](https://raw.githubusercontent.com/ersozberk/eeg_robotic_glove/main/eeg.png)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/Build-Success-brightgreen.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Arduino%20%7C%20Python-blue.svg)]()

**NeuroGlove** is an innovative Assistive Technology (AT) solution designed for patients with hemiplegia or hand paralysis. By utilizing Brain-Computer Interface (BCI) technology, this system decodes neural oscillations via EEG and translates them into physical movement through a soft-robotic pneumatic glove.

## 🚀 Key Features

* **Real-time BCI Integration:** Seamlessly decodes brainwave patterns using NeuroSky MindWave.
* **Pneumatic Actuation:** Provides gentle, high-torque finger extension and flexion.
* **Wireless Connectivity:** Integrated Bluetooth (HC-05/06) communication for a tether-free experience.
* **Adaptive Signal Processing:** Python-based filtering of EEG data for accurate motor-intent detection.

---

## 🛠 Hardware Architecture

The system architecture is divided into three main layers: Signal Acquisition, Processing, and Actuation.

| Component | Function |
| :--- | :--- |
| **NeuroSky MindWave** | EEG signal sensing (Focus/Meditation metrics). |
| **Arduino Uno** | Master controller for solenoid valves and pump logic. |
| **HC-05/06 Bluetooth** | Low-latency serial data transmission. |
| **Pneumatic Pump & Valves** | Soft-robotic drive system for finger movement. |
| **Soft Robotic Glove** | Ergonomic interface for the user's hand. |

---

## 💻 Software Stack

### Prerequisites

* **Python 3.8+**
* **Arduino IDE**
* **Libraries:** `pyserial`, `neuropy` (or relevant BCI library).

### Installation

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/ersozberk/eeg_robotic_glove.git](https://github.com/ersozberk/eeg_robotic_glove.git)
    cd eeg_robotic_glove
    ```

2.  **Setup Python Environment:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Deploy Arduino Firmware:**
    * Open `Firmware/eeg_control.ino` in Arduino IDE.
    * Select your board and upload the code.

4.  **Run the System:**
    ```bash
    python Scripts/eeg_processor.py
    ```

---

## ⚙️ How It Works

1.  **Data Acquisition:** The EEG headset monitors **Beta** and **Alpha** waves associated with concentration.
2.  **Signal Processing:** The Python script processes the raw data stream, filtering noise and detecting "Attention" thresholds.
3.  **Command Execution:** Once the threshold is met, a trigger signal is sent via Bluetooth to the Arduino.
4.  **Physical Response:** The Arduino activates the pneumatic pump, inflating the glove's chambers to facilitate hand movement.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

Distributed under the **MIT License**. See `LICENSE` for more information.

## 📧 Contact

**Berk Ersöz** - [GitHub Profile](https://github.com/ersozberk)

---
*Developed for accessibility and rehabilitation.*
"""

with open("README_CONTENT.txt", "w", encoding="utf-8") as f:
    f.write(readme_content)
