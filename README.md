# 🧺 Smart Washing Machine FSM (Verilog)

### 📌 Project Overview
This project implements a **Smart Automated Washing Machine** using a **Finite State Machine (FSM)** in Verilog. The washing machine follows real-world steps: checking the door, filling water, adding detergent, washing, draining, and spinning clothes. Each step is modeled as a separate state, and transitions occur only when required conditions are satisfied.

---

### ⚡ Features
- FSM with **6 states**: `Check Door`, `Fill Water`, `Add Detergent`, `Cycle`, `Drain Water`, `Spin`.
- **Safety checks**: Ensures door must be closed before operation.
- **Soak and rinse cycles**: Supports soap wash followed by clean water rinse.
- Control signals for **motor, water inlet valve, and drain valve**.
- Final **done signal** when cycle completes.
- Includes **Verilog Testbench** for simulation and verification.

---

### 🛠️ FSM States
1. **Check Door** – Wait until door is closed and machine started.  
2. **Fill Water** – Fills the drum with water (soap wash first, then water wash for rinse).  
3. **Add Detergent** – Waits for detergent addition.  
4. **Cycle** – Washing operation (motor turns on).  
5. **Drain Water** – Empties water after cycle.  
6. **Spin** – Spins clothes for drying and completes the cycle.  

---

### 📊 FSM Diagram
<img width="1317" height="705" alt="fsm_1" src="https://github.com/user-attachments/assets/167deff6-ce90-43cd-8914-97a4d37870fa" />

---

<img width="1287" height="740" alt="fsm_2" src="https://github.com/user-attachments/assets/2e80198b-59e9-4e3e-aac9-f8abfcd1955d" />


---


### ▶️ Simulation
- Testbench initializes inputs and simulates different states.  
- `$monitor` displays transitions in the console.  
- Example log (simplified):
```
Time=15, start=1, door_close=1 → State: Fill Water
Time=25, filled=1 → State: Add Detergent
Time=35, detergent_added=1 → State: Cycle
Time=45, cycle_timeout=1 → State: Drain Water
Time=55, drained=1 → State: Spin
Time=65, spin_timeout=1 → Cycle Done 
```

---

### 🔑 Applications
- Demonstration of **FSM modeling in digital systems**.  
- Practical **Verilog design** for real-life appliances.  
- Can be extended for **smart washing machines** with sensors/IoT.  

