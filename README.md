# Gait Sonification Shoe Insole Training Device for PD
## BME Capstone Project
## Fall 2025
### Hannah Carroll, Sabrina Goslin, Thomas Lynch, Kyle Yost, Caitlyn Robinson

## Project Background
### Motivation
- Why we/Sam chose to do this project
- Small section of PD stats for impact
### Design Process
- Ideation process
- Concept map
### Prototypes
- Images of prototype iterations
### Final Design
- Description & Images 

## Installation and Usage

## Main Features 
- **Live Serial Input**: Accepts JSON-formatted FSR data via PySerial from microcontroller
- **Baseline Measurements**:
  - Collects and calculates average force for all sensors over a period of 10s to determine baseline for patients of different weights
  - Calculates average steps per minute after a period of 30 seconds patient walking (calculated from time between heelstrikes (sensor 0 \geq baseline))
- **Training Mode**:
  - Plays metronome based on patient average step per minute for x seconds (customizable for patients with different onsets)
  - Metronome turns dims to 0 sound
  - Metronome only plays agian if toe sensors fail to acheive baseline 0.25 seconds after heelstrike (indicating shuffle/stutter step)
- **CSV Logging**: All gait data written into `gait_log_cadence.csv` for physician analysis
  
