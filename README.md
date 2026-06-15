# Azure GPT Powered PLC Controller Using Hand Gesture Recognition

## Overview

This project combines Computer Vision, Industrial Automation, and Generative AI to control a Programmable Logic Controller (PLC) using hand gestures.

The system uses a webcam to detect hand gestures through MediaPipe and OpenCV. The detected gesture is sent to Azure OpenAI GPT-4o, which interprets the gesture and generates a PLC control command. The command is then transmitted to OpenPLC using the Modbus TCP protocol.

This project demonstrates the integration of Artificial Intelligence with Industrial Automation systems.

---

## Features

* Real-time hand gesture detection using MediaPipe
* Computer vision powered by OpenCV
* AI-based gesture interpretation using Azure OpenAI GPT-4o
* Industrial communication using Modbus TCP
* PLC control through OpenPLC
* Live command display on screen
* Real-time automation response
* Expandable architecture for multiple industrial devices

---

## Technologies Used

### Programming Language

* Python

### Computer Vision

* OpenCV
* MediaPipe

### Artificial Intelligence

* Azure OpenAI GPT-4o

### Industrial Automation

* OpenPLC
* Modbus TCP

### Additional Libraries

* Requests
* Python Dotenv
* PyModbus

---

## System Architecture

1. Webcam captures hand gestures.
2. MediaPipe detects hand landmarks.
3. Finger positions are converted into a binary gesture list.
4. Gesture data is sent to Azure OpenAI GPT-4o.
5. GPT interprets the gesture and generates a PLC command.
6. The command is transmitted to OpenPLC through Modbus TCP.
7. PLC coils are activated or deactivated based on the generated command.

---

## Gesture Mapping

| Gesture Pattern   | Command   |
| ----------------- | --------- |
| [0,1,0,0,0]       | PLC_1_ON  |
| [0,1,1,0,0]       | PLC_2_ON  |
| [0,0,0,0,0]       | ALL_OFF   |
| Any Other Gesture | NO_ACTION |

---

## Project Structure

```text
project/
│
├── main.py
├── .env
├── requirements.txt
├── README.md
│
└── assets/
    └── screenshots
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/your-username/plc-controller-gpt.git
cd plc-controller-gpt
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file:

```env
OPENAI_API_KEY=YOUR_AZURE_OPENAI_KEY
AZURE_ENDPOINT=YOUR_AZURE_OPENAI_ENDPOINT
```

### Start OpenPLC

Ensure OpenPLC Runtime is running and Modbus TCP Server is enabled on:

```text
IP Address : 127.0.0.1
Port       : 502
```

### Run the Application

```bash
python main.py
```

---

## Output

The application displays:

* Detected hand gesture
* AI-generated PLC command
* Live webcam feed
* PLC activation status

Example:

```text
Gesture: [0,1,0,0,0]
Command: PLC_1_ON
```

---

## Applications

* Smart Factory Automation
* Human Machine Interaction (HMI)
* Gesture Controlled Industrial Systems
* AI Assisted PLC Programming
* Industry 4.0 Demonstrations
* Industrial Research and Education

---

## Future Enhancements

* Support for multiple PLC devices
* Voice command integration
* Dashboard for monitoring PLC status
* Azure IoT Hub integration
* Predictive maintenance using AI
* Industrial digital twin implementation

---

## Author

Kavin Kumar S

B.Tech Artificial Intelligence and Data Science

Passionate about AI, Industrial Automation, IoT, Computer Vision, and Generative AI.

---

## License

This project is intended for educational and research purposes.
