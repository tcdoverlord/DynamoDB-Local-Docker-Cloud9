# ☁️ DynamoDB Local Deployment with AWS Cloud9

A hands-on AWS project demonstrating how to deploy and manage **DynamoDB Local** within an **AWS Cloud9** development environment using **Docker**, **Docker Compose**, **Python automation**, and **Linux administration**.

This project provides a lightweight local database environment for development, testing, and learning DynamoDB workflows without consuming AWS resources.

---

# 🚀 Project Overview

This project walks through the complete setup process for:

✅ AWS Cloud9 Development Environment

✅ DynamoDB Local Deployment

✅ Docker Container Management

✅ DynamoDB Admin Web Interface

✅ Python-Based Environment Preparation

✅ Linux Bash Administration

---

# 🛠️ Technologies Used

* AWS Cloud9
* Amazon DynamoDB Local
* Docker
* Docker Compose
* Python 3
* Linux Bash
* YAML Configuration

---

# 🎯 Skills Demonstrated

This project showcases practical experience with:

* Cloud Development Environments
* Infrastructure Automation
* Containerized Applications
* Database Deployment
* Linux System Administration
* Python Scripting
* DevOps Workflows
* AWS Development Tools

---

# 📋 Prerequisites

Before beginning, ensure the following are installed:

* AWS Cloud9 Environment
* Docker
* Docker Compose
* Python 3
* Sudo Privileges

Verify installation:

```bash
docker --version
docker-compose --version
python3 --version
```

---

# 📂 Step 1 — Navigate to Home Directory

Move to your Cloud9 home directory:

```bash
cd ..
ls -l
```

Verify that you are working within your user home folder before creating files.

---

# 🐍 Step 2 — Create Python Setup Script

Create a file named:

```text
setup_dynamodb.py
```

This script creates the required DynamoDB data directory and applies permissions needed for local storage.

```python
import os

def setup_dynamodb_local():

    dynamodb_data_path = "/home/dynamodb/data"

    try:
        os.makedirs(dynamodb_data_path, exist_ok=True)

        print(
            f"Directory created or already exists: {dynamodb_data_path}"
        )

        os.chmod(dynamodb_data_path, 0o777)

        print(
            f"Permissions set to 777 for: {dynamodb_data_path}"
        )

    except PermissionError:
        print(
            "Permission denied. Run with elevated privileges."
        )

    except Exception as e:
        print(f"An error occurred: {e}")

if __name__ == "__main__":
    setup_dynamodb_local()
```

---

# 🐳 Step 3 — Create Docker Compose Configuration

Create a file named:

```text
docker-compose.yml
```

Paste the following configuration:

```yaml
version: '3.8'

services:

  dynamodb-local:
    image: amazon/dynamodb-local:latest
    container_name: dynamodb-local
    command: "-jar DynamoDBLocal.jar -sharedDb -dbPath ./data"

    ports:
      - "8002:8000"

    restart: always

    volumes:
      - "./data:/home/dynamodblocal/data"

    working_dir: /home/dynamodblocal

  dynamodb-admin:
    image: aaronshaf/dynamodb-admin
    container_name: dynamodb-admin

    depends_on:
      - dynamodb-local

    restart: always

    ports:
      - "8001:8001"

    environment:
      - DYNAMO_ENDPOINT=http://dynamodb-local:8000
      - AWS_REGION=us-east-2
```

---

# ⚙️ Step 4 — Initialize Storage

Run the setup script:

```bash
sudo python3 setup_dynamodb.py
```

This creates the required DynamoDB storage directory and permissions.

---

# 📦 Step 5 — Download DynamoDB Local

Pull the official DynamoDB Local container:

```bash
sudo docker pull amazon/dynamodb-local
```

---

# ▶️ Step 6 — Start Services

Run interactively:

```bash
sudo docker-compose up
```

Or run in the background:

```bash
sudo docker-compose up -d
```

---

# 🔍 Step 7 — Verify Deployment

Check running containers:

```bash
sudo docker ps
```

Verify Docker Compose:

```bash
docker-compose --version
```

Verify created files:

```bash
ls -l
```

---

# 🌐 Access DynamoDB Admin

After deployment:

| Service        | URL                   |
| -------------- | --------------------- |
| DynamoDB Admin | http://localhost:8001 |
| DynamoDB Local | http://localhost:8002 |

---

# 🧠 Learning Outcomes

By completing this project you gain experience with:

* AWS Cloud9
* DynamoDB Local
* Docker Containers
* Docker Networking
* Linux Administration
* Python Automation
* Cloud Development Workflows
* Infrastructure Deployment

---

# 🏗️ Project Purpose

This project was created to demonstrate practical cloud administration and development skills by building a local DynamoDB environment using AWS Cloud9 and modern containerization technologies.

The focus is on repeatable deployments, automation, and hands-on AWS learning.

---

# 👨‍💻 Author

**TCD_Overlord**

GitHub:

https://github.com/tcdoverlord

---

# 📄 License

This project is released under the MIT License.
