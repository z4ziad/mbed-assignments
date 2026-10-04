# Setup Guide

Complete these steps once, before Assignment 1.

## 1. Hardware

- Arduino Nicla Vision
- Micro-USB adapter plus a USB-C to USB C or USB-C to USB-A **data** cable (charge-only cables will not work)

## 2. Edge Impulse account

1. Create a free account at <https://edgeimpulse.com>.
2. _Naming convention for projects, e.g. `mbed-a1-<Andrew-id>`._

## 3. Software
#### For data collection:   
1. First, Please follow [the instructions by Edge Impulse](https://docs.edgeimpulse.com/hardware/boards/arduino-nicla-vision) to install
   - [ ] Edge Impulse CLI.
   - [ ] Arduino CLI.   
  

2. [Follow the instructions on this Youtube video](https://youtu.be/sWVJv-UDo-c) to flash the board with the data collection firmware and start collecting data for your project.  

**Note:** For the assignments, we do not need the instructions given in the [Data Ingestion](https://docs.edgeimpulse.com/hardware/boards/arduino-nicla-vision#data-ingestion) section by Edge Impulse. The firmware you download in step-2 above is sufficient for our purposes.  
    
#### For application deployment: 
- [ ] Arduino IDE (preferred) or OpenMV IDE


## Troubleshooting

| Symptom | Fix |
|---------|-----|
| Board not detected | Try a different cable; double-press reset to enter bootloader mode |
| Other issues | Please post on Piazza |
