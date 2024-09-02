# Code

## Model
The wake word detection model is implemented using a neural network. This model is responsible for detecting the specific wake word ("Marvin") from audio input, triggering the ESP32 to start processing further commands.

## Server
The server is implemented using Django in Python. It handles:

- Receiving raw audio streams from the ESP32.
- Converting and saving the audio as .wav files.
- Sending the audio data to Wit.ai for speech recognition.
- Processing the results from Wit.ai to determine the appropriate device and action (e.g., turning lights on/off) and sending this information back to the ESP32.


## ESP32
The ESP32 is programmed using C++ in the Arduino IDE. It utilizes the wake word detection model to:

- Continuously monitor for the wake word.
- Capture and stream audio data to the server once the wake word is detected.
- Execute commands (e.g., turning lights on/off) based on the instructions received from the server after processing the audio data.
