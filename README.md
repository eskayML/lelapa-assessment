# LELAPA Assessment Submission

## Contents
- `LELAPA SUBMISSION.ipynb`: Main notebook containing Exploratory Data Analysis (EDA), Exploratory Model Analysis (EMA), and Error Analysis.
- `README.md`: Instructions to run and reproduce results.
- `Dockerfile` or `requirements.txt`: Environment setup (choose one).

## How to Run
<a href="https://colab.research.google.com/github/eskayML/lelapa-assessment/blob/main/LELAPA%20SUBMISSION.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

>[!TIP]
> Opening the notebook in Colab with T4 GPU Enabled is the most recommended method to run this Notebook. Other ways of setting it up are listed below

### 1. Environment Setup

#### Option A: Using Docker (Recommended for reproducibility)
1. Ensure you have [Docker](https://www.docker.com/) installed.
2. Build the Docker image:
   ```
   docker build -t lelapa-assessment .
   ```
3. Run the container:
   ```
   docker run -p 8888:8888 -v %cd%:/workspace lelapa-assessment
   ```
4. Open the Jupyter Notebook link shown in the terminal (usually http://localhost:8888).

#### Option B: Local Python Environment
1. Install [Python 3.8+](https://www.python.org/downloads/).
2. (Recommended) Create a virtual environment:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
4. Start Jupyter:
   ```
   jupyter notebook
   ```
5. Open `LELAPA SUBMISSION.ipynb` and run all cells.


### 2. Data Download & Folder Structure
The notebook automatically downloads the required dataset from Google Drive. If you already have the data, ensure that the `dataset_v2` folder is placed inside the project folder (same location as the notebook and README).

**Folder structure should look like:**

```
lelapa-assessment/
├── LELAPA SUBMISSION.ipynb
├── README.md
├── requirements.txt
├── Dockerfile
└── dataset_v2/
    ├── transcriptions.csv
    └── audios/
        └── ...
```

## Troubleshooting
- If you encounter missing package errors, ensure all dependencies are installed (see `requirements.txt`).
- For Docker, make sure your local folder is mounted to `/workspace` in the container.

## Contact
For any issues, please reach out to the assessment organizer.
