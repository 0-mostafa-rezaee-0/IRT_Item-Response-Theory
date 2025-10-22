## 🧰 How to Use This Template

Click the green **"Use this template"** button at the top of the page, then choose **"Create a new repository"**.

This will create your own copy of this project, which you can modify freely — no need to fork!

---

<div align="center">
    <img src="figures/banner.png" alt="banner" width="50%">
</div>

<h1 align="center">Item Response Theory (IRT)</h1>

<p align="center">A practical introduction to Item Response Theory for AI-based adaptive testing</p>

## 1. Project Overview

This repository provides a concise, practical introduction to Item Response Theory (IRT) — the psychometric framework that powers modern adaptive tests like GRE, GMAT, and PTE. The goal is to help AI engineers and data scientists gain practical understanding of IRT to work effectively on adaptive testing systems, without requiring an extensive background in psychometrics.

## 2. Repository Structure

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

## 3. Quick Start

### 3.1 Setup

1. Clone this repository
2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

### 3.2 Generate Data

```
python scripts/generate_irt_data.py
```

This will create synthetic IRT data files in the `data/` directory.

### 3.3 Run IRT Simulation

```
python scripts/example_irt_simulation.py
```

This will:
1. Generate visualizations of Item Characteristic Curves
2. Simulate an adaptive test
3. Save output images to the `docs/` directory

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
