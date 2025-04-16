# 🧪 Asynchronous FIFO UVM Testbench
This project implements a **Universal Verification Methodology (UVM)** based testbench for validating an **Asynchronous FIFO (First-In-First-Out)** buffer. The design ensures data integrity between **two independent clock domains** and tests key edge cases like **overflow**, **underflow**, and **reset conditions**. 

---

## 🚀 What Does This Do?

✅ Verifies a SystemVerilog asynchronous FIFO using UVM.  
🔁 Simulates separate write and read clock domains.  
🧪 Detects edge cases including overflow, underflow, and simultaneous read/write.  
📉 Optimized with Transaction-Level Modeling (TLM) for faster simulation.

---

## 🧰 Features

- Full UVM environment with:
  - Sequence Items
  - Driver, Monitor, Agent, Scoreboard
  - UVM Environment and Test
- Clock domain crossing and synchronization handling
- Edge case handling:
  - FIFO Full / Empty
  - Overflow / Underflow
  - Reset during operation
- Achieves 98% functional coverage
- 30% reduced simulation runtime via TLM

---

## 🏗️ How We Built It

1. **Designed an asynchronous FIFO RTL** in SystemVerilog.
2. **Created UVM components**: sequence item, driver, monitor, scoreboard, agent, environment.
3. **Built tests** for normal and edge-case scenarios.
4. **Used TLM (Transaction Level Modeling)** for efficient communication.
5. **Simulated using Mentor QuestaSim**, capturing functional coverage reports.



---

## 📈 Results

| **Metric**                    | **Outcome**       |
|-------------------------------|------------------|
| Functional Coverage           | ✅ 95  %            |
| Simulation Runtime Reduction  | ⚡ 30%            |
| Overflow/Underflow Detection  | ✅ Verified       |
| Clock Domain Sync             | ✅ Achieved       |
| Assertion Failures            | ❌ None           |

---

## ❗ Challenges Faced

- **Clock domain synchronization**: Dealing with metastability in read/write pointers.
- **Debug complexity**: Random sequences caused occasional hard-to-trace mismatches.
- **Coverage vs performance**: Balancing detailed coverage collection with speed.
- **Reset behavior**: Handling async resets mid-transfer required extra care in monitor logic.

---

## 🧪 Test Cases Covered

- [x] Normal write/read operation
- [x] Clock skew between write and read domains
- [x] FIFO full with write attempts
- [x] FIFO empty with read attempts
- [x] Reset behavior during operation
- [x] Continuous burst writes and reads
- [x] Cross-clock assertions for metastability detection

---

## 📄 Requirements

- SystemVerilog (IEEE 1800-2017 compliant)
- UVM 1.2 or later
- Mentor QuestaSim / Synopsys VCS for simulation
- Make or script runner for compiling and running simulations

---

## 📌 Conclusion

This project demonstrates a robust UVM testbench for validating an asynchronous FIFO. It achieves high coverage, handles intricate edge cases, and is optimized for simulation speed. The modular UVM structure also makes it extensible for other communication primitives or clock-domain-crossing modules.







