### ✅ Final Exam-Oriented Summary of **CS342 Lecture 18 – Testing Workflow**

This lecture is essential for mastering **software testing** — a key phase before release and during maintenance. It covers test planning, types of testing, **test case strategies**, and especially **integration methods** like top-down and bottom-up. This material is highly likely to appear in short/long answer or MCQ formats.

---

## 🔍 1. Post-Delivery Maintenance

- **Most costly** phase in the software lifecycle.
    
- Two critical testing types:
    
    - **Change testing** (new fixes/features)
        
    - **Regression testing** (ensure nothing previously working is broken)
        

---

## 🗂️ 2. Test Planning

- Test plans must be included in the **Software Project Management Plan (SPMP)**
    
- **Test cases should be prepared** immediately after the **specifications** are done (not after coding starts)
    

---

## 🔄 3. The Test Workflow

Involves:

- **Every developer and maintainer**
    
- **QA team**
    
- Must ensure **traceability** of all tested items back to original specs
    

---

## 🧪 4. Types of Testing Cases

|Type|Description|
|---|---|
|**Random Testing**|Inefficient; may skip critical paths|
|**Test All Cases**|Impractical due to time/complexity|
|**Systematic Testing**|Preferred; targets relevant paths, balances thoroughness & cost|

---

## ⚫⚪ 5. Testing Strategies

|Type|Alias|How It Works|
|---|---|---|
|**Black-box Testing**|Test to specifications|Based on input/output behavior only|
|**White-box Testing**|Test to code|Based on internal logic and paths|

---

## 🚫 6. Limits of Exhaustive Testing

### Example:

- 5 commission types × 7 discount types = 35 combinations → manageable
    
- 20 factors × 4 values each = **4²⁰ = 1+ million years to test!** (impractical)
    

🧠 Conclusion: **Smart selection** of test cases is necessary

---

## 🔁 7. Testing to Code – Issues

- Even if **all paths** are tested, **not all faults** are caught
    
- Example: Missing a `d = 0` check causes runtime error even if all paths are run
    

🧠 You can only test **what's present in the code**, not what’s **missing or forgotten**

---

## 🔍 8. Test Case Design – Logic Flow Example

- Use logic flow diagrams to find:
    
    - Entry/exit points
        
    - Branches and loops
        
    - Paths that cover **positive/negative conditions**
        

---

## 💡 9. How to Choose Test Cases

Use **multi-level knowledge**:

|Knowledge Type|Focus|
|---|---|
|**Analysis**|Use cases, input/output (black-box)|
|**Design**|Control/data structures (white-box)|
|**Implementation**|Algorithms (e.g., division by zero)|

---

## 📘 10. Key Testing Terminology

|Term|Meaning|
|---|---|
|**Fault (Bug)**|Cause of error|
|**Error**|Incorrect internal state|
|**Failure**|Observed incorrect behavior|
|**Reliability**|Probability software works correctly over time|

---

## 🧱 11. Testing Strategies Overview

|Strategy|Description|
|---|---|
|**Unit Testing**|Each artifact in isolation|
|**Integration Testing**|Testing modules together|
|**Product Testing**|Entire system validation|

---

## 🧪 12. Stubs and Drivers

- **Stubs** = fake called functions
    
    - Used when **called module not ready**
        
- **Drivers** = fake calling functions
    
    - Used when **caller module not ready**
        

✅ Enables **testing in isolation** before full system is ready

---

## 🔁 13. Top-Down Integration Testing

|Approach|Description|
|---|---|
|**Horizontal**|Test logic layer by layer|
|**Vertical**|Test logic branches fully down to operations|

✅ **Stubs are not wasted** (replaced in-place)  
✅ **Major design faults** are caught early

---

## 🧩 14. Top-Down Integration – Challenges

- **Reusable (bottom) components** are not tested thoroughly
    
- Defensive coding may block important paths (e.g., skip invalid inputs)
    

---

## ⬇️ 15. Bottom-Up Integration Testing

|Approach|Description|
|---|---|
|**Horizontal**|Begin from low-level operational components|
|**Vertical**|Build up from operational units to logic modules|

✅ Ensures **operational artifacts are tested thoroughly**  
✅ Avoids **defensive coding hiding bugs**

---

## ⚖️ 16. Comparison & Combination Strategy

|Top-Down|Bottom-Up|
|---|---|
|Detects **design faults early**|Tests **reusable components** fully|
|Misses low-level test detail|Delays full system visibility|

✅ **Combined Testing Strategy = Best Practice**

- Logic artifacts → Top-down
    
- Operational artifacts → Bottom-up
    
- Then test **interfaces**
    

---

## 🧠 17. Object-Oriented Product Testing

- Combine **implementation + integration**
    
- Artifacts tested:
    
    - **Bottom-up** for objects
        
    - **Top-down** for non-object artifacts
        

---

## 🧠 Final Exam Focus Checklist:

✅ Difference between **unit**, **integration**, and **product testing**

✅ Understand **black-box vs. white-box testing**

✅ Explain **stubs vs. drivers** (with examples)

✅ Know **top-down vs. bottom-up** (benefits, tradeoffs)

✅ Combined strategy = top-down + bottom-up + interface testing

✅ Realize **why testing all combinations is impossible**

✅ Understand how logic flow diagrams help **test path selection**

✅ Know **error vs. fault vs. failure** differences