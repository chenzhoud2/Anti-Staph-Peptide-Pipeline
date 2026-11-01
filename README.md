# 1 Interpretable Machine Learning Pipeline for Anti-Staphylococcal Peptides
This repository contains the complete source code and instructions for reproducing the results in our paper:"A lightweight, homology-audited machine learning pipeline for Pareto screening of anti-staphylococcal peptides with balanced efficacy and safety". 

# 2 Repository Structure
*   `main.ipynb`: The complete pipeline for data processing, feature extraction, model training, evaluations, and generation of all figures and tables.
*   `requirements.txt`: Python dependencies required to run the code.
*   `data/`: Folder where you need to place the downloaded dataset (not included in GitHub).
*   `results/`: Folder that will be automatically created to save all generated figures (`.png`) and tables (`.csv`).

# 3 Environment Setup
We recommend using **Anaconda** to manage the environment. The code was tested on **Python 3.10**.

## Step 1: Create a Virtual Environment
Open your Anaconda Prompt (or terminal) and run:
```bash
conda create -n projectamp python=3.10 -y
conda activate projectamp

## Step 2: Install Dependencies
We have provided a requirements.txt file. To install all required packages, run:
```bash
pip install -r requirements.txt
(Note for users in China: If the download is slow, you can add the Tsinghua mirror by appending -i https://pypi.tuna.tsinghua.edu.cn/simple to the command above.)

## Step 3: Launch Jupyter Lab
Navigate to the project directory (where main.ipynb is located) and launch Jupyter:
cd /path/to/your/AMP-Project
jupyter lab

Important: Make sure to select the kernel of the environment you just created (e.g., Python (projectamp)).

# 4 Data Preparation
The datasets generated and analyzed during this study are available in the Zenodo repository (DOI: https://doi.org/10.5281/zenodo.23788823).
Download the dataset archive and extract it.
Place the 4 provided .csv files (mic_train_val.csv, mic_external_test.csv, hemo_train_clean.csv, hemo_external_test.csv) directly into the data/ folder in the root directory of this project.
(Note: To strictly comply with the data usage policies of DBAASP and HemoPI2, we only provide the cleaned intermediate datasets. The raw downloaded database files are not redistributed. The provided 4 files are exactly the inputs required to start the pipeline from Module 2.)


# 5 How to Reproduce the Results
Open the main.ipynb in Jupyter Notebook or JupyterLab.
Ensure your kernel is set to the environment with the installed requirements (e.g., projectamp).
Click "Kernel" -> "Restart & Run All" (or "Run All").

Important Notes:
1）Module 1 (Raw Data Cleaning) is commented out by default, as the raw database files cannot be redistributed. The pipeline starts directly from Module 2 using the 4 intermediate datasets provided in the Zenodo archive.
2）Computation Time: Please note that running the entire pipeline (from Module 2 to the final figure generation) may take approximately 25 minutes in total, depending on your CPU performance.
3）All final figures (Fig 2-4, Fig S1-S5) and tables (Table 1-4, Table S1-S4,S5-S9) will be automatically generated and saved in the results/ folder.
