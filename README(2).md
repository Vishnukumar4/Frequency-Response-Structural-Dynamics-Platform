# Frequency Response Structural Dynamics Platform

A student-built simulation platform for **frequency response analysis, modal analysis, and structural dynamics modeling** using **MATLAB, Python, FORTRAN-style numerical solvers, and FEA concepts**.

This project was designed to understand how mechanical and structural systems respond to harmonic excitation across a frequency range. It combines matrix-based structural dynamics, modal analysis, frequency response functions, vibro-acoustic interpretation, and automated post-processing.

---

## Project Title

**Frequency Response Structural Dynamics Platform**  
**MATLAB | Python | FORTRAN | FEA Concepts | Vibro-Acoustics | SEA Concepts**

---

## Project Summary

This project implements a simulation workflow for predicting the dynamic response of structural systems under frequency-domain excitation.

The platform supports:

- Modal analysis
- Frequency response function calculation
- Harmonic response simulation
- Damping comparison
- Resonance peak identification
- Vibro-acoustic interpretation
- SEA-based high-frequency response concepts
- Automated result processing and documentation

The goal was to create a clear academic simulation project that demonstrates both engineering theory and practical numerical implementation.

---

## Motivation

Structures used in aerospace, automotive, mechanical systems, acoustic enclosures, and electronic hardware are often exposed to vibration and sound. Their response depends strongly on natural frequencies, mode shapes, damping, and excitation frequency.

This project was created to answer questions such as:

- What are the natural frequencies of a structure?
- Which mode shapes dominate the response?
- At what frequency does resonance occur?
- How does damping reduce vibration amplitude?
- How can FEA mass and stiffness matrices be used for dynamic simulation?
- How can structural vibration be connected to vibro-acoustic behavior?

---

## Repository Structure

```text
Frequency-Response-Structural-Dynamics-Platform/
|
|-- README.md
|-- README_01_theory_and_background.md
|-- README_02_implementation_pipeline.md
|-- README_03_simulation_cases.md
|-- README_04_results_validation.md
|-- README_05_student_experience.md
|
|-- src/
|   |-- matlab/
|   |   |-- modal_analysis.m
|   |   |-- frequency_response.m
|   |   |-- damping_model.m
|   |   |-- plot_frf.m
|   |
|   |-- python/
|   |   |-- run_batch_simulation.py
|   |   |-- postprocess_results.py
|   |   |-- generate_plots.py
|   |   |-- report_generator.py
|   |
|   |-- fortran/
|       |-- numerical_solver_reference.f90
|
|-- input/
|   |-- mass_matrix.csv
|   |-- stiffness_matrix.csv
|   |-- damping_matrix.csv
|   |-- excitation_config.json
|
|-- results/
|   |-- modal_frequencies.csv
|   |-- frequency_response.csv
|   |-- resonance_summary.csv
|   |-- damping_comparison.csv
|
|-- figures/
|   |-- mode_shape_1.png
|   |-- frequency_response_plot.png
|   |-- damping_comparison.png
|
|-- docs/
    |-- theory_notes.md
    |-- simulation_methodology.md
    |-- validation_report.md
```

---

## Main Workflow

```text
Define structural model
        |
        v
Assemble or import mass, stiffness, and damping matrices
        |
        v
Apply boundary conditions
        |
        v
Solve modal eigenvalue problem
        |
        v
Extract natural frequencies and mode shapes
        |
        v
Run frequency response simulation
        |
        v
Post-process displacement, velocity, and acceleration
        |
        v
Identify resonance peaks and damping effects
        |
        v
Generate plots, tables, and documentation
```

---

## Technologies Used

| Tool | Purpose |
|---|---|
| MATLAB | Modal analysis, matrix solving, FRF plotting |
| Python | Automation, post-processing, batch simulation, report generation |
| FORTRAN | Numerical solver reference and high-performance computation style |
| FEA Concepts | Mass, stiffness, damping, boundary conditions, modal dynamics |
| Vibro-Acoustics | Sound radiation and transmission interpretation |
| SEA Concepts | High-frequency energy flow interpretation |

---

## Quick Start

### MATLAB

```matlab
run('src/matlab/modal_analysis.m')
run('src/matlab/frequency_response.m')
```

### Python

```bash
python src/python/run_batch_simulation.py
python src/python/postprocess_results.py
```

---

## Output Files

The project generates:

- Natural frequency tables
- Mode shape plots
- Frequency response curves
- Resonance peak summaries
- Damping comparison plots
- Validation tables
- Technical report notes

---

## Resume Version

**Frequency Response Structural Dynamics Platform — MATLAB, Python, FORTRAN, FEA Concepts**

Developed MATLAB and Python-based frequency response and modal analysis simulation platform using FEA structural dynamics concepts. Applied vibro-acoustic and SEA concepts for frequency-domain response interpretation, automated structural dynamics post-processing using Python and FORTRAN-style solver workflows, validated dynamic response against analytical results, and documented findings through technical reports and plots.
