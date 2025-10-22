## 🧰 How to Use This Template

Click the green **"Use this template"** button at the top of the page, then choose **"Create a new repository"**.

This will create your own copy of this project, which you can modify freely — no need to fork!

---

<div align="center">
    <img src="figures/banner.png" alt="banner" width="50%">
</div>

<h1 align="center">Item Response Theory (IRT)</h1>

<p align="center">A practical introduction to Item Response Theory for AI-based adaptive testing</p>

You've likely encountered standardized tests like GRE, GMAT, TOEFL, or IELTS—these aren't just traditional exams, but sophisticated adaptive testing systems that dynamically adjust to your ability level, delivering precise measurements in half the time. This repository explores the mathematical foundation behind these systems: Item Response Theory (IRT), which models the relationship between your ability, question characteristics, and response probabilities. As the world moves toward AI-powered assessment, understanding IRT becomes crucial for building the next generation of intelligent testing systems that combine mathematical rigor with machine learning capabilities.

## 1. Quick Start

### 1.1 Prerequisites
- Docker and Docker Compose installed on your system
- VS Code with Dev Containers extension

### 1.2 Setup and Run

**Step 1: Clone and Navigate**
```bash
git clone <repository-url>
cd IRT_Item-Response-Theory
```

**Step 2: Build and Run Container**
```bash
# Make start.sh executable (if not already)
chmod +x start.sh

# Build and run the container
./start.sh
```

**Alternative method:**
```bash
docker-compose up --build -d
```

**Step 3: Verify Container**
```bash
docker-compose ps
```
Ensure the container status is "Up" and port 8888 is mapped.

**Step 4: Run Python Scripts**

```bash
# First, find your container name
docker-compose ps

# Enter the container and navigate to scripts directory
docker exec -it <container_name> bash
cd /app/scripts

# Run scripts one by one
python generate_irt_data.py
python example_irt_simulation.py
```

**Step 5: Work with Jupyter Notebooks**

1. **Attach VS Code to Container:**
   - Press `Ctrl+Shift+P` to open command palette
   - Select `Dev Containers: Attach to Running Container…`
   - Choose your project container
   - In the new VS Code window, click "Open Folder" → select `/root/app`
   - Install extensions: Docker, Dev Containers, Python, and Jupyter

2. **Select Kernel and Run Notebooks:**
   - Open `notebooks/1_IRT_Data_Generator.ipynb` or `notebooks/2_IRT_Exploratory_Analysis.ipynb`
   - Select the correct kernel (should auto-detect)
   - Start exploring IRT concepts by running cells!

**Step 6: Stop Container**
```bash
docker-compose down
```

### 1.3 Access Jupyter in Browser
Visit `localhost:8888/tree` to access Jupyter interface directly.

### 1.4 Update Environment
To rebuild with changes:
```bash
docker-compose up --build
```

To update dependencies:
```bash
# Inside container
pip freeze > requirements.txt
```

## 2. Project Overview

This repository provides a concise, practical introduction to Item Response Theory (IRT) — the psychometric framework that powers modern adaptive tests like GRE, GMAT, and PTE. The goal is to help AI engineers and data scientists gain practical understanding of IRT to work effectively on adaptive testing systems, without requiring an extensive background in psychometrics.

## 3. Repository Structure

```
.
├── docs/                    # Documentation and visualizations
│   └── README.md            # Conceptual overview of IRT
├── data/                    # Data for IRT examples
│   └── README.md            # Dataset documentation
├── scripts/                 # Python implementation
│   ├── generate_irt_data.py # Generate synthetic IRT data
│   ├── example_irt_simulation.py # Core IRT simulation
│   └── README.md            # Script documentation
├── requirements.txt         # Python dependencies
└── README.md                # This file
```

## 4. Learning Path

To get the most from this repository:

1. Start by reading `docs/README.md` for a conceptual overview of IRT
2. Examine the data structure described in `data/README.md`
3. Run the example scripts and review their output
4. Explore the code in `scripts/example_irt_simulation.py` to see IRT in action
5. Experiment by modifying parameters and observing the effects

## 5. Key Takeaways

After exploring this repository, you should understand:

- How IRT models the relationship between ability and item performance
- The meaning and impact of item parameters (difficulty, discrimination, guessing)
- How adaptive tests select items to maximize measurement precision
- The basic mathematics behind IRT probability functions
- How to simulate responses based on IRT models

## 6. About This Project

This repository provides a foundation for understanding the psychometric principles that underlie adaptive testing systems, enabling AI engineers to collaborate effectively with psychometricians in developing next-generation assessment platforms.
