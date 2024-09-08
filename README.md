
# Multiphase Flow Separation Simulation in Horizontal Pipes

This project simulates the distribution of oil, water, and emulsion layers inside a horizontal pipe, calculates flow parameters, and models slip velocity between water and oil phases. It provides a graphical user interface (GUI) using `Tkinter` to interact with the simulation.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Code Structure](#code-structure)
6. [Key Concepts](#key-concepts)
7. [Future Improvements](#future-improvements)

---

## 1. Project Overview
This project models **multiphase fluid flow separation** in horizontal pipes, where oil, water, and emulsion coexist. The simulation calculates:
- Layer thicknesses for oil, water, and emulsion.
- Flow parameters such as mixture velocity and pipe area.
- Slip velocity between oil and water phases.
The program uses a GUI interface for user interaction.

---

## 2. Features
- **Water Fraction Calculation:** Models water contamination in oil, emulsion, and water layers across a pipe's cross-section.
- **Layer Thickness Optimization:** Uses Newton-Raphson method to find the optimal thicknesses for oil and water layers based on user input.
- **Slip Velocity Calculation:** Computes the relative velocity of water droplets moving through oil based on fluid properties.
- **Flow Parameters Calculation:** Determines important flow properties such as mixture velocity and pipe area.
- **Graphical User Interface (GUI):** A user-friendly interface to interact with the simulation.

---

## 3. Installation

### Prerequisites
- Python 3.x
- The following Python libraries:
  - `numpy`
  - `matplotlib`
  - `math`
  - `tkinter`

### Steps
1. Clone this repository:
    ```bash
    git clone https://github.com/hamidras000/MPPS-design.git
    ```
2. Navigate to the project folder:
    ```bash
    cd pipe-flow-simulation
    ```
3. Install dependencies:
    ```bash
    pip install numpy matplotlib
    ```
4. Run the simulation:
    ```bash
    python main.py
    ```

---

## 4. Usage

### Running the Program
- After installation, you can run the program using the Python command.
- Upon starting, the GUI will display, and you can interact with the action button to perform specific calculations.

### Adjusting Parameters
- The simulation includes default parameters like:
  - Pipe diameter
  - Oil, water, and emulsion contamination
  - Flow rates
- These parameters can be adjusted directly in the code for more custom simulations.

---

## 5. Code Structure
### Key Functions

#### 1. `calculate_water_fraction`:
Calculates the fraction of water at each height inside the pipe, considering the thicknesses of oil, emulsion, and water layers.

#### 2. `find_layer_thicknesses`:
Uses the Newton-Raphson method to optimize the oil and water layer thicknesses, ensuring that the calculated water fraction matches the target water cut.

#### 3. `calculate_flow_parameters`:
Computes key flow parameters like mixture velocity, pipe area, and volumetric flow rate.

#### 4. `calculate_slip_velocity`:
Calculates the relative velocity (slip velocity) between water droplets and the surrounding oil based on their densities, viscosities, and droplet size.

#### 5. `calculate_water_layer_thickness`:
Determines the thickness of the water layer along the length of the pipe as it develops during the flow.

#### 6. `Tkinter GUI`:
Provides a graphical user interface to display an image and allow interaction with the simulation.

### Files
- `main.py`: The main script that runs the simulation.
- `utils.py`: Contains utility functions used throughout the project.
- `README.md`: The file you're reading now.

---

## 6. Key Concepts
- **Multiphase Flow:** Refers to the simultaneous flow of different phases (oil, water, and emulsion) in a pipeline.
- **Slip Velocity:** The relative velocity between dispersed water droplets and the continuous oil phase.
- **Water Cut:** The fraction of water in the mixture, crucial in oil and gas industries for managing the efficiency of extraction and transportation.

---

## 7. Future Improvements
- Implement more interactive GUI features to allow users to input their own parameters directly.
- Add visualization of the fluid layers and velocity profiles inside the pipe.
- Include more detailed error handling and validation of inputs.
