
![Logo](https://via.placeholder.com/600x150?text=Your+Logo+Here+600x150)


# Voice Assistant with ESSP32 and wit.ai

This project aims to design and build a voice-controlled assistant using the ESP32 microcontroller, I2S microphone. The system listens for a specific wake-up word and, once detected, records the user's voice command, sends it to a local Django server, and then forwards it to Wit.ai for processing. The processed command is returned to the ESP32 for execution.there are three main components:
- Wake word detection
- Audio capture and Intent Recognition
- Intent Execution


## Tools
- ESP32: Microcontroller for voice command processing and communication.
- I2S Microphone: Captures audio for wake-up word detection and command recognition.
- LED and resistor: for intent execution
- Django: Local server to interface between ESP32 and Wit.ai.
- Wit.ai: Online service for voice command recognition.
- Platform.io: a development environment for microcontrollers like the Arduino

## Implementation Details

In this section, you will explain how you completed your project. It is recommended to use pictures to demonstrate your system model and implementation.


Feel free to use sub-topics for your projects. If your project consists of multiple parts (e.g. server, client, and embedded device), create a separate topic for each one.

## How to Run

In this part, you should provide instructions on how to run your project. Also if your project requires any prerequisites, mention them. 

#### Examples:
#### Build Project
Your text comes here
```bash
  build --platform=OvmfPkg/OvmfPkgX64.dsc --arch=X64 --buildtarget=RELEASE --tagname=GCC5
```

#### Run server
Your text comes here
```bash
  pyhton server.py -p 8080
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `-p` | `int` | **Required**. Server port |



## Results
In this section, you should present your results and provide an explanation for them.

Using image is required.

## Related Links
Some links related to your project come here.
- [similar project](https://github.com/atomic14/diy-alexa?tab=readme-ov-file)
- [wit.ai](https://wit.ai/)
- [Django Doc](https://docs.djangoproject.com/en/5.0/)
- [ESP32 Pinout](https://randomnerdtutorials.com/esp32-pinout-reference-gpios/)


## Authors
Authors and their github link come here.
- [@asemnaehnafe](https://github.com/asemanehnafe)
- [@nikisepasian](https://github.com/Sharif-University-ESRLab)
- [@erfansalime](https://github.com/Sharif-University-ESRLab)


