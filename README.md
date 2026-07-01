# IoT Security Project: 6LoWPAN Attack Detection & Mitigation

Implementation of SDN-enabled intrusion detection with TinyML and Reinforcement Learning for constrained IoT networks.

## Project Overview

This project implements an intelligent security framework for detecting and preventing routing attacks (Selective Forwarding, Sinkhole, Spoofing, DDoS) in 6LoWPAN networks using:
- Centralized SDN-based monitoring
- TinyML for lightweight anomaly detection
- Reinforcement Learning for autonomous mitigation

## Quick Start

```bash
# Phase 2: Network Simulation
cd phase2_simulation
# See README.md for Cooja setup

# Phase 3: Machine Learning
cd ../phase3_tinyml
jupyter notebook

# Phase 4: Reinforcement Learning  
cd ../phase4_rl
python src/dqn_training.py
```

## Project Structure

├── phase1_setup/           # Environment and tools setup
├── phase2_simulation/       # Cooja IoT network + attack implementations
├── phase3_tinyml/          # Anomaly detection models and evaluation
├── phase4_rl/              # Reinforcement learning agent training
├── integration/            # End-to-end pipeline
└── docs/                   # Documentation and analysis
## Technologies

- **Simulation:** Contiki-NG, Cooja
- **Language:** C (embedded), Python (ML/RL)
- **ML/RL:** TensorFlow, Keras, TinyML, Stable Baselines3
- **Data:** Pandas, NumPy, Scikit-learn

## Progress

- [x] Environment setup and verification
- [ ] Network simulation with attack implementation
- [ ] TinyML anomaly detection model
- [ ] RL-based mitigation framework
- [ ] Full integration and evaluation

---

Last updated: 01/07/2026
