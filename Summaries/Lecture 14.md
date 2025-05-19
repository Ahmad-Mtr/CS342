### ✅ Final Exam-Oriented Summary of **CS342 Lecture 14 – Object-Oriented Analysis (MSG Case Study & Interaction Diagrams)**

This lecture **continues from Lecture 13**, focusing on completing the Object-Oriented Analysis (OOA) using the **MSG Foundation** case study. The key additions here include **dynamic modeling using statecharts**, **interaction diagrams (collaboration & sequence)**, and **class diagram realization**. These concepts are **likely to appear on the final exam**, so this summary will target what's most test-relevant.

---

## 🔹 1. **Dynamic Modeling – Step 3 of OOA**

- Construct a **UML statechart** from all system **operations**.
    
- Each **event** (user action) triggers **transitions** between system states.
    

### MSG System – Event Options:

1. Estimate funds for the week
    
2. Manage an asset
    
3. Update annual expenses
    
4. Produce report
    
5. Quit
    

🎯 **Goal:** Capture the system's behavior over time in response to events.

---

## 🖥️ 2. GUI & Boundary Classes

- Each **input/output/report screen** = 1 boundary class
    
- Initial boundary classes for MSG:
    
    - User Interface Class
        
    - Estimated Funds Report Class
        

---

## ⚙️ 3. Control & Entity Classes in MSG

- **Control Class** (logic-heavy):
    
    - `Estimate Funds for Week Class`
        
- **Entity Classes** (data storage):
    
    - `Mortgage Class`
        
    - `Investment Class`
        
    - `MSG Application Class`
        

---

## 🧱 4. Initial Class Diagram – MSG System

|Class Type|Description|
|---|---|
|**Boundary**|User Interface & Report classes|
|**Control**|Estimate Funds logic class|
|**Entity**|Mortgage, Investment, Application (data classes)|

---

## ❌ 5. Class Diagram Limitation

A class diagram:

- Only shows **class structure** and **relationships**
    
- Does NOT show:
    
    - Actual objects during runtime
        
    - Order of message exchanges
        

✅ **Solution → Interaction Diagrams**

---

## 🔄 6. Interaction Diagrams

### 1. **Collaboration Diagram**

- Shows:
    
    - **Objects** involved in a scenario
        
    - **Messages exchanged** between them
        
    - Numbered **order** of message flow
        

📝 Must be accompanied by a **written flow-of-events description**  
📉 **Disadvantage:** Can be cluttered and harder to follow for clients.

---

### 2. **Sequence Diagram**

- Shows:
    
    - **Objects**
        
    - **Messages**
        
    - **Timeline (vertical axis)**
        

✅ **Best for understanding communication order**  
✅ Preferred when **info transfer** clarity is the goal.

---

## 📊 7. Comparison – Sequence vs. Collaboration

|Diagram Type|When to Use|
|---|---|
|**Sequence**|Focus on **message order**|
|**Collaboration**|Focus on **class responsibilities**|

Both represent the same use-case scenario.

---

## 🧬 8. Class Diagram Realization

- Update the class diagram after analyzing **use-case interactions**
    
- Realized class diagram shows:
    
    - Updated **relationships**
        
    - Dependencies from **dynamic behavior**
        

---

## 🧰 9. CASE Tools for OOA (Support UML)

|Tool Type|Examples|
|---|---|
|Commercial|IBM Rational Rose, Together|
|Open Source|ArgoUML|

---

## ⚠️ 10. Challenges of OOA

- Avoid slipping into **Object-Oriented Design**
    
    - Don’t assign methods yet
        
- Only focus on **what the system should do**, not how
    

---

## 📏 11. Metrics in OOA

Track these for planning and estimation:

- **Size** (e.g., pages of UML diagrams)
    
- **Cost, effort, duration**
    
- **Quality**
    

---

## 🧠 Final Exam Focus Points:

✅ **Statechart:**

- Start state, end state, rounded rectangles = operations
    
- Arrows = transitions from GUI events
    

✅ **Boundary, Control, Entity class examples**

✅ **Interaction diagrams:**

- **Collaboration** = messages with object layout
    
- **Sequence** = message timeline view
    

✅ **Class Diagram Realization:**

- How dynamic behavior leads to structural changes
    

✅ **Difference between diagrams** (use table above)

✅ **Tools** (CASE tools supporting UML)

✅ **OOA scope vs. Design scope** — keep them separate!