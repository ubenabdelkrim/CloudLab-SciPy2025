# ☁️ CloudLab-SciPy2025

This repository contains hands-on examples for processing large-scale scientific data in the cloud using:

- [**Dataplug**](https://github.com/CLOUDLAB-URV/dataplug): Unified data access from cloud storage.
- [**Lithops**](https://github.com/lithops-cloud/lithops): Serverless framework for scalable parallel processing.

---

## 🚀 Quick Start (Recommended): Use [pyrun.cloud](https://pyrun.cloud)

This tutorial is designed to run **seamlessly** on [**pyrun.cloud**](https://pyrun.cloud), a cloud-based JupyterLab platform with:

✅ Pre-installed dependencies  
✅ Auto-configured Lithops backend  
✅ Direct support for Dataplug and serverless workflows

> 🟢 No setup required — just launch the notebooks and start experimenting!

---

## 🧪 Running the Examples

### 📁 Example 1 – Using Dataplug Locally

Notebook: [`dataplug_example.ipynb`](dataplug_example.ipynb)

This notebook shows how to:

1. Load a FASTA file from an S3 bucket using `CloudObject.from_s3`
2. Explore metadata (e.g., number of sequences)
3. Preprocess and split the file into chunks
4. Partition the data for analysis

Run it on pyrun or locally with:

```bash
jupyter notebook dataplug_example.ipynb
```

---

### ☁️ Example 2 – Scalable Processing with Dataplug + Lithops

Notebook: [`dataplug_lithops.ipynb`](dataplug_lithops.ipynb)

This notebook demonstrates how to scale the same processing logic to the cloud using Lithops:

- Partition the FASTA file with `co.partition(...)`
- Apply `process_fasta_partition` to each slice
- Launch parallel processing with `lithops.FunctionExecutor`

Run it on pyrun or locally with:

```bash
jupyter notebook dataplug_lithops.ipynb
```

> ✅ The integration between Dataplug and Lithops is native — no code changes needed to go from local to serverless!

---

## 💻 Running Locally (Optional)

If you prefer to run the notebooks locally instead of pyrun, follow these steps:

### 📦 Install required libraries

```bash
pip install git+https://github.com/CLOUDLAB-URV/dataplug
pip install lithops
```

### ⚙️ Configure Lithops

To execute functions in the cloud (AWS, IBM Cloud, Azure, etc.), you’ll need to configure your Lithops backend manually.

You can follow the official guide here:  
👉 https://github.com/lithops-cloud/lithops#configuration

Create a `lithops_config.yaml` file with your credentials and backend options.

---

## 📚 Requirements

- Python 3.10 or higher
- Access to an S3-compatible storage (e.g., AWS S3, MinIO)
- Internet connection
- Cloud credentials (automatically set in pyrun, or configured manually for local runs)

---

## 📣 About

This code is part of the **CloudLab-SciPy2025** tutorial series for scientific computing in the cloud.  

---
