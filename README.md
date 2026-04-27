# Financial Fraud Detection using Big Data & HPC

## 📌 Project Overview
This project implements an end-to-end Financial Fraud Detection system. It leverages Big Data technologies for distributed preprocessing of massive transaction datasets and High-Performance Computing (HPC) techniques to accelerate the training of deep learning anomaly detection models. 

## 🛠 Tech Stack & Architecture

**Big Data Processing:**
* **HDFS:** Distributed storage for large-scale datasets.
* **Apache Spark (PySpark):** Distributed data preprocessing, feature scaling, and data export.

**High-Performance Computing (HPC) & Deep Learning:**
* **Frameworks:** TensorFlow / PyTorch
* **Models:** Autoencoder / LSTM 
* **Acceleration:** GPU-accelerated training, mini-batch parallel processing, and optimized resource allocation.

**API & Deployment (DevOps):**
* **API:** RESTful endpoint serving (`/predict`) with batch inference support.
* **Containerization:** Docker, Docker Compose for isolated environment setup and volume mounting (data + model).

---

## 🚀 Project Phases & Implementation

### 1. Data Pipeline (Big Data)
* **Data Ingestion:** Load raw financial transaction datasets into HDFS.
* **Distributed Preprocessing:** Handle missing values, categorical encoding, and feature scaling natively on Spark clusters.
* **Data Export:** Convert processed DataFrames into optimized training formats for deep learning ingestion.

### 2. Model Training (HPC)
* **Architecture Design:** Implement Autoencoder/LSTM networks designed for anomaly and fraud sequence detection.
* **Parallel Computing Strategy:** Utilize data parallelism and optimized mini-batch processing across GPUs.
* **Optimization:** Focus on minimizing epoch duration, maximizing GPU memory throughput, and tuning anomaly thresholds for optimal precision/recall.

### 3. API Development
* **Inference Engine:** Load trained models into a lightweight serving environment.
* **Endpoints:** Expose a `/predict` endpoint equipped to handle JSON payloads for real-time and batch fraud inference.

### 4. DevOps & Infrastructure
* **Containerization:** `Dockerfile` created for consistent environment replication.
* **Orchestration:** `docker-compose.yml` to spin up the API, model server, and necessary volumes for data and model artifacts.

---

## ⚙️ Getting Started

### Prerequisites
* [Docker](https://www.docker.com/) & [Docker Compose](https://docs.docker.com/compose/)
* NVIDIA GPU with CUDA support (for HPC training)
* Git

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/NguyenPhanNhatLan/FraudDetection.git](https://github.com/NguyenPhanNhatLan/FraudDetection.git)
   cd FraudDetection
