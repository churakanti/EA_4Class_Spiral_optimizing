# Optimizing Hyperparameters for Deep Learning Models Using Evolutionary Algorithms: Solving the Four-Class Intertwined Spiral Classification Problem

<div align="center">

[![IEEE](https://img.shields.io/badge/IEEE-EIT%202025-blue.svg)](https://ieeexplore.ieee.org/document/11103665)
[![ResearchGate](https://img.shields.io/badge/ResearchGate-Paper-00CCBB.svg)](https://www.researchgate.net/publication/394575077)
[![Python](https://img.shields.io/badge/Python-3.8+-green.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Solving the Four-Class Intertwined Spiral Classification Problem**

[Paper](https://www.researchgate.net/publication/394575077) • [IEEE Xplore](https://ieeexplore.ieee.org/document/11103665) • [Citation](#citation)

</div>

---

## 📖 Overview

This repository contains the complete implementation of our **IEEE EIT 2025** paper addressing the challenging **four-class intertwined spiral classification problem** using evolutionary algorithms for hyperparameter optimization.

**Key Achievement:** Improved accuracy from **39% (baseline)** to **95% (optimized)** using evolutionary strategies and genetic algorithms.

### 🎯 Research Highlights

- **Novel Application**: First comprehensive study applying Evolution Strategies with 1/5 success rule to four-class spiral problem
- **Comparative Analysis**: ES(1+1) vs. Genetic Algorithms (DEAP) for DNN hyperparameter optimization
- **Reproducible Implementation**: Complete code, data generation, and visualization pipeline
- **Published Research**: Peer-reviewed and presented at IEEE EIT 2025

---

## 🚀 Quick Start

### Prerequisites
```bash
Python 3.8 or higher
TensorFlow 2.x
DEAP library
NumPy, Pandas, Matplotlib
```

### Installation
```bash
# Clone the repository
git clone https://github.com/churakanti/EA_4Class_Spiral_optimizing.git
cd EA_4Class_Spiral_optimizing

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook notebooks/spiral_classification.ipynb
```

---

## 📊 Results Summary

| Optimization Method | Accuracy | Average Loss | Key Characteristics |
|---------------------|----------|--------------|---------------------|
| **Baseline** (No optimization) | 39% | 1.32 | Manual hyperparameters, poor convergence |
| **ES(1+1)** with 1/5 rule | 93% | - | Adaptive step-size, efficient exploration |
| **Genetic Algorithm** (DEAP) | **95%** | - | Population-based, best overall performance |

### Key Findings

✅ **Evolutionary algorithms dramatically outperform manual tuning** (95% vs 39%)  
✅ **GA achieves highest accuracy** but ES(1+1) converges faster  
✅ **1/5 success rule** provides effective self-adaptation in ES  
✅ **Hyperparameter optimization is critical** for nonlinear classification tasks  

---

## 📁 Repository Structure
```
EA_4Class_Spiral_optimizing/
│
├── notebooks/
│   └── spiral_classification.ipynb    # Main implementation with detailed comments
│
├── paper/
│   ├── ICMI-EIT2025_v3cj.pdf         # Published IEEE paper
│   └── IEEE_EIT_paper                # Paper source files
│
├── presentation/
│   └── IEEE_EIT_Poster.pptx          # Conference poster presentation
│
├── results/
│   ├── spiral_results_summary.csv    # Experimental results data
│   └── optimization_logs.txt         # Hyperparameter optimization logs
│
├── figures/                           # Generated visualizations (created when running code)
│   ├── decision_boundaries.png       # Model decision boundaries
│   ├── convergence_plots.png         # Optimization convergence
│   └── accuracy_comparison.png       # Method comparison charts
│
├── requirements.txt                   # Python dependencies
├── README.md                          # This file
├── LICENSE                            # MIT License
└── .gitignore                        # Git ignore rules
```

---

## 🔬 Methodology

### Problem Definition
The **four-class intertwined spiral** is a challenging nonlinear classification benchmark where four spiral arms are interleaved in 2D space. Traditional neural networks struggle without proper hyperparameter tuning.

### Approach

**1. Data Generation**
- Synthetic four-class spiral dataset
- 1000 samples (250 per class)
- Controlled noise levels for difficulty adjustment

**2. Neural Network Architecture**
- Multi-layer Perceptron (MLP) with optimized architecture
- Hyperparameters optimized: neurons per layer, activation functions, learning rate, batch size
- Framework: TensorFlow 2.x / Keras

**3. Optimization Methods**

#### Evolution Strategy ES(1+1)
- **1/5 Success Rule**: Adaptive step-size control
  - Success rate > 1/5 → Increase step size (explore)
  - Success rate < 1/5 → Decrease step size (exploit)
- Single-parent, single-offspring strategy
- Mutation-based exploration

#### Genetic Algorithm (DEAP)
- Population-based evolutionary search
- Tournament selection (size=3)
- Two-point crossover
- Gaussian mutation
- Elitism preservation

---

## 📈 Visualization Examples

The implementation includes comprehensive visualization tools:

- **Decision Boundaries**: 2D contour plots showing model predictions across feature space
- **Convergence Plots**: Fitness evolution over generations
- **Hyperparameter Evolution**: Tracking of optimized parameters
- **Comparison Charts**: Side-by-side method performance analysis

*(Figures are generated automatically when running the notebook, check the Figures folder)*

---

## 📖 Citation

If you use this code or reference our work, please cite:
```bibtex
@inproceedings{churakanti2025optimizing,
  title={Optimizing Hyperparameters for Deep Learning Models Using Evolutionary Algorithms: Solving the Four-Class Intertwined Spiral Classification Problem},
  author={Churakanti, Siri Sri and Chung, CJ},
  booktitle={2025 IEEE International Conference on Electro Information Technology (EIT)},
  year={2025},
  organization={IEEE},
  doi={10.1109/EIT64491.2025.11103665}
}
```

---

## 📄 Publication

**Full Paper:**  
- [IEEE Xplore](https://ieeexplore.ieee.org/document/11103665)  
- [ResearchGate](https://www.researchgate.net/publication/394575077)

**Conference:** IEEE International Conference on Electro/Information Technology (EIT) 2025  
**Presentation:** Oral presentation and poster session  

---

## 🛠️ Technical Details

### Optimized Hyperparameters

| Parameter | Search Space | Optimal (GA) | Optimal (ES) |
|-----------|--------------|--------------|--------------|
| Layer 1 Neurons | 16-128 | 96 | 84 |
| Layer 2 Neurons | 16-64 | 48 | 42 |
| Learning Rate | 0.0001-0.1 | 0.005 | 0.008 |
| Batch Size | 16, 32, 64, 128 | 32 | 64 |
| Activation | relu, tanh, sigmoid | tanh | relu |

### Computational Requirements
- **Training Time**: ~2-3 hours on CPU (full optimization)
- **Hardware**: Works on standard laptop (8GB RAM)
- **GPU**: Optional but recommended for faster convergence

---

## 🤝 Contributing

This is a research project, but improvements and suggestions are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/improvement`)
3. Commit changes with clear messages
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## 👤 Authors

**Siri Sri Churakanti** (First Author)  
- MS Computer Science (Intelligent Systems)  
- Lawrence Technological University  
- 📧 schurakan@ltu.edu  
- 🔗 [LinkedIn](https://www.linkedin.com/in/siri-sri-churakanti-3487942b4/) | [GitHub](https://github.com/churakanti)

**Research Advisor:**  
Professor CJ Chung, Lawrence Technological University

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Lawrence Technological University** - Research facilities and support
- **IEEE EIT 2025 Conference** - Platform for presenting this research
- **DEAP Development Team** - Excellent evolutionary computation library
- **TensorFlow/Keras Community** - Deep learning framework and resources

---

## 📞 Contact

For questions about the research or implementation:
- **Email**: schurakan@ltu.edu
- **GitHub Issues**: [Open an issue](https://github.com/churakanti/EA_4Class_Spiral_optimizing/issues)
- **ResearchGate**: [Message on ResearchGate](https://www.researchgate.net/publication/394575077)

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

Made with ❤️ for advancing evolutionary deep learning research

</div>
```

---

#### **FILE 2: LICENSE**

Create a file called `LICENSE` and paste:
```
MIT License

Copyright (c) 2025 Siri Sri Churakanti

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

#### **FILE 3: .gitignore**

Create a file called `.gitignore` and paste:
```
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
*.egg-info/
.installed.cfg
*.egg

# Virtual Environments
env/
venv/
ENV/
env.bak/
venv.bak/

# Jupyter Notebook
.ipynb_checkpoints
*/.ipynb_checkpoints/*

# IDEs
.vscode/
.idea/
*.swp
*.swo
*~

# OS
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

# Project specific
*.h5
*.hdf5
*.pkl
*.pickle
figures/*.png
figures/*.jpg
results/temp_*