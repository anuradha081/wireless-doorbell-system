# 🔔 Wireless Doorbell System

An Arduino-based **Wireless Doorbell System** that uses **433 MHz RF communication** to transmit a doorbell signal wirelessly from a push-button transmitter unit to a receiver unit that activates a buzzer.

The project demonstrates practical concepts of **Arduino programming, RF communication, digital signal processing, and real-time embedded systems**.

## 📌 Project Overview

Traditional doorbells require physical wiring between the switch and indoor unit. This project eliminates the need for wired connections by using **433 MHz RF transmitter and receiver modules**.

When the doorbell push button is pressed:

**Push Button → Arduino Transmitter → 433 MHz RF Transmission → RF Receiver → Arduino Receiver → Buzzer**

The system successfully demonstrates wireless communication over an approximate range of **10–50 meters**, depending on environmental conditions and antenna quality.

## ✨ Features

* 🔔 Wireless doorbell operation
* 📡 433 MHz RF communication
* 🎛️ Push-button input
* 🔊 Automatic buzzer activation
* ⚡ Real-time signal processing
* 🔌 No physical connection required between transmitter and receiver
* 🧠 Arduino-based control
* 📶 Approximate operating range of 10–50 meters in the implemented setup
## Working prototype
![Wireless doorbell system prototype](https://github.com/anuradha081/wireless-doorbell-system/blob/main/Doorbell%20ring%20working%20prototype.mp4)
## 🛠️ Components Used

### Transmitter Unit

* Arduino Uno
* Push Button
* 433 MHz RF Transmitter Module
* 10 kΩ Resistor
* Power Supply/Battery

### Receiver Unit

* Arduino Uno
* 433 MHz RF Receiver Module
* Buzzer
* Power Supply

The project report specifies the transmitter button on **Arduino digital pin D2** and the RF transmitter data line on **D12**.

For the receiver, the RF module's data output is connected to **digital pin D11** according to the RF module documentation included in the report.

## 🔧 Working Principle

### 1. Button Press

When the push button is pressed, the Arduino detects a digital HIGH signal and treats it as the doorbell trigger.

### 2. Transmitter Processing

The transmitter-side Arduino continuously monitors the button. When the button is pressed, the Arduino generates the required control signal.

### 3. RF Transmission

The Arduino sends the signal to the **433 MHz RF transmitter module**.

The RF module transmits the signal wirelessly through the antenna using RF communication. The project documentation describes the modules as operating around **433 MHz** and supporting ASK/OOK modulation.

### 4. RF Reception

The RF receiver captures the transmitted signal and converts it back into an electrical/digital signal.

### 5. Receiver Processing

The received signal is supplied to the second Arduino. The Arduino reads and validates the incoming signal.

### 6. Buzzer Activation

When a valid doorbell signal is received, the receiver Arduino activates the buzzer, producing the doorbell sound.

## 🔌 Pin Configuration

### Transmitter

| Component           | Arduino Pin |
| ------------------- | ----------- |
| Push Button         | D2          |
| RF Transmitter DATA | D12         |
| RF Transmitter VCC  | 5V          |
| RF Transmitter GND  | GND         |

### Receiver

| Component        | Arduino Pin  |
| ---------------- | ------------ |
| RF Receiver DATA | D11          |
| RF Receiver VCC  | 5V           |
| RF Receiver GND  | GND          |
| Buzzer           | Digital GPIO |

The included RF module guide specifically recommends **D12 for transmitter DATA** and **D11 for receiver DATA** when using the corresponding Arduino setup.

## 💻 Software & Libraries

* Arduino IDE
* C/C++ (Arduino)
* RadioHead Library
* `RH_ASK` driver

The project documentation uses the **RadioHead library** for ASK-based RF communication.




## 📊 Result

The wireless doorbell system was successfully implemented using two Arduino Uno boards and 433 MHz RF modules.

The implemented system successfully:

* Detects the push-button press.
* Transmits the signal wirelessly.
* Receives the RF signal.
* Processes the received signal using Arduino.
* Activates the buzzer.
* Demonstrates reliable wireless communication within the tested range.

The project achieved its objective of implementing wireless communication without dedicated encoder and decoder ICs.

## 🚀 Future Scope

### IoT Integration

The system can be upgraded using Wi-Fi modules such as ESP8266 to send doorbell notifications directly to a smartphone.

### 📷 Smart Video Doorbell

A camera module can be integrated to capture visitor images or video and provide live monitoring.

### 🎵 Custom Doorbell Sounds

The buzzer can be replaced with a speaker to support multiple tones, melodies, or customized doorbell sounds.

## 🎓 Learning Outcomes

Through this project, we gained practical understanding of:

* Arduino Uno and embedded programming
* Digital input/output
* RF wireless communication
* 433 MHz RF transmitter and receiver modules
* ASK/OOK communication
* Real-time signal processing
* Hardware interfacing
* Electronic circuit implementation

The project provided practical exposure to RF communication, Arduino programming, and real-time signal processing.

## 👩‍💻 Project Team

**Department:** Electronics and Instrumentation Engineering
**National Institute of Technology Agartala**

* Anuradha Kumari
* Saumya Shreya
* Rahul Goswami
* Are Leela Sahith
* Thota Gowreesh


