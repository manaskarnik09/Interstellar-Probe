# Interstellar Probe Trajectory Design

[![Python](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/) 
[![GMAT](https://img.shields.io/badge/GMAT-trajectory-green)](https://gmatcentral.org) 
[![PyKEP](https://img.shields.io/badge/PyKEP-lambert-orange)](https://esa.github.io/pykep/)

A mission design study for an **Interstellar Probe** using gravity assists and trajectory optimization.  
This project demonstrates advanced astrodynamics techniques, including **Lambert solvers, patched flybys, trajectory optimization with PyGMO, and GMAT**.

---

## 🌌 Problem Statement
Design a trajectory for a probe to exit the heliosphere (90–200 AU) using planetary flybys.  
Two trajectory families were explored:
1. **Earth → Jupiter** direct flyby  
2. **Earth → Venus → Jupiter** sequence
3. **Earth → Venus → Earth → Jupiter** Sequence

---

## 🛠 Tools & Methods
- **Astrodynamics libraries:** PyKEP, PyGMO, SPICE
- **Mission analysis software:** GMAT
- **Programming:** Python
- **Techniques:**  
  - Lambert solver for interplanetary transfers  
  - Jupiter flyby using patched conics approximation (turning angle, v∞ analysis, flyby periapsis radius)  
  - Delta v optimization of Earth-Venus-Jupiter trajectory using PyGMO.  
  - Validation for Lambert solver using New Horizons and PyGMO using Cassini.  

---

## 📊 Results
- **Launch:** 2045-05-08 (C3 = 90.52 km²/s²)  
- **Jupiter flyby:** 2046-12-18, turning angle = 56.72°, v∞ = 8.99 km/s  
- **Exit speed after Jupiter:** 20.12 km/s  
- **Mission durations:**  
  - 90 AU → 20.43 years  
  - 120 AU → 27.37 years  
  - 200 AU → 45.97 years  
  - **Total (Earth → 200 AU): ~45.97 years**

---

## 📂 Repository Structure
|-----PyGMO results/ # Results of delta v optimization of Earth-Venus-Jupiter trajectories
|-----notebooks/ # Jupyter notebooks with full calculations
|-----gmat_scripts/ # GMAT files for trajectory validation
|-----results/ # Plots and trajectory data
|-----requirements.txt # Dependencies for Python environment
|-----README.md # Project overview (this file)


---

## 📸 Example Plots

<p align="center">
  <img src="results/Earth-Jupiter_C3_138.png" height="300px">
  <img src="results/Earth-Jupiter_C3_133.png" height="300px">
</p>

<p align="center">
  <img src="results/Earth-Jupiter_C3_98.png" height="300px">
  <img src="results/Earth-Jupiter_C3_90.png" height="350px">
  <img src="results/Earth-Jupiter_C3_81.png" height="300px">
  <img src="results/Earth-Jupiter_C3_81.png" height="300px">
</p>

---

## 🚀 Future Work
- Complete **optimized trajectory** to the Heliopause/ISM using models  

---

## 📖 References
- Cassini Trajectory & New Horizons Validation  
- JPL Horizons Data for planetary positions  
- ESA PyKEP & GMAT documentation  

---

## 👤 Author
**Manas Karnik**  
M.Sc. Space Exploration Systems, University of Leicester (2024–2025)  
- [LinkedIn](https://www.linkedin.com/in/manaskarnik)  
- [Medium Blog](https://manaskarnik.medium.com)  
- [Email](mailto:manaskarnik09@gmail.com)

---

## 🛰 How to Run
Clone and install dependencies:
```bash
git clone https://github.com/manaskarnik09/Interstellar-Probe
cd Interstellar-Probe
pip install -r requirements.txt
