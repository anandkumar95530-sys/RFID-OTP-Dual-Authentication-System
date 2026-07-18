# SecurePass Duo: RFID and OTP-Based Dual Authentication System

## Overview

SecurePass Duo is an embedded security system developed using the LPC2148 (ARM7) microcontroller to provide a robust two-factor authentication mechanism for secure access control. The system combines RFID card verification with One-Time Password (OTP) authentication to improve security over conventional single-factor authentication systems.

When a valid RFID card is detected, the system generates a random OTP and sends it to the registered user's mobile phone through the M660A GSM module. The generated OTP remains valid only for a predefined time interval, which is monitored using the LPC2148's on-chip Real-Time Clock (RTC). The user must enter the correct OTP using a 4×4 matrix keypad before the timer expires. If both authentication stages are successful, the system grants access by activating the security device. Otherwise, access is denied.

---

## Features

- Dual-factor authentication using RFID and OTP
- RFID card verification through UART communication
- OTP generation and SMS transmission using GSM module
- OTP timeout monitoring using on-chip RTC
- 4×4 Matrix Keypad for OTP entry
- 16×2 LCD for user interaction
- Security device control (Door Lock / LED / DC Motor)
- UART interrupt-based communication
- RTC editing through External Interrupt

---

## Hardware Components

- LPC2148 ARM7 Microcontroller
- RFID Reader
- RFID Cards
- Neoway M660A GSM Module
- 16×2 LCD Display
- 4×4 Matrix Keypad
- RTC (On-chip LPC2148)
- External Interrupt Switch (RTC Edit Mode)
- LED / Door Lock / DC Motor (through L293D Driver)
- MAX232 (for serial communication during testing)
- Power Supply

---

## Software Requirements

- Embedded C
- Keil µVision
- Flash Magic

---

## Working Principle

1. The system initializes all peripherals.
2. It waits for an RFID card.
3. If the RFID card is valid, an OTP is generated.
4. The OTP is sent to the registered mobile number using the GSM module.
5. The OTP generation time is stored using the LPC2148 RTC.
6. The user enters the OTP through the keypad.
7. If the entered OTP matches within the allowed time, access is granted.
8. Otherwise, authentication fails and the system returns to the initial state.

---

## Communication Interfaces

| Peripheral | Interface |
|------------|-----------|
| RFID Reader | UART1 (Interrupt) |
| GSM Module | UART0 |
| LCD | GPIO |
| Keypad | GPIO |
| RTC | On-chip RTC |
| Edit Switch | External Interrupt |

---

## Project Structure

```
SecurePass-Duo/
│
├── Source/
│   ├── main.c
│   ├── lcd.c
│   ├── uart0.c
│   ├── uart1.c
│   ├── keypad.c
│   ├── rtc.c
│   ├── gsm.c
│   ├── rfid.c
│   └── interrupt.c
│
├── Header/
│   ├── lcd.h
│   ├── uart.h
│   ├── keypad.h
│   ├── rtc.h
│   ├── gsm.h
│   ├── rfid.h
│   └── interrupt.h
│
├── Documents/
│   ├── Project_Report.pdf
│   ├── Block_Diagram.png
│   └── Circuit_Diagram.pdf
│
├── Images/
│   ├── Hardware_Setup.jpg
│   └── Working_Demo.jpg
│
└── README.md
```

---

## Applications

- Smart Door Lock Systems
- Office Access Control
- Laboratory Security
- Banking Security Systems
- Industrial Access Management
- Educational Institution Security

---

## Future Enhancements

- Fingerprint Authentication
- Face Recognition
- Mobile Application Integration
- Cloud-Based Authentication Logs
- Wi-Fi / IoT Connectivity
- Database Integration for User Management

---

## Developed Using

- Embedded C
- ARM7 LPC2148
- UART Communication
- Interrupt Programming
- RTC
- GSM AT Commands
- RFID Technology

---

## Author

**Anand Kumar**

B.Tech – Electrical and Electronics Engineering

Embedded Systems Enthusiast
