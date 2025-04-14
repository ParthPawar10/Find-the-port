
# Find the port
A simple Arduino hardware/software serial port tester using Python and pySerial.

## Overview

This tool is designed to test the reliability of serial communication (both hardware and software serial) between your PC and an Arduino board.

It continuously sends bytes from 0 to 255 and checks if the received byte matches the sent byte.

## Requirements

- Python 2.x (Python 3 not supported in this script)
- pySerial

Install pySerial using pip if not already installed:

```bash
pip install pyserial
```

## Usage

```bash
python2 serial_tester.py <port>
```

For example:

```bash
python2 serial_tester.py /dev/ttyUSB0
```

Replace `/dev/ttyUSB0` with the appropriate serial port for your system (e.g., `COM3` on Windows).

## Example Output

Here is the test result of software serial running on a Leonardo board.  
Arduino IDE version: 1.8.5  
Baudrate: 115200  


Left column: test number  
Right column: byte sent and received

## How it Works

1. The script opens the specified serial port at 115200 baud.
2. Sends a byte from 0 to 255.
3. Waits for a response.
4. Compares the received byte with the sent byte.
5. Logs the result and continues until a mismatch is found.
