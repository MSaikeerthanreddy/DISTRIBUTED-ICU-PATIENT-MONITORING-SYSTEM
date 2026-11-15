# DISTRIBUTED-ICU-PATIENT-MONITORING

An LPC2129-based distributed patient monitoring system that measures temperature, SpO₂ and light intensity, and transfers sensor data between two nodes using CAN communication.

## Project Overview
This project is an embedded systems-based patient monitoring solution using two LPC2129 ARM7 microcontroller nodes. It monitors temperature, oxygen saturation (SpO₂), and light intensity, and transfers the collected sensor data between the nodes using CAN communication.

## Key Features
- Temperature monitoring using LM35.
- SpO₂ estimation using MAX30102.
- Light intensity monitoring using LDR.
- ADC-based analog sensor data acquisition.
- I²C communication with MAX30102.
- CAN-based communication between transmitter and receiver.
- UART-based serial data monitoring.

## Hardware Components
- LPC2129 ARM7 Microcontrollers (2)
- MAX30102 Pulse Oximeter Sensor
- LM35 Temperature Sensor
- LDR Sensor
- CAN communication interface

## Software and Tools
- Embedded C
- Keil µVision IDE
- ADC
- I²C
- UART
- CAN Protocol

## System Architecture

### Transmitter Node
- Reads temperature and LDR sensor values through ADC.
- Reads RED and IR data from MAX30102 through I²C.
- Estimates SpO₂ using sensor readings.
- Packs sensor values into a CAN data frame.
- Transmits data through CAN1.

### Receiver Node
- Receives sensor data through CAN1.
- Extracts individual sensor values using bitwise operations.
- Converts raw ADC values into meaningful readings.
- Displays the monitoring data through UART.

## Communication Protocols
| Protocol | Purpose |

| ADC      | Analog sensor data acquisition |
| I²C      | MAX30102 interfacing |
| UART     | Serial data display |
| CAN      | Communication between nodes |

## Learning Outcomes
- LPC2129 peripheral interfacing.
- Embedded C programming.
- Sensor interfacing and data acquisition.
- CAN communication between microcontrollers.
- Data packing and unpacking using bitwise operations.

## Disclaimer
This project is developed for educational purposes. The SpO₂ calculation is a simplified estimation and is not intended for medical diagnosis or clinical use.
