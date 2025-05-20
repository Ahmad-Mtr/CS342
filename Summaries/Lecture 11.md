### ✅ Final Exam-Oriented Summary of **CS342 Lecture 11 – Analysis of Dynamic Systems (Finite State Machines)**

This lecture introduces **Finite-State Machines (FSMs)** as tools to analyze and specify **dynamic systems**. Two case studies (Locker and Elevator) are used to illustrate FSMs in practical, real-world scenarios. This is likely to appear in your final — focus on **FSM structure, examples, transitions, and real-time challenges**.

---

## 🔹 1. **What is a Finite-State Machine (FSM)?**

- A **mathematical model** with:
    
    - A **finite number of states**
        
    - **Inputs** that cause **transitions** between those states
        
- At any moment, only **one state is active**
    
- FSMs are used for:
    
    - Computer programs
        
    - Sequential logic circuits
        

---

## 🔐 2. **Case Study 1: Locker Combination FSM**

### Scenario:

- A safe has 3 dial positions: 1, 2, 3
    
- You can turn the dial Left or Right → 6 possible inputs: 1L, 1R, 2L, 2R, 3L, 3R
    
- The **correct sequence**: `1L → 3R → 2L`
    
- Any incorrect move → **Alarm**
    

### FSM Definition:

- **States (J):** {Safe Locked, A, B, Safe Unlocked, Sound Alarm}
    
- **Inputs (K):** 1L, 1R, 2L, 2R, 3L, 3R
    
- **Initial State:** Safe Locked
    
- **Final States:** Safe Unlocked or Sound Alarm
    
- **Transition Table:** Defines how you move from one state to another based on inputs
    

---

## 🛗 3. **Case Study 2: Elevator System FSM**

### Scenario:

- Building with **M floors** and **N elevators**
    
- Control system responds to:
    
    - **Floor buttons** (Up/Down)
        
    - **Elevator buttons** (1 per floor inside each elevator)
        

---

### 🔸 Elevator Buttons (EB)

- States:
    
    - `EBON(e, f)` = ON (elevator `e`, floor `f` requested)
        
    - `EBOFF(e, f)` = OFF
        
- Events:
    
    - `EBP(e, f)` = button pressed
        
    - `EHAF(e, f)` = elevator arrived at floor `f`
        
- Transitions:
    
    1. EBOFF + Press → EBON
        
    2. EBON + Arrival → EBOFF
        

---

### 🔸 Floor Buttons (FB)

- Two per floor (Up/Down), except first/top floor
    
- States:
    
    - `FBON(d, f)`
        
    - `FBOFF(d, f)`
        
- Events:
    
    - `FBP(d, f)` = button pressed
        
    - `EHAF(1..n, f)` = elevator arrived
        
- Predicates:
    
    - `S(d, e, f)` = elevator `e` is at floor `f` moving in direction `d`
        
- Transitions:
    
    1. FBOFF + Press + No elevator at floor `f` → FBON
        
    2. FBON + Elevator arrives in correct direction → FBOFF
        

---

### 🔸 Elevator Component Sub-States

|State|Description|
|---|---|
|M(d, e, f)|Move in direction `d` to floor `f`|
|W(e, f)|Wait at floor `f` with door closed|
|S(d, e, f)|Stopped (Up, Down, or Neutral)|

**Sub-state transitions** occur based on:

- Door closing
    
- Button press
    
- Arrival at a floor
    

---

### 🔸 Elevator Event Examples:

- `DC(e, f)`: Door closed at elevator `e`, floor `f`
    
- `ST(e, f)`: Sensor triggered near floor `f`
    
- `RL`: Request logged (button pressed)
    

### Example Transition Rules:

- Elevator is stopped at floor `f`, door closed, button pressed:
    
    - Move up → `M(U, e, f+1)`
        
    - Move down → `M(D, e, f-1)`
        
    - No request → wait → `W(e, f)`
        

---

## ⚙️ 4. FSM Power & Characteristics

### ✅ Advantages:

- Easy to write, validate, convert to design/code
    
- Easy to maintain and debug
    
- More **precise** than informal or graphical models
    

### ❌ Disadvantages:

- **Timing** is not handled well (important in real-time systems)
    
- Doesn’t address **synchronization**, **race conditions**, or **deadlocks**
    

---

## ⏱️ 5. Real-Time Systems & FSM Limitations

### Real-time issues:

- **Race conditions**: Events happen at the same time
    
- **Deadlock**: System freezes due to cyclic waiting
    
- **Solution:** Use **Petri Nets** to handle concurrency and timing
    

---

## 🧠 Final Exam Focus Points:

-  Define FSM and explain its structure (states, transitions, inputs)
    
-  Solve or draw **Locker FSM** from the case study
    
-  Know how **Elevator FSM** handles button states and movements
    
-  List the **advantages/disadvantages** of FSM
    
-  Recognize **limitations of FSM in real-time systems**
    
-  Know that **Petri Nets** are the solution for real-time FSM design