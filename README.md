# AI-Driven IoT Security: Detecting and Preventing Routing Attacks in SDN-Enabled 6LoWPAN Networks

An intelligent security framework that combines Software-Defined Networking (SDN), TinyML, and Reinforcement Learning (RL) to detect and mitigate routing attacks in resource-constrained 6LoWPAN IoT networks.

This project is an independent implementation and extension of the Amrita B.Tech project framework, with additional improvements in spoofing detection, baseline comparisons, and an end-to-end integration pipeline.

---

## Technology Stack

* **Network Simulation:** Contiki-NG, Cooja
* **Programming Languages:** C, Python
* **Machine Learning:** TensorFlow, Keras, Scikit-learn
* **TinyML:** TensorFlow Lite
* **Reinforcement Learning:** Stable Baselines3
* **Data Processing:** Pandas, NumPy, Matplotlib

---

## System Architecture

```text
6LoWPAN Network
       ↓
Traffic Collection
       ↓
SDN Controller
       ↓
Feature Extraction
       ↓
TinyML Anomaly Detection
       ↓
Attack Classification
       ↓
RL Mitigation Agent
       ↓
Network Recovery
```

---

## Quick Start

### Phase 1: Environment Setup

```bash
cd phase1_setup
# Follow setup instructions in phase1_setup/README.md
```

### Phase 2: Network Simulation

```bash
cd phase2_simulation
# Follow phase2_simulation/README.md to run Cooja simulations
```

### Phase 3: TinyML Model Training

```bash
cd ../phase3_tinyml
jupyter notebook notebooks/
# Run notebooks sequentially: 01 → 06
```

### Phase 4: Reinforcement Learning Training

```bash
cd ../phase4_rl
python src/dqn_training.py
```

---

## Project Structure

```text
iot-security-project/
├── phase1_setup/         # Environment setup and dependencies
├── phase2_simulation/    # Cooja simulations and attack implementations
├── phase3_tinyml/        # TinyML anomaly detection models
├── phase4_rl/            # Reinforcement Learning agent training
├── integration/          # End-to-end integration pipeline
├── docs/                 # Documentation, diagrams, and reports
├── INTERVIEW_PREP.md     # Project interview questions and answers
└── README.md
```

---

## Project Phases

### Phase 1 – Environment Setup

* Install and configure Contiki-NG and Cooja
* Configure Python environment and dependencies
* Verify simulation and ML toolchain

### Phase 2 – IoT Network Simulation

* Build 6LoWPAN and RPL-based topology
* Implement routing attacks:

  * Selective Forwarding
  * Sinkhole
  * Spoofing
  * DDoS
* Generate network traffic datasets

### Phase 3 – TinyML-Based Anomaly Detection

* Feature extraction and preprocessing
* Train lightweight autoencoder model
* Perform anomaly detection and attack classification
* Compare against traditional machine learning baselines

### Phase 4 – Reinforcement Learning Mitigation

* Train RL agent for adaptive response
* Learn optimal mitigation strategies
* Evaluate network recovery and resilience

---

## Experimental Evaluation (In Progress)

The following metrics will be reported after completing the experiments:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Packet Delivery Ratio (PDR)
* Detection Latency
* Mitigation Success Rate

Results will be added after the completion of the TinyML and Reinforcement Learning evaluation phases.

---

## Planned Enhancements

* Investigate identity consistency features to improve spoofing detection.
* Compare LSTM Autoencoder against Random Forest and other baselines.
* Develop an end-to-end integration pipeline.
* Build a real-time monitoring dashboard.

---

## How to Use This Repository

1. Start with `phase1_setup/` for environment installation.
2. Follow `phase2_simulation/README.md` to generate datasets.
3. Execute notebooks in `phase3_tinyml/notebooks/` sequentially.
4. Train and evaluate the RL agent using:

```bash
python phase4_rl/src/dqn_training.py
```

5. Run the complete pipeline:

```bash
python integration/pipeline.py
```

---

## Project Status

* [x] Environment Setup and Verification
* [ ] Network Simulation and Attack Implementation
* [ ] TinyML Anomaly Detection
* [ ] Reinforcement Learning Evaluation
* [ ] End-to-End Integration
* [ ] Final Documentation and Dashboard

**Current Status:** Development and experimentation in progress.

**Last Updated:** 2026-07-01

---

## Future Work

* Deploy on physical IoT hardware.
* Support additional routing attacks.
* Explore Graph Neural Network-based intrusion detection.
* Investigate Federated Learning for distributed security.
* Develop a real-time web dashboard for network monitoring.

---

## Interview Preparation

Project-related questions and answers are available in:

```text
INTERVIEW_PREP.md
```

---

## Author

**Yashwanth Maloth**
B.Tech Information Technology
VNR Vignana Jyothi Institute of Engineering and Technology (VNR VJIET)

---

*AI-Driven Security for Resource-Constrained IoT Networks using SDN, TinyML, and Reinforcement Learning.*
