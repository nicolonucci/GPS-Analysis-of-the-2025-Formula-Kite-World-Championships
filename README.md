# GPS-Analysis-of-the-2025-Formula-Kite-World-Championships
Advanced data analysis and visualization of Formula Kite GPS telemetry. The project reconstructs race dynamics and compares elite athletes using metrics such as Speed Over Ground, VMG, start acceleration, and tacking efficiency.

This repository contains the complete analysis pipeline used to perform a GPS-based performance analysis of the first upwind leg at the 2025 Formula Kite World Championships.

The project focuses on a comparative analysis between two elite athletes, Riccardo Pianosi and Maximilian Maeder, using raw GPS telemetry data and official race timing information.

All figures and tables in the final report are generated directly from the analysis notebook contained in this repository.

---

## Repository Structure

- `GPS Analysis of the 2025 Formula Kite World Championships.ipynb`  
  Jupyter Notebook containing the full analysis pipeline.

- `Folder with all files to run the pipeline`  
  Raw GPS tracks of the athletes and Formula Kite Men FINAL.xlsx

- `Analysis report`  

---

## How to Run the Analysis

### 1. Download the repository

Download the repository as a ZIP file or clone it locally.  
Make sure to keep the folder structure unchanged.

---

### 2. Update local directories in the notebook

Before running the notebook, you must update **two directory paths**:
- the directory_p containing Pianosi GPX files
- the directory_m containing Maeder GPX files

These paths are **clearly marked inside the notebook** with comments indicating that they must be modified.

---

### 3. Execute the notebook

Open the notebook and run all cells sequentially from top to bottom.

No web access, APIs, or external services are required.

---

## Using the Code for a Different Regatta

The analysis pipeline is reusable for other Formula Kite regattas.  
To analyze a different event, the following elements must be updated:

- **Input data**
  - Replace the GPX files with the tracks of the new athletes

- **Racecourse parameters**
  - Update the geometric parameters defining the racecourse (start line, marks, finish line)
  - Update wind direction and reference points if needed

- **Tack identification**
  - Tacking maneuvers must be identified for the new race
  - Manual tack timestamps must be updated accordingly

All sections of the code that may require manual modification are explicitly highlighted inside the notebook.

---

## Reproducibility

The analysis is fully deterministic:
- all computations are based on explicit analytical formulas
- no random components are used
- no machine learning models are involved

Given the same input files and the same manually identified tack timestamps, the results can be reproduced exactly.

---

## Data Sources and Usage

The GPS data used in this project were obtained from the public tracking platform **metasail.it**.

This project is intended for **non-commercial, academic use only**.  
Raw data are not redistributed beyond this repository.

---

## Requirements

The analysis is implemented in Python and relies on standard scientific libraries, including:
- `numpy`
- `matplotlib`
- `gpxpy`
- `datetime`

Any standard Python environment supporting these libraries is sufficient.

---

## Author

**Nicolò Nucci**  
University of Milano–Bicocca  
Academic Year 2025/2026
