# ☁️ AWS Cloud9 Survival Guide

Troubleshooting and deployment guide documenting the process used to install AWS Cloud9, resolve dependency conflicts, and recover a fully functional Linux development environment.

---

# 🎯 Objective

Successfully deploy AWS Cloud9 while resolving installation and dependency issues involving:

➜ Java

➜ Python Virtual Environments

➜ Python 2.7 Legacy Requirements

➜ Pip

➜ Node.js

➜ NVM

➜ Linux Package Dependencies

---

# 🔍 Environment Verification

Before troubleshooting, verify the current environment.

## ☕ Java

Verify Java installation:

```bash
java --version
```

Installed Version:

```text
OpenJDK 21.0.7
```

---

# 🚀 AWS Cloud9 Installation

Cloud9 was installed using:

```bash
curl -L https://d3kgj69l4ph6w4.cloudfront.net/static/c9-install-2.0.0.sh | bash
```

Initial issues encountered:

❌ Missing Python virtual environment support

❌ Dependency installation failures

❌ Cloud9 setup unable to complete

---

# 🐍 Resolving Python Virtual Environment Dependencies

Install required packages:

```bash
sudo apt update

sudo apt install python3-venv
```

Additional packages installed:

➜ python3-pip-whl

➜ python3-setuptools-whl

➜ python3.13-venv

Verify functionality:

```bash
python3 -m venv testenv
```

Result:

✅ Python virtual environments functioning correctly

---

# ⚙️ Installing Python 2.7

Some Cloud9 components referenced legacy Python 2.7 packages.

Install Python 2.7:

```bash
sudo apt update

sudo apt install python2.7
```

Installed dependencies:

➜ libpython2.7-minimal

➜ libpython2.7-stdlib

➜ python2.7-minimal

Verify installation:

```bash
python2.7 --version
```

Expected Output:

```text
Python 2.7.18
```

Result:

✅ Python 2.7 installed successfully

---

# 📦 Installing Pip for Python 2.7

Download installer:

```bash
curl https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py
```

Install:

```bash
sudo python2.7 get-pip.py
```

Installed Components:

➜ pip 20.3.4

➜ setuptools 44.1.1

➜ wheel 0.37.1

Verify installation:

```bash
pip --version
```

Result:

✅ Pip operational

---

# ⚠️ Python 2.7 Notice

Python 2.7 has reached End-of-Life and should only be used when required by legacy software.

Recommended for modern projects:

✅ Python 3

✅ Virtual Environments

✅ Updated Dependencies

✅ Security Supported Packages

---

# 🟢 Installing Node.js with NVM

Install NVM:

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
```

Load NVM:

```bash
export NVM_DIR="$HOME/.nvm"

[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"

[ -s "$NVM_DIR/bash_completion" ] && . "$NVM_DIR/bash_completion"
```

Install Node.js:

```bash
nvm install node
```

Verify:

```bash
node --version
```

Installed Version:

```text
v23.10.0
```

Result:

✅ Node.js installed successfully

---

# 🔄 Resume Cloud9 Installation

After resolving dependencies:

```bash
curl -L https://d3kgj69l4ph6w4.cloudfront.net/static/c9-install-2.0.0.sh | bash
```

Result:

✅ Cloud9 installation completed successfully

---

# 🧪 Validation Checklist

Verify all required components before launching Cloud9.

### Java

```bash
java --version
```

### Python 2.7

```bash
python2.7 --version
```

### Python 3

```bash
python3 --version
```

### Pip

```bash
pip --version
```

### Node.js

```bash
node --version
```

---

# 🚀 Launch AWS Cloud9

Start Cloud9:

```bash
cloud9
```

Verify:

➜ Workspace loads successfully

➜ Terminal launches correctly

➜ Python environments function normally

➜ Node.js executes correctly

➜ No dependency errors appear

---

# 🔧 Troubleshooting Quick Reference

| Issue                    | Resolution                          |
| ------------------------ | ----------------------------------- |
| Missing venv module      | Install python3-venv                |
| Python dependency errors | Install Python 2.7 support          |
| Missing pip              | Install get-pip.py                  |
| Node.js unavailable      | Install through NVM                 |
| Cloud9 startup failure   | Re-run installer after dependencies |

---

# 📚 Skills Demonstrated

### ☁️ Cloud Engineering

➜ AWS Cloud9 Administration

➜ Development Environment Deployment

➜ Cloud Development Workflows

---

### 🐧 Linux Administration

➜ Package Management

➜ Environment Configuration

➜ Dependency Resolution

---

### 🐍 Development Tooling

➜ Python Environment Management

➜ Pip Administration

➜ Node.js Deployment

➜ NVM Configuration

---

### 🔍 Troubleshooting

➜ Installation Recovery

➜ Dependency Analysis

➜ Environment Validation

➜ Root Cause Investigation

---

# 🔄 Deployment Workflow

```text
START
  ↓
Verify Java
  ↓
Install Python VENV
  ↓
Install Python 2.7
  ↓
Install Pip
  ↓
Install NVM
  ↓
Install Node.js
  ↓
Resume Cloud9 Installation
  ↓
Validate Environment
  ↓
Launch Cloud9
  ↓
WORKING DEVELOPMENT ENVIRONMENT
```

---

# 🏗️ Project Purpose

AWS Cloud9 Survival Guide was developed as a practical cloud engineering and Linux administration project demonstrating:

➜ AWS Cloud9 Administration

➜ Dependency Troubleshooting

➜ Linux System Management

➜ Package Installation

➜ Environment Recovery

➜ Development Tool Configuration

➜ Cloud Engineering Fundamentals

➜ Technical Documentation

The project focuses on solving real-world deployment challenges commonly encountered when configuring cloud development environments.

---

# 👨‍💻 Author

**TCDOverLord**

GitHub:
https://github.com/tcdoverlord

---

# ⚠️ Disclaimer

This guide documents one successful deployment path and troubleshooting process. Software versions, package availability, and installation procedures may change over time. Always verify commands and dependencies before deployment in production or shared environments.
