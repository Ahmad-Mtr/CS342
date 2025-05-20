### ✅ Final Exam-Oriented Summary of **CS342 Lecture 13 – Object-Oriented Analysis (OOA)**

This lecture is essential for understanding **Object-Oriented Analysis (OOA)** using UML, scenarios, class diagrams, and CRC cards. It uses the **elevator case study** as a running example and shows the **evolution from centralized to distributed control systems**. For the final exam, you must understand **class types, modeling steps, and architectural patterns**.

---

## 🔹 1. What Is Object-Oriented Analysis (OOA)?

- **Semiformal technique** used in modern software development
    
- Focuses on identifying:
    
    - **Entity Classes** (long-lived data)
        
    - **Boundary Classes** (I/O interface)
        
    - **Control Classes** (logic & coordination)
        

🧩 Used within the **Unified Process**, combined with:

- Use Cases
    
- UML Diagrams
    
- CRC Cards
    

---

## 🔍 2. Elevator Case Study Overview

### Use Cases:

1. Pressing Elevator Button
    
2. Pressing Floor Button
    

### Functional Modeling → Use Case Scenarios:

- Each **scenario** = specific instance of a use case
    
- Helps understand the required system behavior
    

---

## 🧱 3. Step-by-Step Class Extraction

### **Step 1: Functional Modeling**

- Identify use cases & scenarios
    

### **Step 2: Entity Class Modeling**

- Extract classes and their attributes using:
    
    - **Noun Extraction**
        
    - **CRC (Class Responsibility Collaboration) Cards**
        

**Example nouns:**

- Valid classes: `Elevator`, `Button`
    
- Subclasses: `Elevator Button`, `Floor Button`
    
- Excluded nouns: `building`, `floor`, `door` (if outside the system)
    

### **Step 3: Dynamic Modeling (UML Statechart)**

- Define class behavior over time
    
- Transitions triggered by events and conditions
    

---

## 📘 4. UML Class Diagram Iterations

### **Iteration 1:**

- Basic button and elevator class
    
- ❌ Problem: No communication → fix needed
    

### **Iteration 2:**

- Introduce **Elevator Controller Class**
    
- All relationships become **1-to-n**
    

### **Iteration 3:**

- Add stateful elements (e.g., Elevator Doors Class)
    
- Better info hiding and responsibility distribution
    

---

## 🧩 5. CRC Cards (Class Responsibility Collaboration)

### CRC Structure:

- **Class Name**
    
- **Responsibilities** (What it does)
    
- **Collaborations** (Who it interacts with)
    

### CRC Weakness:

- Requires **domain knowledge**
    
- Helps identify **missing classes or overloaded control**
    

---

## ⚙️ 6. Design Pitfalls & Fixes

### Problem:

- **Elevator Controller** was doing too much (centralized design)
    
    - Violates **information hiding**
        
    - Harder to scale and maintain
        

### Fix:

➡️ **Decentralized Architecture**

- Each **Elevator** has its **own sub-controller**
    
- Each **Floor** has its **own sub-controller**
    
- **Scheduler** handles coordination among sub-controllers
    

---

## 🧠 7. Dynamic Modeling – UML Statechart

- Models how objects **change state** over time
    
- Includes:
    
    - **States** (e.g., Moving, Waiting)
        
    - **Events** (e.g., Button Pressed)
        
    - **Predicates** (e.g., Door Closed?)
        

### Final Statechart Output:

- Reflects communication between elevator buttons, sub-controllers, and sensors
    

---

## 🧭 Final Class Diagram – Iteration 4

- Includes:
    
    - Sub-controllers for elevators and floors
        
    - Dedicated classes for:
        
        - Buttons
            
        - Doors
            
        - Sensors
            
        - Scheduler
            

### Benefits:

- Modular
    
- Scalable
    
- Clean separation of responsibilities
    

---

## 🧠 Final Exam Checklist:

✅ **Know the 3 class types:**

- Entity, Boundary, Control (with examples)
    

✅ **Understand modeling process:**

- Functional → Class Diagram → Dynamic Modeling
    

✅ **Be able to apply noun extraction** to extract classes from a paragraph

✅ **Draw or interpret CRC cards**

✅ **Understand architectural differences:**

- Centralized controller vs. Distributed sub-controllers
    

✅ **Understand how UML statecharts work**

✅ **Be ready to update class diagrams across iterations**