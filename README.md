# Arduino-to-Excel
# Arduino to Excel Data Logging

## Overview

This project enables real-time data logging from an Arduino to Microsoft Excel using Python. By capturing sensor data through the Arduino and transmitting it via serial communication, the data is recorded into a CSV (Comma Separated Values) file, which can be easily opened and analyzed in Excel.

## Features

- **Real-Time Data Logging**: Capture and log data from multiple sensors connected to the Arduino in real-time.
- **CSV File Generation**: Store logged data in a CSV format, compatible with Excel and other data analysis tools.
- **Cross-Platform Compatibility**: The system works on both Windows and Linux operating systems.

## Requirements

- **Hardware**:
  - Arduino UNO or compatible board
  - Sensors (e.g., temperature, humidity, CO₂)
  - USB cable for Arduino-PC connection

- **Software**:
  - Python 3.6 or newer
  - Required Python libraries:
    - `pyserial`
    - `pandas`
    - `openpyxl`

## Installation & Setup

1. **Install Python**:
   - Download and install Python from the [official website](https://www.python.org/).

2. **Install Python Libraries**:
   - Open a terminal or command prompt and run:
     ```sh
     pip install requirements.txt
     ```

3. **Arduino Setup**:
   - Connect your sensors to the Arduino.
   - Upload the appropriate Arduino sketch to read sensor data and send it via serial communication.

4. **Run the Python Script**:
   - Execute the Python script to start logging data:
     ```sh
     python fff.py
     ```

## How It Works

1. **Arduino**:
   - Reads data from connected sensors.
   - Sends the data over serial communication to the connected PC.

2. **Python Script**:
   - Establishes a serial connection with the Arduino using `pyserial`.
   - Reads incoming data and appends a timestamp.
   - Logs the data into a CSV file using `pandas`.

3. **Excel**:
   - The generated CSV file can be opened in Excel for data analysis and visualization.

## Data Format

The logged data is stored in a CSV file with the following columns:

- `Timestamp`: Date and time of the data entry
- `Sensor1`: Data from the first sensor
- `Sensor2`: Data from the second sensor
- ...

Example:

```csv
Timestamp, Sensor1, Sensor2, Sensor3
2025-03-12 12:00:00, 23.5, 45.2, 400
2025-03-12 12:00:01, 23.6, 45.3, 405
...
