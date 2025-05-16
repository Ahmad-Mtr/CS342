### ✅ Final Exam-Oriented Summary of **CS342 Lecture 15 – Design Workflow**

This lecture bridges **analysis** and **implementation** by refining what you’ve learned in the analysis phase into a practical **design**. It compares **Classical vs Object-Oriented Design**, introduces **Data Flow Analysis (DFA)**, and explains **transaction-based and data-oriented design** techniques — all highly testable material.

---

## 🔹 1. What Is the Design Workflow?

- Main purpose: **Refine the analysis workflow** to prepare for implementation.
    
- Finalizes **non-functional requirements**, including:
    
    - Programming language
        
    - Reuse issues
        
    - Portability
        

### Two Major Design Types:

- **Classical Design**
    
- **Object-Oriented Design**
    

---

## 🧱 2. Classical Design

### 2 Key Phases:

- **Architectural Design**:
    
    - Divide the system into modules
        
    - Input = Specs, Output = modular structure
        
- **Detailed Design**:
    
    - Define algorithms, data structures per module
        

---

## ⚙️ 3. Object-Oriented Design

- Starts from the **OOA (Object-Oriented Analysis)** classes
    
- **Architectural Design = class-level structure**
    
- **Detailed Design = method-level design**
    

---

## 🧠 4. Operation vs Data in Design

|Design Style|Focus|
|---|---|
|**Operation-oriented**|Actions/functions first|
|**Data-oriented**|Data structures first|
|**Hybrid**|Object-Oriented Design (mix of both)|

---

## 🔄 5. Operation-Oriented Design: Data Flow Analysis (DFA)

### Key Concept:

> "Find the **point of highest abstraction** for input and output."

### Process:

1. Break product into:
    
    - **Input module**
        
    - **Transform module**
        
    - **Output module**
        
2. Refine each module until:
    
    - Each has **high cohesion**
        
    - Minimal coupling
        

---

## 🧪 6. Case Study – Word Counting Tool (like UNIX `wc`)

### Step-by-step Refinement:

- 1st Step: Read & validate filename, read file content, count words
    
- 2nd Step: Separate file name validation and word display into different modules
    
- Goal: Ensure **high cohesion** at every level
    

---

## 📋 7. Detailed Design Formats

|Format|Use|
|---|---|
|**Tabular**|Structured, visual logic|
|**PDL**|Pseudocode format (clear to programmers)|

✅ After DFA completes the module architecture, pick a detailed design format.

---

## 🔄 8. DFA Extensions (Real-World Apps)

- You may have:
    
    - Multiple input/output streams
        
- Repeat DFA for **each stream**, identifying their own abstraction points
    

---

## 💳 9. Transaction-Based Design

### What is a transaction?

- A **user-facing operation**, like “Withdraw Cash”
    

### Problem with DFA:

- Can’t handle **interconnected transaction operations** well
    
- Results in **logically cohesive modules** (bad)
    

### Example Fix (ATM Software):

- Create **generic edit & update modules**
    
- **Reuse** across 5 different transactions
    

---

## 🧱 10. Data-Oriented Design

### Principle:

> Design should follow the **structure of data**

- Related methods:
    
    - **Jackson Structured Programming**
        
    - **Warnier-Orr Design**
        

🟥 **Less popular** today due to Object-Oriented Design dominance

---

## 🧠 Final Exam Focus Checklist:

✅ **Differentiate between Classical and OO Design**

✅ **Steps of Data Flow Analysis:**

- Point of highest abstraction
    
- Input/Transform/Output decomposition
    
- Refinement until high cohesion
    

✅ **Identify poor design via logical cohesion** in DFA  
✅ **Apply transaction-based design** where DFA fails  
✅ **Recognize when to use tabular vs. pseudocode**

✅ **Understand real-world adjustments (multiple streams)**  
✅ **Explain data-oriented design's principle & decline in use**