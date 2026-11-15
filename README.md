# Sensitive Theremin MIDI Controller

### Tocá música sin tocar nada.
https://sensitive-theremin-controller-inter.vercel.app/

An interactive web-based musical instrument developed by **Sensitive Lab**, combining Arduino electronics, ultrasonic sensing and MIDI technology.

The project transforms hand movements into musical notes using an HC-SR04 ultrasonic sensor connected to an Arduino Nano. A custom web interface receives the data, generates sound and sends MIDI messages to external virtual instruments (VST) and DAWs.

## Features


https://github.com/user-attachments/assets/a175158e-6275-43f4-ad0b-30cae132141c



- **Touchless control:** Generate musical notes through hand movements.
- **Arduino USB connection:** Direct serial communication using Web Serial API.
- **Pentatonic scale:** 15 musical notes with real-time visual feedback.
- **Web MIDI:** MIDI input and output support.
- **VST integration:** Control external virtual instruments and DAWs.
- **Built-in synthesizer:** Sine, triangle, sawtooth and square waveforms.
- **Sound controls:** Volume, glide, brightness and echo.
- **Oscilloscope:** Real-time waveform visualization.
- **Interactive interface:** Play notes using the screen, mouse or keyboard.

## Hardware

- Arduino Nano
- HC-SR04 ultrasonic distance sensor
- USB connection  <img width="1122" height="1402" alt="c43addeb-077c-4a0c-83c4-69647859dbbd" src="https://github.com/user-attachments/assets/584dbd1d-52fb-4886-b8b1-528fd277b86a" />



## Technologies

- HTML5
- CSS3
- JavaScript
- Web Audio API
- Web MIDI API
- Web Serial API
- Arduino

## Getting started

1. Clone or download this repository.
2. Open `index.html` using Google Chrome or Microsoft Edge on a desktop computer.
3. Connect your Arduino Nano via USB.
4. Close the Arduino IDE Serial Monitor and any other application using the serial port.
5. Click **Connect Arduino (USB)**.
6. Move your hand in front of the ultrasonic sensor to control the notes.

## Using external VST instruments

The interface can send MIDI notes to external music production software.

1. Install [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html) on Windows.
2. Create a virtual MIDI port.
3. Select the port in the interface.
4. Enable MIDI input in your DAW (Reaper, Ableton Live, FL Studio, Cubase, etc.).
5. Activate VST Mode and start playing.

The browser generates its own sound through Web Audio API, while MIDI output allows external instruments to receive the notes.

## Communication

The Arduino communicates with the web interface through USB serial at 115200 baud.

The interface expects MIDI messages encoded as three-byte serial messages (Note On / Note Off).

**Note:** The Arduino firmware must implement the corresponding ultrasonic sensing and MIDI serial transmission. The web interface is provided in `index.html`.

## About Sensitive Lab

**Sensitive Lab** is an independent experimental space exploring electronic musical instruments, digital luthiery and accessible creative technologies.

Our philosophy:

- Minimal Innovation
- Digital Luthiery
- Technological Sovereignty

**Building new ways to interact with sound.**


