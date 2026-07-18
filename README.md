# RFID-OTP-Dual-Authentication-System
A dual-authentication access control system built on LPC2148 ARM7 microcontroller using RFID and GSM-based OTP verification for enhanced security.
# RFID Secure Password-Based Dual Authentication

## Overview
This project implements a secure dual authentication system using an LPC2148 microcontroller. Access is granted only after successful RFID card verification followed by password authentication.

## Features
- RFID-based authentication
- Password verification using keypad
- 16x2 LCD interface
- Buzzer for invalid access
- Relay-controlled door lock
- Embedded C programming
- LPC2148 (ARM7)

## Hardware
- LPC2148
- RFID Reader
- 4x4 Keypad
- 16x2 LCD
- Relay
- Buzzer
- Power Supply

## Software
- Embedded C
- Keil uVision
- Flash Magic

## How it Works
1. Scan RFID card.
2. If valid, prompt for password.
3. If password matches, unlock the door.
4. Otherwise, deny access and sound the buzzer.
