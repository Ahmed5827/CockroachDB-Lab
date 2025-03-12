# CockroachDB Lab 🐞

This repository is a lab environment created to experiment with NewSQL databases, specifically CockroachDB. 

### 📌 Overview
In this lab, we will explore various CockroachDB commands using Python and Jupyter Notebook.
We will cover:

- CRUD operations (Create, Read, Update, Delete)
- Indexing for query optimization
- Transactions & Rollbacks
- System monitoring queries
- Time-travel queries (AS OF SYSTEM TIME)
- Performance analysis using CockroachDB internal tables
- Multi-Node CockroachDB cluster

### 🛠️ Prerequisites
Before running this lab, ensure you have the following installed:

#### 1️⃣ Docker (Required)
CockroachDB runs inside a Docker container.
If you haven't installed Docker yet, download and install it from the official site:
🔗 [Install Docker](https://docs.docker.com/desktop/setup/install/windows-install/)

#### 2️⃣ Python (Required)
This lab is written in Python 3.11.4, and it is recommended to use this version to avoid unexpected issues.

Check your Python version:

```sh
python --version
```

If Python is not installed, download it from:
🔗 [Install Python](https://www.python.org/downloads/)

### 📦 Setup
Follow these steps to set up your environment:

#### 1️⃣ Run the CockroachDB Container
Run the following command in your terminal to start CockroachDB inside Docker:

```sh
docker run -d --name cockroachdb -p 26257:26257 -p 8080:8080 cockroachdb/cockroach start-single-node --insecure
```
- -d → Runs the container in detached mode
- --name cockroachdb → Names the container
- -p 26257:26257 -p 8080:8080 → Maps ports for SQL and web UI
- start-single-node --insecure → Starts a single-node instance without authentication (for testing)

#### 2️⃣ Clone the Repository
```sh
git clone https://github.com/Ahmed5827/CockroachDB-Lab.git
cd CockroachDB-Lab
```

#### 3️⃣ Install Dependencies
Install the required Python libraries:

```sh
pip install -r requirements.txt
```

### 🚀 Running the Lab

#### 1️⃣ Launch Jupyter Notebook
Run:

```sh
jupyter notebook
```
Then open Lab.ipynb and start experimenting.

#### 2️⃣ If Jupyter Web Interface Has Issues
Some users may experience missing libraries when launching Jupyter via the browser.

#### 💡 Solution: Run Jupyter inside VS Code:

- Install the Jupyter extension in VS Code.
- Open the repository in VS Code.
- Run Jupyter inside VS Code's terminal.

### 🖥️ Using the CockroachDB CLI
If you want to interact directly with CockroachDB inside the container, use:

```sh
docker exec -it cockroachdb cockroach sql --insecure
```
This opens the CockroachDB interactive SQL shell.

### 📚 Repository Contents
File	Description
Lab.ipynb	Jupyter Notebook with all CockroachDB queries
requirements.txt	List of required Python libraries
README.md	This documentation

### 📌 Notes
⚠ This setup is for educational purposes only. In production, always run CockroachDB with authentication and proper security settings.

- For official CockroachDB documentation, visit: 🔗 [CockroachDB Docs](https://www.cockroachlabs.com/docs/cockroachcloud/learn-cockroachdb-sql)

### 🌟 Contribute & Feedback
Feel free to fork this repo, experiment, and suggest improvements!
If you find bugs or issues, open an issue in this repository.

Happy coding! 🚀🐞
