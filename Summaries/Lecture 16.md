### ✅ Final Exam-Oriented Summary of **CS342 Lecture 16 – Object-Oriented Design (OOD)**

This final lecture wraps up the **design workflow** by focusing on **Object-Oriented Design (OOD)**. It connects class diagrams from OOA (Lecture 13–14) to real-world implementation using **method assignments, design architecture, and subsystems**. This is a **must-know** for the exam if you're asked how designs turn into code or how to handle real-time systems.

---

## 🔹 1. Purpose of Object-Oriented Design (OOD)

> “Design the product in terms of the classes extracted during OOA.”

### OOD Has 2 Steps:

1. **Complete the class diagram**
    
    - Define attribute formats (e.g., dates, text, numbers)
        
    - Assign each **method** to the right class
        
2. **Perform detailed design**
    
    - Define logic using **pseudocode or tables**
        

---

## 🔧 2. Completing the Class Diagram

### a) **Attribute Formatting**

- Use format info from OOA artifacts (e.g., date = "dd/mm/yyyy")
    
- Don't overload diagrams too early — only add attributes when needed.
    

### b) **Method Assignment Principles**

1. **Information hiding** – Keep internal details private
    
2. **Responsibility-driven design** – Give methods to the class responsible
    
3. **Reusability** – If many classes use an operation, assign it to the object
    

---

## 🛗 3. Example – Elevator System

- Each **class** (e.g., Elevator Subcontroller) has **methods** like `elevatorEventLoop`
    
- Represent detailed logic with:
    
    - **Pseudocode (PDL)**
        
    - **Tabular format**
        

---

## 📚 4. MSG Case Study – Object-Oriented Design

### Architectural Design:

- Add support classes like **Date**
    
- Complete attribute & method assignment
    

### Example:

- `getAssetNumber()` → belongs to `Asset Class`  
    (since both `Investment` and `Mortgage` inherit it)
    

### Detailed Design:

- Write each method’s logic clearly using **PDL**
    

---

## 📦 5. Subsystems & Packages Design

### Why break into subsystems?

- Easier implementation
    
- Enables **parallel development**
    
- Reduces delays
    

### A subsystem = manageable part of a big system

---

## 🧱 6. Software Architecture

> “The overall structure of components and how they fit together.”

- **Designed by software architect**
    
- Includes:
    
    - Component allocation
        
    - Subsystem responsibilities
        
    - Interface behavior
        

---

## ⚖️ 7. Architecture Trade-Offs

The architect must balance:

|Requirement Type|Examples|
|---|---|
|**Functional**|Use cases|
|**Non-Functional**|Portability, reliability, security|

🧠 If all can't be satisfied:

- Either **relax requirements**, **increase budget**, or **extend deadline**
    

📌 **A bad architecture = total redesign. You can’t “fix” it later.**

---

## 🧪 8. Testing the Design

- **Design Reviews**:
    
    - Check if specs are reflected accurately
        
    - Ensure logical correctness
        

---

## 📐 9. Formal Techniques (for High-Quality Design)

Used to:

- Prove correctness of modules
    
- Reduce fault rate
    
- Help programmers develop positive attitude toward design
    

---

## ⏱️ 10. Real-Time Design Techniques

### Challenges:

- Timing is unpredictable (inputs come from real-world)
    
- Often distributed = **communication/synchronization issues**
    

### Key Goals:

- Ensure **timing constraints** are met
    
- Handle **race conditions** and **delays**
    

🧠 Most real-time design methods extend **normal OOD**, but with extra constraints.

---

## 🧰 11. CASE Tools for Design

|Tool Type|Examples|
|---|---|
|**Commercial**|Rational Rose, Software Through Pictures|
|**Open Source**|ArgoUML|

Helps ensure **analysis artifacts** are carried into design.

---

## 📏 12. Design Metrics

Metrics help measure design quality:

- **Cohesion** – Each class/module has one clear responsibility
    
- **Coupling** – Modules should be loosely connected
    
- **Fault Statistics** – Track problems across modules
    

---

## ❗ 13. Design Limitations

Designers must find the **balance**:

- Don’t write full code in design phase
    
- But don’t leave it too vague for implementers
    

✅ A complete **detailed design** makes implementation faster & more accurate

---

## 👨‍💻 14. Growing Design Professionals

To develop expert designers:

- **Identify talent**
    
- Provide **formal education**
    
- Allow **collaboration and mentorship**
    

---

## 🧠 Final Exam Focus Checklist:

✅ Difference between **analysis class diagram** and **design class diagram**

✅ Method assignment rules (info hiding, responsibility)

✅ MSG method example: why `getAssetNumber()` belongs in parent class

✅ Tabular & pseudocode representation

✅ Subsystems: purpose, advantage, and architecture definition

✅ Trade-offs in architecture: what to do if budget/time is tight

✅ Real-time system challenges

✅ Design metrics: cohesion, coupling, faults

✅ CASE tools that support UML (name a few!)