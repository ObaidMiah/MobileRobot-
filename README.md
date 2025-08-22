# Voice-Controlled Mobile Robot

A mobile robot that can recognize and execute basic **voice commands** using speech recognition and wireless communication. This project demonstrates the fundamentals behind self-driving cars and voice-controlled automation.

---

## 🚀 Features
- Speech recognition of four commands: **Go, Left, Right, Stop**  
- Wireless communication between base station and robot using **nRF24L01** transceivers  
- Integration of **DSP (FFT + MFCC)** for feature extraction and neural network classification  
- Remote control via Arduino + Texas Instruments **LCDK (L138/C6748)**  

---

## 🛠 System Architecture
The project is split into two stations:

### Base Station
- Microphone  
- LCDK for speech recognition (Code Composer Studio + DSP functions)  
- Arduino Nano  
- nRF24L01 transceiver  

### Receiver Station
- Arduino Nano  
- nRF24L01 transceiver  
- Mobile robot chassis with DC motors, resistors, transistors, and batteries  

---

## ⚙️ How It Works
1. User speaks a command into the microphone.  
2. LCDK processes speech → extracts MFCC features → classifies command.  
3. Command is sent to Arduino via GPIO → transmitted wirelessly via nRF24L01.  
4. Receiver Arduino drives the robot motors according to the command.  

---

## 🔩 Hardware Used
- Texas Instruments LCDK (L138/C6748)  
- 2 × Arduino Nano  
- nRF24L01 radio transceivers  
- DC motors, TIP120 transistors, 1kΩ resistors  
- 9V and 6V batteries  
- Microphone  

---

## 💻 Software & Tools
- **Code Composer Studio** (C for DSP & speech recognition)  
- **MATLAB** (neural network training for speech commands)  
- **Arduino IDE** (motor control + wireless communication)  

---

## 📊 Results
- Successfully implemented voice-controlled movement of a robot.  
- Recognized and executed commands with moderate accuracy.  
- Wireless functionality worked but was limited by hardware quality.  
- Future improvements:  
  - Expand speech dataset  
  - Improve radio modules  
  - Enable continuous listening mode  

---

## 🎥 Demo
[![Demo Picture](assets/car_setup.png)]
👉 [YouTube Demo Link] [(Add your video link here)](https://www.youtube.com/watch?v=Bbf-TNEz7DQ)

---

## 👥 Team
- **Obaid Miah** – Speech Recognition & Hardware Integration  
- **Edward Kang** – DSP & System Architecture  
