# 🐺 Quro – An Offline AI-Powered Companion Robot

## 🤖 About Quro

**Quro** is an experimental, AI-powered companion robot designed to interact with people through voice, audio, visual input and physical actions.

The vision behind Quro is to create an affordable, intelligent and privacy-conscious robotic companion that can communicate with people, provide companionship, assist with learning and eventually support specialised environments such as educational institutions and healthcare facilities.

Unlike conventional cloud-dependent voice assistants, Quro is being developed around local AI processing. Its language model runs directly on an Orange Pi Zero 2W with just 1GB of RAM, using a quantized version of TinyLLaMA.

The project combines embedded systems, artificial intelligence, speech recognition, robotics, computer vision and hardware automation into one compact platform.

Quro is an ongoing independent robotics project. Its architecture and capabilities are continuously evolving.

## 🎯 Our Vision

We believe intelligent technology should not be limited to expensive computers, cloud services or sophisticated robotics laboratories.

Our goal is to explore how affordable hardware and lightweight AI models can be combined to create useful, interactive robots.

Quro is being developed around five major objectives:

- **Companionship:** Building a robot that can interact with people and help reduce feelings of loneliness.
- **Offline AI:** Exploring locally running language models on low-resource hardware.
- **Education:** Developing an interactive learning companion for students.
- **Healthcare assistance:** Exploring potential applications in patient interaction and assistance, subject to appropriate clinical, privacy and safety validation.
- **Smart environments:** Enabling voice-controlled interaction with compatible household devices.

## 🛠️ Hardware Architecture

Quro uses two primary processing and control platforms.

### 1. Orange Pi Zero 2W – Main Processing Unit

The Orange Pi acts as the central brain of Quro.

**Hardware specifications:**
- Board: Orange Pi Zero 2W
- RAM: 1GB
- Operating system: Armbian Linux (Debian Bookworm)
- AI processing: Local CPU-based inference

**Responsibilities:**
- Running the local language model.
- Processing voice input.
- Managing conversational logic.
- Handling audio input and output.
- Processing camera integration.
- Communicating with the ESP32.
- Managing robot behaviour and commands.

### 2. ESP32 – Robotics and Hardware Controller

The ESP32 handles hardware-level operations and communication with physical components.

**Responsibilities:**
- Motor control.
- OLED display management.
- Animated facial expressions.
- Communication with the main processing unit.
- Future sensor and actuator integration.

The separation between AI processing and hardware control allows Quro to perform computationally demanding tasks on the Orange Pi while keeping hardware operations on a dedicated microcontroller.

## 🧠 Software Architecture

Quro combines several lightweight technologies to enable local interaction.

| Technology | Purpose |
|---|---|
| TinyLLaMA | Local language-model inference |
| llama.cpp | Running quantized language models |
| Porcupine | Wake-word detection |
| Vosk | Speech recognition |
| Edge TTS | Text-to-speech generation |
| Python | Main application and integration logic |
| ESP32 firmware | Hardware and motor control |
| Armbian | Operating system |

### AI and Conversation

Quro uses a quantized TinyLLaMA model to generate responses locally on its Orange Pi hardware.

Running a language model on a device with only 1GB of RAM is one of the project's central engineering challenges.

The objective is to make conversational AI accessible on affordable hardware without requiring a powerful GPU or continuous cloud-based language-model access.

### Voice Interaction

The voice interaction pipeline combines:

1. Wake-word detection using Porcupine.
2. Voice recognition using Vosk.
3. Processing the recognised text through the local language model.
4. Generating a response.
5. Converting the response into speech using the configured TTS system.

**Note:** Local language-model inference and speech recognition are separate from the speech-generation service. The current Edge TTS implementation requires internet connectivity.

### Camera Integration

Quro includes camera hardware for exploring visual perception and environmental interaction.

The camera integration is part of the ongoing development of more intelligent and context-aware robotic behaviour.

### Physical Interaction

The Orange Pi communicates with the ESP32 to coordinate software commands with physical robot operations.

The ESP32 manages the motor-control and display-related functionality, allowing Quro to combine conversational interaction with physical responses.

## ⚙️ Operating Modes

Quro is being developed with multiple interaction and control modes.

### 1. Autonomous Mode

The objective is to allow Quro to operate with minimal human intervention.

Planned capabilities include:
- Responding to voice interactions.
- Executing permitted robot behaviours.
- Interacting with connected hardware.
- Developing more intelligent autonomous decision-making.

### 2. Wi-Fi Control Mode

Quro is also designed to support remote control through Wi-Fi communication.

This allows interaction with the robot without directly operating its hardware.

### 3. Smart-Home Control

An important part of Quro's roadmap is household automation.

The intended capabilities include controlling compatible:

- Lights.
- Fans.
- Television systems.
- Air conditioners.
- Other supported household appliances.

The implementation will use suitable hardware interfaces, such as infrared transmitters and relay controllers.

## 🔬 Research and Future Development

Quro is not intended to remain a basic voice assistant.

We want to explore several advanced areas of robotics and artificial intelligence.

### Reinforcement Learning

We plan to investigate reinforcement learning techniques to help Quro improve its behaviour through interaction and feedback.

Potential applications include:
- More intelligent action selection.
- Adaptive behaviour.
- Autonomous decision-making.
- Learning from interaction with its environment.

### Human-Robot Interaction

Future development will focus on making conversations more natural and improving how Quro understands and responds to people.

### Education

We want to explore Quro as an interactive educational companion that can explain concepts, answer questions and encourage students to learn through interaction.

### Healthcare Applications

We are interested in researching how companion robots could support patient interaction, provide non-clinical assistance and offer companionship in healthcare environments.

These are exploratory goals and would require appropriate testing, professional oversight and safety validation before real-world deployment.

## 🗺️ Development Roadmap

| Area | Development status |
|---|---|
| Orange Pi integration | Implemented |
| Local TinyLLaMA integration | Working prototype |
| Wake-word detection | Implemented |
| Speech recognition | Implemented |
| Voice response | Implemented |
| ESP32 communication | Implemented |
| OLED animations | Implemented |
| Motor control | Implemented |
| Camera integration | Experimental |
| Wi-Fi remote control | Under development |
| Smart-home automation | Planned |
| Reinforcement learning | Research planned |
| Educational applications | Future vision |
| Healthcare applications | Future research |

## 🔋 Hardware and Power

Quro uses a compact embedded computing architecture with an Orange Pi Zero 2W and an ESP32.

The power arrangement and peripheral connections are part of the hardware development and will be documented further as the design evolves.

Detailed wiring diagrams, power requirements and component specifications will be added as the hardware documentation becomes available.

## 🎥 Project Demonstrations

The repository includes demonstration videos showing Quro's physical prototype and development progress.

These videos document the project as it evolves from an experimental robotics platform towards a more capable AI companion.

See the demonstration videos available in this repository.

## 🌱 Why This Project Matters

One of the biggest challenges in accessible AI robotics is the hardware cost and computational requirements associated with running intelligent systems.

Quro explores a different approach:

**Can we build a useful AI-powered companion robot using affordable hardware, lightweight language models and local processing?**

By experimenting with a 1GB Orange Pi, quantized language models and a separate microcontroller for hardware operations, we aim to understand the practical possibilities and limitations of low-cost edge AI.

We hope the knowledge gained through this project can eventually help other developers, students and robotics enthusiasts experiment with similar systems.

## 🤝 Contributions and Collaboration

Quro is currently an independently developed project, and we are interested in learning from the wider robotics and open-source community.

We welcome interest from developers, students, researchers and robotics enthusiasts working in areas such as:

- Edge AI and lightweight language models.
- Embedded Linux.
- ESP32 and microcontroller development.
- Speech recognition and synthesis.
- Computer vision.
- Autonomous robotics.
- Human-robot interaction.

As the project becomes more thoroughly documented and its source code is prepared for public release, contribution guidelines will be added.

## ⚠️ Project Status

Quro is an experimental development project.

Some features are functional, some are under development and others are part of our long-term research vision.

The project is not a certified medical device, and its healthcare-related applications are exploratory.

## 👨‍💻 Project Developer

**Chitransh Jadhav**

Independent Robotics and AI Developer | India

Building Quro to explore the possibilities of affordable AI, offline intelligence and human-robot interaction.

GitHub: https://github.com/chitranshc

Project Repository: https://github.com/chitranshc/quro-robot

---

<p align="center">
  <strong>QURO – More Than a Robot. A Step Towards Intelligent Companionship.</strong>
</p>

<p align="center">
  <em>Built with curiosity, experimentation and a vision for accessible AI.</em>
</p>
