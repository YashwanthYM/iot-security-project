# Installation Guide – Phase 1 Setup

This document covers the installation and setup of all dependencies required for the **AI-Driven IoT Security: Detecting and Preventing Routing Attacks in SDN-Enabled 6LoWPAN Networks** project.

---

# System Requirements

* **Operating System:** Ubuntu 20.04 LTS or Ubuntu 22.04 LTS (Recommended)
* **Alternative Platforms:** macOS or WSL2
* **RAM:** Minimum 8 GB (16 GB recommended for simulations and ML workloads)
* **Storage:** At least 10 GB of free disk space
* **Java:** JDK 11 or later
* **Python:** Python 3.8+ (Python 3.10+ recommended)

---

# Prerequisites

## 1. Update System Packages

```bash
sudo apt update
sudo apt upgrade -y
```

## 2. Install Java Development Kit (JDK)

```bash
sudo apt install -y openjdk-11-jdk openjdk-11-jdk-headless
java -version
javac -version
```

Expected output:

```text
openjdk version "11.x.x"
javac 11.x.x
```

---

## 3. Install Build Tools

```bash
sudo apt install -y \
build-essential \
git \
wget \
curl \
ant \
doxygen \
graphviz
```

Verify:

```bash
git --version
ant -version
```

---

## 4. Install Python and Development Tools

```bash
sudo apt install -y \
python3 \
python3-pip \
python3-venv \
python3-dev
```

Verify:

```bash
python3 --version
pip3 --version
```

---

# Phase 1 Installation Steps

## Step 1 – Clone Contiki-NG

```bash
cd ~

git clone https://github.com/contiki-ng/contiki-ng.git
cd contiki-ng

git submodule update --init --recursive
```

---

## Step 2 – Configure Contiki-NG Environment Variables

Add the following lines to your `~/.bashrc`:

```bash
echo 'export CONTIKI_NG_HOME=$HOME/contiki-ng' >> ~/.bashrc
echo 'export PATH=$CONTIKI_NG_HOME/tools/cc-tool:$PATH' >> ~/.bashrc
```

Reload:

```bash
source ~/.bashrc
```

Verify:

```bash
echo $CONTIKI_NG_HOME
```

Expected output:

```text
/home/<username>/contiki-ng
```

---

## Step 3 – Compile and Launch Cooja

```bash
cd $CONTIKI_NG_HOME/tools/cooja

ant clean
ant run
```

The first build may take several minutes.

If successful, the Cooja simulator window should open.

Close the simulator after verifying that it launches correctly.

---

## Step 4 – Clone the Project Repository

```bash
cd ~/projects

git clone https://github.com/YashwanthYM/iot-security-project.git
cd iot-security-project
```

Configure Git:

```bash
git config user.name "Yashwanth"
git config user.email "your-email@example.com"
```

---

## Step 5 – Create Python Virtual Environment

From the project root:

```bash
python3 -m venv venv
```

Activate:

```bash
source venv/bin/activate
```

Your terminal prompt should now begin with:

```text
(venv)
```

---

## Step 6 – Create Requirements File

Create:

```text
requirements-phase1.txt
```

with the following contents:

```text
numpy>=1.21.0
pandas>=1.3.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
notebook>=6.4.0
ipykernel>=6.0.0
pytest>=6.2.5
pyyaml>=5.4.0
```

Install dependencies:

```bash
pip install -r requirements-phase1.txt
```

---

## Step 7 – Configure Jupyter Kernel

```bash
python -m ipykernel install --user --name=iot-security-project
```

Verify:

```bash
jupyter kernelspec list
```

---

## Step 8 – Verify Project Structure

```bash
tree -I '.git'
```

Expected structure:

```text
iot-security-project/
├── README.md
├── .gitignore
├── INTERVIEW_PREP.md
├── docs/
├── integration/
├── phase1_setup/
├── phase2_simulation/
├── phase3_tinyml/
└── phase4_rl/
```

---

# Verification Checklist

## Check Ubuntu Version

```bash
lsb_release -a
```

---

## Check Java Installation

```bash
java -version
javac -version
```

---

## Check Git

```bash
git --version
```

---

## Check Python Environment

```bash
source venv/bin/activate

python --version
pip --version
```

---

## Verify Python Libraries

```bash
python -c "import numpy, pandas, sklearn; print('✓ ML libraries OK')"
```

Expected output:

```text
✓ ML libraries OK
```

---

## Verify Contiki-NG

```bash
echo $CONTIKI_NG_HOME
ls $CONTIKI_NG_HOME/tools/cooja
```

---

## Verify Cooja Launch

```bash
cd $CONTIKI_NG_HOME/tools/cooja
ant run
```

If the simulator window opens successfully, the installation is complete.

---

# Troubleshooting

## Issue: Cooja Fails to Compile

Check Java version:

```bash
java -version
javac -version
```

If necessary:

```bash
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

---

## Issue: Python Import Errors

Reinstall dependencies:

```bash
pip install --upgrade --force-reinstall -r requirements-phase1.txt
```

---

## Issue: Contiki-NG Path Not Recognized

Verify:

```bash
echo $CONTIKI_NG_HOME
```

If empty:

```bash
source ~/.bashrc
```

---

## Issue: `ant` Command Not Found

Install Ant:

```bash
sudo apt install ant
```

---

## Issue: Jupyter Cannot Find Kernel

Reinstall kernel:

```bash
python -m ipykernel install --user --name=iot-security-project
```

---

# Next Steps

After completing Phase 1:

1. Create a basic Cooja simulation and verify packet transmission.
2. Build the 6LoWPAN and RPL network topology.
3. Implement baseline client and server motes.
4. Generate initial network logs for the TinyML pipeline.
5. Proceed to `phase2_simulation/README.md`.

---

# Additional Resources

* Contiki-NG Documentation: https://docs.contiki-ng.org/
* Cooja Simulator Guide: https://docs.contiki-ng.org/en/develop/doc/guides/cooja.html
* 6LoWPAN Overview: https://en.wikipedia.org/wiki/6LoWPAN

---

**Last Updated:** 2026-07-02
**Maintained By:** Yashwanth Maloth
