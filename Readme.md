
<img src="https://github.com/user-attachments/assets/ddb1306b-9592-427d-9dc0-a8d04ecd842b" width="100" height="100"/>

# Voice Assistant with ESSP32 and wit.ai

This project aims to design and build a voice-controlled assistant using the ESP32 microcontroller, I2S microphone. The system listens for a specific wake-up word and, once detected, records the user's voice command, sends it to a local Django server, and then forwards it to Wit.ai for processing. The processed command is returned to the ESP32 for execution.there are three main components:
- Wake word detection
- Audio capture and Intent Recognition
- Intent Execution


## Tools
- ESP32: Microcontroller for voice command processing and communication.
- I2S Microphone: Captures audio for wake-up word detection and command recognition.
- LED and resistor: for intent execution
- python3+: to run the server
- Django: Local server to interface between ESP32 and Wit.ai.
- Wit.ai: Online service for voice command recognition.
- Platform.io: a development environment for microcontrollers like the Arduino

## Implementation Details
### System Overview
The system consists of three main components:

Wake-Up Word Detection: The ESP32 continuously monitors audio input to detect a predefined wake-up word.
Command Recording & Processing: Upon detecting the wake-up word, the system records the user's voice command and sends it to the Django server.
Command Execution: The processed command from Wit.ai is sent back to the ESP32 for execution.

### ESP32 Implementation
The ESP32 handles wake-up word detection and interfaces with the server via Wi-Fi. The I2S protocol is used for high-quality audio data transmission between the microphone and the ESP32. you can find the code implementation in ESP32 folder.

### Local Django Server
The Django server acts as a bridge between the ESP32 and Wit.ai, managing the voice command processing requests and returning the results to the ESP32. you can find the code implementation in Server foulder.

### Wit.ai Integration
Wit.ai processes the audio file, recognizes the command, and returns the result to the local server.

## How to Run
### Prerequisites
- ESP32 development environment set up with PlatformIO or Arduino IDE.
- Django server installed and running locally.
- Wit.ai account and API token configured.

#### Build Project
you can use vscode build and upload project to esp32:
![20240903_004334](https://github.com/user-attachments/assets/531cc988-5456-4979-8656-851b30bd35b7)
serial monitor the output:
![20240903_004402](https://github.com/user-attachments/assets/79fa5d42-a69a-44cb-9cfc-d62085bd94bc)

#### Run server
Navigate to the server directory and run:
```bash
  python manage.py runserver IPv4address:port
```
you can find your IPv4 address by following command
```bash
  ipconfig
```
# Configuration
Ensure the ESP32 firmware is configured with the correct Wi-Fi credentials and server IP address.


## Results
The system successfully detects wake-up words, processes voice commands via Wit.ai, and executes the commands on the ESP32.
![IMG_20240903_011505_242](https://github.com/user-attachments/assets/49147938-3027-42c8-8105-403b21b7fe67)
![IMG_20240903_004034_837](https://github.com/user-attachments/assets/954f3aec-e405-4ac4-8fd0-63defa5a812c)


## Related Links
Some links related to your project come here.
- [similar project](https://github.com/atomic14/diy-alexa?tab=readme-ov-file)
- [wit.ai](https://wit.ai/)
- [Django Doc](https://docs.djangoproject.com/en/5.0/)
- [ESP32 Pinout](https://randomnerdtutorials.com/esp32-pinout-reference-gpios/)


## Authors
Authors and their github link come here.
- [@nikisepasian](https://github.com/NikiSP)
- [@erfansalima](https://github.com/erfansalima)
- [@asemanehnafe](https://github.com/asemanehnafe)


