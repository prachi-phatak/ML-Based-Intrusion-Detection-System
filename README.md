# ML-Based-Intrusion-Detection-System

ML-Based Intrusion Detection System is a cybersecurity solution that leverages Machine Learning to identify and classify network attacks such as DoS, DDoS, Brute Force, Botnet, Infiltration, and Web Attacks. The project includes data preprocessing, class imbalance handling, 5-fold cross-validation, comprehensive performance evaluation, feature importance analysis, model saving/loading, and custom attack prediction for enhanced network security.

Overview

This project covers the complete ML workflow — from raw data ingestion and quality checks to model training, evaluation, and custom predictions on new traffic samples.

Attack types detected:
DoS (Denial of Service)
DDoS (Distributed Denial of Service)
Brute Force
Botnet
Infiltration
Web Attack (SQL Injection, XSS, CSRF)

<img width="771" height="620" alt="image" src="https://github.com/user-attachments/assets/d987a801-c845-4033-916d-40b8a6b0e490" />

About Dataset
The dataset used for this project is hosted on Google Drive due to its large size and is not included in this repository.
Dataset Link: https://drive.google.com/drive/u/7/folders/11kLak3ED_C01yZGzEy0t-qCHqNXHDyQC


Requirements: 
Python 3.8 or higher
pip
Git
Minimum 8 GB RAM (16 GB recommended when loading all 10 files)
Around 5 GB free disk space for the dataset and generated files


Setup and Installation

Step 1 — Clone the repository
git clone https://github.com/prachi-phatak/ML-Based-Intrusion-Detection-System.git
cd ML-Based-Intrusion-Detection-System

Step 2 — Install Python
For Windows:
Go to https://www.python.org/downloads/ and download Python 3.10 or higher. During installation, make sure to check "Add Python to PATH" before clicking Install. After installation, open Command Prompt and verify:
python --version
pip --version

For macOS:
Install via Homebrew (recommended):
brew install python@3.10
python3 --version
pip3 --version

Alternatively, download the installer from https://www.python.org/downloads/mac-osx/

For Linux (Ubuntu/Debian):
sudo apt update
sudo apt install python3 python3-pip python3-venv -y
python3 --version
pip3 --version

Step 3 — Create a virtual environment
A virtual environment keeps this project's dependencies separate from other Python projects on your machine. It is strongly recommended.
Windows — Command Prompt

python -m venv venv
venv\Scripts\activate

Windows — PowerShell
python -m venv venv
.\venv\Scripts\Activate.ps1

macOS and Linux
python3 -m venv venv
source venv/bin/activate

Once activated, your terminal prompt will show (venv) at the start. All packages installed from this point will be scoped to this environment only.

Step 4 — Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn joblib jupyter pyarrow

To install from requirements.txt on another machine:
pip install -r requirements.txt

Step 5 — Download the dataset

Download link: https://drive.google.com/drive/u/7/folders/11kLak3ED_C01yZGzEy0t-qCHqNXHDyQC

Download all 10 .parquet files from the link above. Then create the IDSDataset folder inside the project and place all files there. Also create a models folder for the saved model artifacts.

For Windows:
mkdir IDSDataset
mkdir models

Move the 10 downloaded .parquet files into the IDSDataset folder.

For macOS and Linux:
mkdir -p IDSDataset models
Move the 10 downloaded .parquet files into the IDSDataset folder.

Step 6 — Update the dataset path in the notebook
Open PrachIDS_Final__ETI1.ipynb and go to Cell 2. Find the DATASET_FOLDER variable and change it to match where you placed the IDSDataset folder on your machine.

For Windows:
DATASET_FOLDER = r'C:\Users\prachi-phatak\ML-Based-Intrusion-Detection-System
\IDSDataset'

For macOS:
DATASET_FOLDER = '/Users/prachi-phatak/ML-Based-Intrusion-Detection-System
/IDSDataset'

For Linux:
DATASET_FOLDER = '/home/prachi-phatak/ML-Based-Intrusion-Detection-System
/IDSDataset'

Step 7 — Launch the notebook
Make sure the virtual environment is still activated (you should see (venv) in your terminal), then run:
jupyter notebook PrachIDS_Final__ETI1.ipynb

Step 8 — Deactivate the virtual environment when done
deactivate


Tech Stack:
Python 3.10
scikit-learn (Decision Tree, cross-validation, metrics)
pandas and numpy
matplotlib and seaborn
joblib
Jupyter Notebook
CIC-IDS-2018 dataset


License
This project is licensed under the MIT License. See the LICENSE file for details.

