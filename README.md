# Digital Logic & CPU Architecture Lab: D Flip-Flop & XOR Integration

A hands-on step-by-step experiment exploring sequential logic, memory elements, and state preservation using the **Digital** logic simulator.

---

## Circuit Architecture Overview

This project bridges combinational logic (gates like XOR) with sequential logic (memory storage elements like D Flip-Flop), mimicking how a CPU manages register states and instruction cycles.

### Components Used:
1. **Inputs (Toggles / Switches):** Represent raw data bits (`0` or `1`), acting like variables in low-level programming.
2. **XOR Gate:** Performs a logical operation on input data before it reaches the storage stage.
3. **Control Switch:** Acts as a gatekeeper to allow or block data flow to the input pin (`D`).
4. **Clock Signal (`C`):** The timing heartbeat of the circuit. It determines *when* data is officially captured and stored (akin to a CPU clock cycle).
5. **D Flip-Flop:** The core memory cell. It holds 1 bit of data stable.
   - **`D` (Data Input):** The staging area where incoming data waits.
   - **`C` (Clock Input):** The trigger that loads data from `D` into memory.
   - **`Q` (Output):** The stored value currently held inside the memory cell.
   - **$\overline{Q}$ (Inverse Output):** The logical negation of the stored value.
6. **Digital Output (LED):** Visual indicator of the current state of `Q`.

---

## How It Works (Low-Level Concept)

* **Combinational Stage (XOR):** Computes the result dynamically based on current inputs.
* **Staging Phase (`D`):** The computed value sits at the `D` port. *Note: Data at `D` does not affect the output yet; it is merely waiting at the door.*
* **Storage Trigger (`Clock`):** When a clock tick/pulse occurs, the D Flip-Flop captures the value at `D` and locks it into `Q`. 
* **State Preservation:** Once stored in `Q`, the value remains stable and persistent, ignoring subsequent changes at `D` until the *next* clock pulse arrives.

---

## Step-by-Step Construction Guide

1. **Place the D Flip-Flop:** Drop a standard D-Flip-Flop component onto your workspace.
2. **Setup the Clock:** Place a **Clock** component and connect its output to the clock pin (`C`) on the Flip-Flop (marked with a clock triangle symbol).
3. **Add Logic Inputs:** 
   - Place input switches and feed them into an **XOR gate**.
   - Connect the output of the XOR gate through a control switch to the **`D`** pin of the Flip-Flop.
4. **Connect the Output:** 
   - Connect an **LED** (Digital Output) to the **`Q`** terminal (the primary top output of the Flip-Flop) to monitor the saved state.
5. **Run and Test:**
   - Turn on the simulation.
   - Change your input switches and close the control switch so data reaches the `D` pin.
   - Click the **Clock** component to issue a pulse and watch the LED update and stabilize according to the stored state!
