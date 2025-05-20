### ✅ Final Exam-Oriented Summary of **CS342 Lecture 10 – Structured Systems Analysis**

This lecture is **very important for your final exam** and focuses on **analyzing and refining requirements** using structured methods like **DFDs** and **stepwise decomposition**. Below is your clear, focused, and informative summary.

---

## 🔍 1. **Purpose of the Analysis Workflow**

- Refines and formalizes the **requirements gathered earlier**.
    
- Cannot be part of the requirements workflow because:
    
    - Requirements use **natural language** (understandable by the client)
        
    - Analysis must use **precise technical language** for developers
        

---

## 📝 2. **Why Informal Specifications Fail**

- Example in English: "If sales drop below target..." → This can be **ambiguous**.
    
- Ambiguity arises from:
    
    - Vague terms (e.g., “optimal”)
        
    - Unclear subjects (e.g., "it" refers to what?)
        
- Solution: Split into two workflows:
    
    - **Requirements:** Natural language (client-oriented)
        
    - **Analysis:** Precise, structured (developer-oriented)
        

---

## 🔗 3. **Traceability**

- Every item in the **analysis** must be **linked back to a requirement**.
    
- Ensures nothing important is missed or invented out of thin air.
    

---

## 📄 4. **Specifications Document**

- Acts as a **contract** between the client and developers.
    
- Must be:
    
    - Clear and unambiguous
        
    - Complete, testable, and maintainable
        
- Includes constraints: deadlines, portability, reliability, real-time constraints.
    

---

## 🧠 5. **Structured Analysis Methods**

Three methods from the 1970s (still useful today):

- **DeMarco**
    
- **Yourdon**
    
- **Gane & Sarson** (most commonly used)
    

---

## 🏪 6. **Software Shop Case Study**

The shop:

- Buys/sells software (keeps popular stock, orders rare ones)
    
- Gives discounts to educational institutions (10% for ≤4 packages, 15% for ≥5)
    

### **Case Study Objective**

> “Computerize the business to make more money.”

Requires:

- **Cost–benefit analysis** for every department (accounts, inventory, etc.)
    
- **Risk Management:** Avoid building a solution without understanding the problem
    

---

## 🔁 7. **Structured DFD Development (9-Step Process)**

### **Step 1:** Create a DFD

- Start with **high-level** processes and **refine** gradually.
    
- Use symbols:
    
    - Process (rounded rectangle)
        
    - Data store (open rectangle)
        
    - External entity (square)
        
    - Data flow (arrow)
        

### **Step 2:** Decide what to computerize

- **Batch processing:** Large volume, strict controls
    
- **Online processing:** Small volume, instant updates
    

### **Step 3:** Define data flows

- Break each flow into smaller items (e.g., order = order_id + customer + items)
    
- Create a **data dictionary** for larger systems
    

### **Step 4:** Define process logic

- E.g., use a **decision tree** to model discount logic:
    
    - ≤4 packages → 10%
        
    - ≥5 packages → 15%
        

### **Step 5:** Define data stores

- What data needs to be stored and how it will be accessed (by name, function, etc.)
    

### **Step 6:** Define physical resources

- Files: name, type (indexed, sequential), medium
    
- Storage: hard drive, cloud, etc.
    

### **Step 7:** Input/Output specs

- Design:
    
    - Input forms
        
    - Input screens
        
    - Output reports/displays
        

### **Step 8:** Estimate project size

- Data volume per hour/day/month
    
- File sizes and processing frequency
    

### **Step 9:** Determine hardware needs

- CPU, memory, I/O channels
    
- Can only be **roughly estimated**
    

---

## 💡 Final Notes on Software Shop Case

- You **can’t precisely determine** response time or hardware specs at this stage.
    
- Still, no other method provides **more structured data** early in development.
    

---

## 🧪 Bonus: DFD Case Study Example – MSG Foundation

Appears briefly to **link the use of DFDs** with real-world requirements handling.

---

### ✅ Final Exam Focus Checklist:

-  Can you explain **why analysis and requirements must be separated**?
    
-  Can you describe a **DFD** and use **correct symbols**?
    
-  Can you apply the **9-step structured analysis process** to a case study?
    
-  Can you spot why informal specs lead to ambiguity?
    
-  Can you trace a requirement through analysis and design artifacts?