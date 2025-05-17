### ✅ Final Exam-Oriented Summary of **CS342 Lecture 12 – Analysis Workflow & Petri Nets**

This lecture builds directly on FSMs from Lecture 11, and focuses on modeling **real-time systems** using **Petri Nets** — a powerful tool for analyzing timing and synchronization. It also compares **formal, informal, and semiformal analysis techniques**. This material is **crucial** for understanding how to model and analyze **concurrent, event-driven systems** like elevators.

---

## 🔹 1. **Finite State Machines (FSM) Recap**

### Core structure of FSM:

```vbnet
Current State + Event + Predicate ⇒ Next State
```


|Term|Meaning|
|---|---|
|**State**|Waiting system status|
|**Transition**|What action occurs under a condition|
|**Event**|Something that happens|
|**Predicate**|Boolean check|

✅ **FSM is easy to:**

- Write, validate, design, code, maintain
    

❌ **FSM limitation:** Cannot model **timing issues** → Need Petri Nets

---

## ⏱️ 2. **Real-Time System Challenges**

### Common problems:

- **Synchronization**
    
- **Race conditions** (conflicting simultaneous actions)
    
- **Deadlocks** (system freeze)
    

📌 **Solution:** Use **Petri Nets** instead of FSM for real-time behavior.

---

## 🧠 3. **What Are Petri Nets?**

- A **graph-based formal modeling language** for distributed systems
    
- Great for modeling **events, timing, concurrency**
    

### Petri Net 4-Tuple Definition:

```mathematica
C = (P, T, I, O)
```

- `P`: Places (e.g., buttons, floors, waiting states)
    
- `T`: Transitions (e.g., move elevator)
    
- `I(t)`: Input arcs (from places to transition)
    
- `O(t)`: Output arcs (from transition to places)
    

🔴 **Tokens** are used to indicate the current state (e.g., light on, floor requested)

---

## 🧪 4. **How Petri Nets Work**

- A **"marking"** = token distribution
    
- A **transition is enabled** if:
    
    - Each **input place** has required tokens
        
    - Each **inhibitor arc** place has **no tokens**
        

### Example:

If `t1` has input: `{p2, p4}` and output: `{p1}`  
When fired: it **removes tokens** from p2 and p4 and **adds** one to p1.

---

## 🔁 5. **Petri Nets Behavior Examples**

### Marking = (1, 2, 0, 1) → 4 tokens across 4 places

#### Transition Example:

- `t1` fires → new marking = (2, 1, 0, 0)
    
- `t2` fires next → new marking = (2, 0, 2, 0)
    

---

## ⛔ 6. **Inhibitor Arc**

- Allows a transition to fire **only if a place is empty**
    
- Noted with a **small circle**, not an arrow
    
- Adds **negation logic** to the system
    

---

## 🛗 7. **Elevator Case Study with Petri Nets**

### 🔸 Elevator Button Constraint:

- Each elevator has `m` buttons
    
- Buttons light up when pressed, go off when floor is reached
    

#### Petri Net Representation:

- Place: `EBf` (Elevator Button for floor f)
    
- Token in EBf = button light ON
    

#### Sequence:

1. Button pressed → token placed in `EBf`
    
2. Elevator reaches `f` → token removed → light OFF
    

---

### 🔸 Floor Button Constraint:

- Two buttons on each floor (Up & Down)
    
- Button turns ON when pressed
    
- Turns OFF when elevator arrives **in correct direction**
    

#### Places: `FBuₓ` and `FBdₓ`

Only one light turns off depending on elevator direction.

---

### 🔸 Elevator Waiting State

- If no requests exist → elevator waits at current floor
    
- Petri Net: No transitions (e.g., "Elevator in Action") are enabled
    

---

## 📊 8. Comparison of Analysis Techniques

|Type|Description|
|---|---|
|**Formal**|Precise but hard to use (e.g., Petri Nets)|
|**Informal**|Easy but weak (e.g., English specs)|
|**Semiformal**|Balance of both (e.g., SREM, FSMs)|

---

## 💻 9. CASE Tools for Classical Analysis

Useful graphical software tools:

- Analyst/Designer
    
- System Architect
    
- Software Through Pictures
    

---

## ✅ 10. Testing & Challenges in Classical Analysis

### Testing:

- Use **specification inspection**
    
- Backed by a **fault checklist**
    

### Challenges:

- Specs must be:
    
    - **Informal enough** for clients
        
    - **Formal enough** for developers
        
- Important to keep analysis and design **separate**:
    
    - Analysis = "What"
        
    - Design = "How"
        

---

## 🧠 Final Exam Focus Checklist:

-  Petri Net definition & components: (P, T, I, O)
    
-  Token behavior and transition enabling
    
-  Elevator button & floor button modeled using places/tokens
    
-  Differences between FSM vs Petri Nets
    
-  Use cases of inhibitor arcs and marking vectors
    
-  Choose suitable analysis methods (formal, informal, etc.)
    
-  Know strengths/limitations of each approach