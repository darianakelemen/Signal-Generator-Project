
# Analog Signal Generator (Triangle & Square Wave)

This project features the design and simulation of an analog signal generator developed for the **Computer Aided Design** course at the **Technical University of Cluj-Napoca**. It simultaneously produces high-integrity triangle and square waveforms with adjustable parameters.

## Technical Specifications

The circuit was designed to meet the following precise requirements:

* **Frequency Range:** Continuously adjustable from **2.6 kHz to 7.2 kHz**.


* **Triangle Wave Amplitude:** Fixed at **1 Vpp**.


* **Square Wave Amplitude:** User-selectable between **5 V and 6 V**.


* **Output Resistance ():** Fixed at **15 Ω** for both outputs.


* **Supply Voltage:** Symmetrical **±18 V** DC.



## System Architecture

The generator is built from three core functional analog blocks:

1. **Schmitt-Trigger Comparator ():** Acts as the core oscillator to generate the initial square wave.


2. **Active Integrator ():** Converts the square wave into a perfectly phase-aligned triangle wave.


3. **Power Buffers ():** High-current buffers that isolate the oscillator core, provide short-circuit protection, and enforce the 15 Ω source resistance.



## Key Design Choices

* **OPA27 Precision Op-Amps:** Selected for ultra-low noise and precision, ensuring triangle amplitude accuracy to within 1%.


* **OPA541 Power Op-Amps:** These provide up to 5A of continuous current, allowing the generator to drive low-impedance laboratory loads without distortion.


* **Frequency Control:** Implemented via a 5 kΩ multi-turn precision potentiometer () in the integrator stage.


* **Amplitude Scaling:** A resistive ladder and 1 kΩ trimmer allow fine-tuning of the internal square wave for precise hysteresis control.



## Simulation Results

Transient analysis (Time Domain) was performed to validate the design:

* **Frequency Accuracy:** Measured at **2.632 kHz** at the low end, matching the design target of 2.6 kHz.


* **Signal Integrity:** Both waveforms show minimal harmonic distortion (<2%) with crisp transitions and linear ramps.


* **Stability:** The integrator-comparator feedback loop ensures stable phase alignment, where square transitions occur exactly at triangle peaks/troughs.



## Bill of Materials (BOM)

| Component | Value/Model | Quantity | Purpose |
| --- | --- | --- | --- |

| **Op-Amp** | OPA27 | 2 | Schmitt-Trigger & Integrator 

| **Power Buffer** | OPA541 | 2 | Output Buffering & Protection 


| **Capacitor** | 22 nF | 1 | Integrator Timing () 


| **Potentiometer** | 5 kΩ | 1 | Frequency Adjustment () 

 
| **Potentiometer** | 1 kΩ | 1 | Amplitude Scaling () 

 
| **Resistors** | 15 Ω | 2 | Output Source Resistance 

 

**Total Estimated Cost:** ~43.30 €.

## Project Information

* **Author:** Kelemen Dariana-Gabriela 


* **Supervisor:** Șl. Dr. Ing. Raul Traian Fizeşan 


* **Institution:** Faculty of Electronics, Telecommunications and Information Technology, 2024 
