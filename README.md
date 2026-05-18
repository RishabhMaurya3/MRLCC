# MRLCC: Adaptive Cloud Task Scheduling using Meta Reinforcement Learning

## Project Overview

This project implements MRLCC (Meta Reinforcement Learning for Cloud Computing), an adaptive cloud task scheduling framework designed to optimize task allocation and resource utilization in cloud environments.

The model uses:

- Reinforcement Learning (RL)
- Meta Reinforcement Learning
- Markov Decision Process (MDP)
- Cloud workload traces (Azure & Tencent datasets)

The objective is to improve:

- Task scheduling efficiency
- Load balancing
- Resource utilization
- Execution time
- Scheduling performance in dynamic cloud environments

## Project Folder Structure

```
project/
│
├── data/                  # Input datasets
│   ├── azure_raw.csv
│   └── batch_task.csv
│
├── output/                # Generated outputs/results
│
├── dataset.py             # Dataset loading and preprocessing
├── environment.py         # Cloud environment simulation
├── evaluation.py          # Evaluation metrics and testing
├── heuristics.py          # Baseline heuristic scheduling methods
├── main.py                # Main execution file
├── model.py               # RL/MRLCC model implementation
├── scenarios.py           # Scenario generation/configuration
│
└── README.md
```

## System Requirements

### Software Requirements

- Python 3.9 or above
- pip package manager

### Recommended Hardware

- Minimum 8 GB RAM
- Multi-core CPU
- GPU optional (recommended for faster training)

## Installation Guide

### Step 1: Clone or Download Project

```bash
git clone <repository-url>
```

OR simply extract the project ZIP.

### Step 2: Open Project Folder

Open terminal or command prompt inside the project directory.

Example:

```bash
cd project-folder
```

### Step 3: Create Virtual Environment (IMPORTANT)

#### For Windows

```bash
python -m venv venv
```

Activate environment:

```bash
venv\Scripts\activate
```

#### For Linux / macOS

```bash
python3 -m venv venv
```

Activate environment:

```bash
source venv/bin/activate
```

### Step 4: Install Required Libraries

Install dependencies:

```bash
pip install numpy pandas matplotlib torch gym tqdm scikit-learn tensorflow
```

## Dataset Setup

Place datasets inside the `data/` folder:

```
data/
├── azure_raw.csv
└── batch_task.csv
```

Datasets used:

- Azure workload trace
- Tencent batch task dataset

## Running the Project

### Normal Execution

Run the complete MRLCC training:

```bash
python main.py --azure data\azure_raw.csv --tencent data\batch_task.csv
```

### Fast Execution Mode (Recommended for Testing)

If you want faster execution with smaller iterations and reduced training time:

```bash
python main.py --fast --azure data\azure_raw.csv --tencent data\batch_task.csv
```

### Fast Mode Benefits

- Smaller training iterations
- Faster execution
- Quick testing/debugging
- Suitable for low-end systems

Use `--fast` if:

- You want quick results
- You are testing code changes
- Your system has limited resources

## Output Results

Generated outputs and evaluation results will be stored inside:

```
output/
```

Outputs include:

- **Figure 5**: Comparison of scheduling performance across 3 scenarios
- **Figure 6**: Performance analysis with varying CPU configurations (CPU=12 and CPU=15 cases)
- **Performance Metrics Table**: Comprehensive comparison of algorithms
