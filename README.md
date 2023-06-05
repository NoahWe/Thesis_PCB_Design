# Experiment
This repository contains the PCB designs for a pressure sensor array using BMP581 sensors. The PCBs were designed to be used in the experiment which I will run as part of my MSc thesis. The experiment aims to determine the pressure distribution over a wing, located behind tilting rotors. The sensor array is specifically aimed at the vehicle designed by Alessandro Mancinelli (https://doi.org/10.1109/ICUAS54217.2022.9836063), and is supposed to resolve some of the problems experienced using tilt-rotors to roll.

## How to get started
1. Clone the repository
2. Open one of the KiCad project files (.kicad_pro).

The mainboard is located in /Experiment_PCB/MainBoard/. The sensor strips connected to the top half of the wing are located in Experiment_PCB/SensorStrip_Top/, and finally the sensor strip connected to the bottom half of the wing are located in /Experiment_PCB/SensorStrip_Bottom/.

## Sensors
The sensor which will be used for the experiment is the BMP581: https://www.bosch-sensortec.com/products/environmental-sensors/pressure-sensors/bmp581/

The setup will have 72 pressure sensors which will be driven by a single Teensy4.1 board (https://www.pjrc.com/store/teensy41.html). The Teensy4.1 features 2 SPI buses allowing me to use a single chip select line to drive two sensors. The SPI buses will run at approximately 5 MHz.
