# 🚗 Occupant-Adaptive Airbag Deployment System (OAADS)

### Intelligent Occupant Monitoring and Adaptive Airbag Control

**OAADS** is an automotive safety project that explores how airbags can respond more intelligently to the person sitting inside a vehicle.

Traditional airbag systems are designed around predefined deployment strategies. However, occupants differ in body size, weight, posture, and seating position. These differences can affect how an occupant interacts with an airbag during a collision.

The goal of OAADS is to develop an occupant-aware safety system that analyses relevant occupant characteristics and uses this information to determine an appropriate airbag deployment strategy.

The project combines **embedded systems, sensor-based monitoring, AI-assisted perception, MATLAB, and Simulink** to explore adaptive restraint control through system modelling and simulation.

> **Project vision:** Every occupant is different. Vehicle safety systems should account for those differences.

---

## 🎯 Problem Statement

An airbag must provide protection during a collision, but its deployment can also pose a risk when an occupant is seated too close to the airbag, leans forward, or has other unusual seating characteristics.

A fixed deployment strategy may not adequately account for every occupant and seating condition.

OAADS explores a more adaptive approach by considering occupant-related inputs before determining an appropriate deployment stage.

The central question behind this project is:

**Can an airbag control system use occupant characteristics and sensor information to make more informed deployment decisions?**

---

## 💡 Proposed Solution

OAADS follows an occupant-aware approach that combines sensing, perception, decision-making, and deployment control.

The proposed system considers three main sensing categories:

- **Mass and pressure sensing:** To estimate occupant loading and seating-related characteristics.
- **Camera-based perception:** To analyse occupant presence, posture, and seating position using AI-based techniques.
- **Distance sensing:** To estimate the occupant's distance from the airbag deployment area.

These inputs can be processed by an embedded controller and used by the control logic to select a suitable deployment strategy under defined conditions.

MATLAB and Simulink support the modelling and simulation of the decision-making and control behaviour.

*Note: The complete sensor integration, AI perception, and physical airbag actuation represent the proposed system architecture; their implementation status depends on the corresponding source code and hardware available in the repository.*

---

## ⚙️ How the System Works

The proposed workflow is divided into four stages.

### 1. Sensing

The system collects information related to occupant loading, seating pressure, presence, and position using the selected sensors.

### 2. Occupant Perception

Camera-based processing is intended to identify the occupant's presence and seating posture, while distance sensing provides additional information about the occupant's position relative to the airbag.

### 3. Decision and Risk Assessment

The controller evaluates the available inputs against predefined conditions and determines the appropriate control response. The decision logic is designed to consider occupant characteristics rather than relying only on a single fixed input.

### 4. Adaptive Deployment Control

The selected deployment command can be represented and evaluated through the control model. A physical implementation would require validated restraint hardware and a safety-engineered deployment controller.

---

## 🧠 System Architecture

```text
       OCCUPANT IN THE VEHICLE
                  |
                  v
          SENSOR INPUTS
     +------------+-------------+
     |            |             |
     v            v             v
 Mass Sensor  Pressure Sensor  Camera
                                |
                         AI-Based Perception

     Distance Sensing / Occupant Position
                  |
                  v
        EMBEDDED CONTROLLER
               ESP32
                  |
                  v
       OCCUPANT-RELATED ANALYSIS
                  |
                  v
       ADAPTIVE CONTROL LOGIC
                  |
                  v
       MATLAB / SIMULINK MODEL
                  |
                  v
     DEPLOYMENT-STAGE DECISION
                  |
                  v
     RESTRAINT SYSTEM INTERFACE
```

This diagram represents the **proposed system architecture**, not a claim that all components are already connected or operational.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| MATLAB | Algorithm development, analysis, and simulation support |
| Simulink | Modelling and simulation of the control system |
| ESP32 | Proposed embedded controller for sensor processing and control |
| Mass sensor | Occupant loading estimation |
| Pressure sensor | Seating pressure measurement |
| Camera and AI-based perception | Proposed occupant presence and posture analysis |
| Distance sensor | Occupant-to-airbag distance estimation |
| Embedded C/C++ | Potential implementation of embedded control logic |

The exact software dependencies and hardware components may vary with the implementation available in the repository.

---

## 📂 Repository Contents

The repository includes the project files used to document and develop OAADS.

```text
OAADS/
│
├── README.md
│
├── MATLAB/
│   └── MATLAB source files (.m)
│
├── Simulink/
│   └── Simulink model files (.slx)
│
├── Simulation_Results/
│   └── Output plots and simulation screenshots
│
├── Documentation/
│   └── Project proposal and technical documentation
│
└── Hardware/
    └── Circuit diagrams and implementation files
```

*The directory structure above is a suggested organization. Update it to match the actual files committed to GitHub.*

### MATLAB Source Code

The MATLAB files contain the relevant scripts for the implemented calculations, input processing, control logic, or simulation analysis. Each script should be documented with its purpose and required inputs.

### Simulink Model

The Simulink model represents the system's control flow and allows the modelled behaviour to be evaluated using defined input conditions. The exact functionality depends on the blocks, subsystems, and signals implemented in the supplied model.

### Simulation Results

This folder can contain plots, scope outputs, and screenshots showing how the implemented model responds to different test inputs.

---

## 🧪 Testing and Validation

Simulation is an important part of this project because it allows the proposed control behaviour to be examined without deploying a physical airbag.

Useful test scenarios include:

- Different occupant loading and seating-pressure values.
- Changes in occupant-to-airbag distance.
- Different posture or seating-position conditions, where supported by the implemented perception logic.
- Normal operating conditions and sensor-input boundary cases.
- Missing, invalid, or inconsistent sensor data.
- Controller response under different combinations of input values.

The model's outputs should be recorded and compared against predefined expected behaviour.

**Validation status:** Results should be documented from the actual MATLAB scripts and Simulink simulations. Performance figures, classification accuracy, response times, and injury-reduction claims should only be included when supported by reproducible tests and appropriate evidence.

---

## 🚧 Current Scope and Limitations

OAADS is an engineering project exploring occupant-aware restraint control. Its scope must be distinguished from a production-ready automotive airbag system.

- Sensor integration and calibration require further verification.
- Camera-based occupant classification requires representative test data and accuracy evaluation.
- Deployment decisions require carefully defined operating limits and fault-handling behaviour.
- Simulation results alone cannot establish real-world occupant protection or crashworthiness.
- A physical airbag deployment system requires dedicated restraint hardware, extensive crash testing, and applicable automotive safety validation.

The system should therefore be treated as a research and development project, not as a certified airbag controller.

---

## 🔭 Future Enhancements

The project can be extended in several directions:

1. **Sensor Integration:** Connect the mass, pressure, and distance sensors to the embedded controller.
2. **AI-Based Occupant Analysis:** Develop and evaluate posture and occupant-position detection.
3. **Simulink Integration:** Connect measured or generated sensor inputs to the control model.
4. **Fault Detection:** Define safe responses for missing, noisy, or implausible sensor data.
5. **Hardware-in-the-Loop Testing:** Evaluate controller behaviour using suitable test equipment before considering physical deployment.
6. **Performance Evaluation:** Measure decision latency, input sensitivity, repeatability, and behaviour across defined test scenarios.

---

## 🎓 Project Information

**Project:** Occupant-Adaptive Airbag Deployment System (OAADS)  
**Domain:** Automotive Safety, Embedded Systems, and Intelligent Restraint Control  
**Development Tools:** MATLAB and Simulink  
**Academic Institution:** Presidency University, Bengaluru  
**Project Context:** Automotive safety project proposal and system development

---

## 🤝 Contributions and Feedback

Suggestions, technical discussions, and improvements related to embedded control, sensor integration, simulation, and automotive safety are welcome.

If you are interested in this project, feel free to explore the available source files, review the model, and share constructive feedback.

---

## ⚠️ Disclaimer

OAADS is an educational and research-oriented project. It is not a certified automotive restraint system and must not be used to control a real vehicle airbag or to make safety-critical deployment decisions. Any physical implementation would require independent engineering review, validated hardware, and comprehensive safety testing.

**Smarter sensing. Better-informed decisions. Safer restraint-system design.**
