# 🧩 Knowledge-Based Product Configuration Using MiniZinc

## 📌 Project Overview
This project implements a **knowledge-based configuration (KBC) system** using **MiniZinc**.  
The goal is to create a model where **product knowledge, rules, and constraints** are explicitly encoded, allowing the solver to:
- Generate **valid product configurations**
- Automatically **reject incompatible choices**
- Optionally **optimize configurations** (e.g., minimize cost)

This approach is commonly used in **mass customization**, **complex product configuration**, and **decision-support systems**.

---

## 🗂 Repository Structure
```
├── part1/
│   └── specification.pdf        # Requirements and formal knowledge model design
├── part3/
│   ├── kb_model.mzn             # Knowledge-based configuration model (MiniZinc)
│   ├── kb_data.dzn              # Knowledge base data (components, options)
│   └── kb_test.mzp              # MiniZinc project file (optional)
├── report.pdf                   # Final report describing modeling approach
```

---

## 🧠 Knowledge Representation
The knowledge base encodes:
- **Components & options** (e.g., CPU, GPU, RAM, Storage)
- **Compatibility constraints** (e.g., certain CPUs require specific motherboards)
- **Business rules** (e.g., at least one storage device must be selected)
- **Optional objective function** (e.g., minimize total cost)

---

## 🔧 Key Features
- **Declarative modeling**: The entire system is expressed as constraints, not procedural code
- **Automated reasoning**: Solver finds **all valid configurations** or optimal ones
- **Modular knowledge base**: Easy to extend with new components or rules
- **Feasibility checking**: Prevents invalid product setups

---

## 🛠 How to Run Locally

### 1. Install MiniZinc
Download and install MiniZinc from [https://www.minizinc.org/](https://www.minizinc.org/).

### 2. Open the Project
- Open `kb_model.mzn` in the MiniZinc IDE
- Load the data file `kb_data.dzn` (Tools → Set Data File)

### 3. Run the Solver
- Select a solver (e.g., Gecode, Chuffed)
- Click **Run** to generate valid configurations
- View solutions in the output pane (multiple solutions possible)

---

## 📊 Example Output
Example solution for a laptop configuration:
```
cpu = "Intel i7";
ram = "16GB";
storage = "512GB SSD";
gpu = "NVIDIA GTX 1650";
valid = true;
----------
==========
```

---

## 📦 Tools Used
- **MiniZinc** – knowledge-based modeling language
- **Gecode / Chuffed** – solvers for CSP/optimization
- **Formal Knowledge Representation** – for product rules & constraints

---

## 🚀 Future Improvements
- Extend the knowledge base with **cost attributes** and solve for **optimal (minimum cost) configuration**
- Support **multiple solution exploration** with user preference ranking
- Build a **front-end configurator** (e.g., with Python + Streamlit or a simple CLI)

---

## 📜 License
This project is licensed under the MIT License – see [LICENSE](LICENSE) for details.

---

## 👤 Author
**Mahmudul Hasan**  
Master’s in Business Analytics – TU Graz  
[LinkedIn](https://www.linkedin.com/) | [GitHub](https://github.com/Mahmudul-Hasan-24)
