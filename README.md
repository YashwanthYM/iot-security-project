# IoT Security Project: 6LoWPAN Attack Detection & Mitigation

An intelligent security framework for detecting and mitigating routing attacks in constrained IoT networks using Software-Defined Networking (SDN), TinyML, and Reinforcement Learning (RL).

## Project Overview

This project proposes a multi-layer security architecture for 6LoWPAN-based IoT networks. The framework continuously monitors network traffic, detects malicious behavior using lightweight machine learning models, and automatically applies mitigation strategies through a reinforcement learning agent.

### Key Features

* Centralized SDN-based network monitoring
* TinyML-powered anomaly detection for resource-constrained devices
* Reinforcement Learning-based autonomous mitigation
* Detection of multiple routing attacks:

  * Selective Forwarding Attack
  * Sinkhole Attack
  * Spoofing Attack
  * Distributed Denial-of-Service (DDoS) Attack
* End-to-end integration of simulation, detection, and mitigation components

## Technology Stack

| Category               | Technologies                    |
| ---------------------- | ------------------------------- |
| Network Simulation     | Contiki-NG, Cooja               |
| Programming Languages  | C, Python                       |
| Machine Learning       | TensorFlow, Keras, Scikit-learn |
| TinyML                 | TensorFlow Lite                 |
| Reinforcement Learning | Stable Baselines3               |
| Data Processing        | Pandas, NumPy                   |

## Project Structure

```text
iot-security-project/
├── phase1_setup/         # Environment setup and dependencies
├── phase2_simulation/    # Cooja simulations and attack implementations
├── phase3_tinyml/        # TinyML anomaly detection models
├── phase4_rl/            # Reinforcement Learning agent training
├── integration/          # End-to-end system integration
├── docs/                 # Documentation and analysis
└── README.md
```

## Project Workflow

```text
6LoWPAN Network
       ↓
Traffic Monitoring (SDN Controller)
       ↓
Feature Extraction
       ↓
TinyML Anomaly Detection
       ↓
Attack Classification
       ↓
RL-Based Mitigation
       ↓
Network Recovery
```

## Supported Attacks

| Attack               | Description                                              |
| -------------------- | -------------------------------------------------------- |
| Selective Forwarding | Malicious nodes selectively drop packets                 |
| Sinkhole             | A malicious node attracts surrounding traffic            |
| Spoofing             | Fake identities are used to impersonate legitimate nodes |
| DDoS                 | Multiple nodes flood the network with traffic            |

## Quick Start

### Phase 1: Environment Setup

```bash
cd phase1_setup
```

### Phase 2: Network Simulation

```bash
cd phase2_simulation
# Refer to the README inside this directory for Cooja setup instructions.
```

### Phase 3: TinyML Model Training

```bash
cd ../phase3_tinyml
jupyter notebook
```

### Phase 4: Reinforcement Learning Training

```bash
cd ../phase4_rl
python src/dqn_training.py
```

## Project Status

* [x] Environment setup and verification
* [ ] Network simulation and attack implementation
* [ ] TinyML anomaly detection model
* [ ] Reinforcement Learning mitigation framework
* [ ] End-to-end integration and evaluation

## Expected Outcomes

* Accurate detection of routing attacks in 6LoWPAN networks.
* Lightweight anomaly detection suitable for constrained IoT devices.
* Autonomous attack mitigation using Reinforcement Learning.
* Improved network resilience and packet delivery performance.

## Future Enhancements

* Deploy the framework on physical sensor nodes.
* Support additional attack types.
* Explore federated learning for distributed anomaly detection.
* Implement real-time visualization dashboards.

## Author

**Yashwanth Maloth**
B.Tech Information Technology, VNR VJIET

---

Last Updated: 2026-07-01

