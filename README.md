# CLLC-RESONANT-CONVERTER

A **CLLC resonant converter** is a bidirectional isolated DC-DC converter that uses a resonant tank made of capacitors and inductors (C–L–L–C) to achieve **high efficiency, soft switching (ZVS/ZCS)**, and wide voltage gain control. It is widely used in **EV chargers, energy storage systems, and renewable integration** because it supports both charging and discharging without manual switching.

---
### Circuit Diagram:
<img width="1840" height="867" alt="image" src="https://github.com/user-attachments/assets/fcbc98c4-9578-4c3f-81f4-449084e3ad7f" />

## 🔎 What is a CLLC Resonant Converter?

- **Structure:**  
  The resonant tank consists of two capacitors (C) and two inductors (L–L). Typically:
  - **Lp (primary inductance)**  
  - **Lm (magnetizing inductance of transformer)**  
  - **Ls (secondary inductance)**  
  - **Cp and Cs (resonant capacitors)**  

- **Operation Principle:**  
  - Works on **resonant frequency tuning**: power transfer is maximized when switching frequency matches the resonant frequency.  
  - Achieves **soft switching** (Zero Voltage Switching for MOSFETs, Zero Current Switching for diodes) → reduces switching losses.  
  - Provides **bidirectional power flow**: can step power from DC bus to battery (charging) or from battery to grid (discharging).  


### Gate Pulses 
Gate Pulses given to various MOSFET are shown below with waveforms.
<img width="1902" height="385" alt="image" src="https://github.com/user-attachments/assets/9b0b978d-5c8d-41ad-be82-3fddd3a73460" />


## ⚙️ Key Features of CLLC Resoant Converter

| Feature | Explanation |
|---------|-------------|
| **Bidirectional operation** | Supports both charging (rectifier mode) and discharging (inverter mode) |
| **High efficiency** | Soft switching reduces switching losses, ideal for EV fast charging |
| **Wide gain range** | Can regulate output voltage across varying battery SOC and grid conditions |
| **Isolation** | Transformer provides galvanic isolation between grid and battery |
| **Compact design** | High-frequency operation reduces size of passive components |



## 🔄 Modes of Operation

- **Forward Mode (Charging):** Grid/PV → DC bus → resonant tank → battery.  
- **Reverse Mode (Discharging):** Battery → resonant tank → DC bus → grid (V2G).  
- **Control:** Switching frequency modulation or phase-shift modulation is used to regulate power flow.


## 🧠 Control Considerations

- **Constant Voltage (CV) & Constant Current (CC) modes**: Used for battery charging profiles.  
- **PLL synchronization**: Needed when interfacing with grid.  
- **Digital control (DSP/FPGA)**: Implements adaptive frequency control to maintain resonance.  
- **Challenges:** Gain curve flattening at high frequency, parasitic capacitances affecting regulation.



## ⚠️ Practical Challenges

- **Design complexity:** Precise tuning of L and C values is critical.  
- **Transformer parasitics:** Can distort gain curve.  
- **Control stability:** Needs advanced algorithms (fuzzy logic, adaptive control).  
- **Cost:** Wide-bandgap devices (SiC/GaN) often required for high efficiency.

## Results
We Were Able to get the output volatge and current in DC form  and our coverter was able to provide around 26V to battery and 300mA of Current for charging of Battery(Assumed Resistor)
<img width="1888" height="393" alt="image" src="https://github.com/user-attachments/assets/967c4c3e-2800-4fae-9bdf-0b1807a1fa2c" />

✅ **In summary:**  
The **CLLC resonant converter** is a high-efficiency, bidirectional, isolated DC-DC converter ideal for EV chargers and energy storage. It leverages resonant tank design to achieve soft switching and wide voltage gain, but requires careful design of inductors/capacitors and advanced control strategies to overcome parasitic effects and maintain regulation.

#### Best Wishes & Thanks to TeamMates for Contributions <br>
##### 1.Prajwal R  <br>
##### 2.Sai Suhas Naidu N S <br>
##### 3.Sai Venkat Subba Reddy <br>
##### 4.Chethan N  <br>
##### 5.T Kowshik Rao <br>


#### Note: <br>
1. This Project was taken and implemented during NEXTEER 1.0 Hackathon at UVCE for educational Purpose and Learning. <br>
2. The proposed system is limited to unidirectional power flow, given that the bidirectional CLLC resonant converter topology was not realized in this implementation.<br>
3. This project remains in its preliminary stage, and additional contributions from other users are encouraged.
