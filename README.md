# 🧬 Timetable Scheduling using Genetic Algorithm

## 📌 Overview
This project addresses the **University Timetable Scheduling Problem** using a **Genetic Algorithm (GA)**. The objective is to generate a weekly timetable for various sections and courses while satisfying all hard constraints and optimizing soft constraints.

---

## 🧠 Problem Description
The project aims to:
- Allocate courses to time slots, rooms, and professors
- Prevent clashes across professors, rooms, and sections
- Manage both lecture and lab scheduling for university sections

---

## ✅ Hard Constraints
- No double-booking: professors, rooms, or sections cannot overlap.
- Rooms must accommodate section strength: 60 (classroom) or 120 (hall).
- Professors can teach **up to 3** courses only.
- Each section may enroll in **a maximum of 5 courses**.
- Courses must have **2 lectures per week** on **non-consecutive days**.
- Labs must span **3 hours in consecutive slots**.
- Ensure **15-minute breaks** between consecutive classes.

---

## 💡 Soft Constraints
- **Theory classes** should be scheduled in the **morning**.
- **Lab classes** should be in the **afternoon**.
- Minimize the number of **floor transitions** for students and professors.
- Classes should preferably occur in the **same room** throughout the week.
- Professors may prefer **longer continuous teaching blocks** for efficiency.

---

## ⚙️ Genetic Algorithm Design
- **Chromosome Encoding**: Binary string encoding with fields like course ID, section, professor, room, day, time slot, etc.
- **Fitness Function**: Inverse of the total number of constraint violations.
- **GA Components**:
  - **Initial Population**: Randomly generated bitstrings
  - **Selection**: Tournament selection
  - **Crossover**: Single-point crossover
  - **Mutation**: Bit-flipping with probability `r_mut`
  - **Generations**: Evolve over `n_iter` iterations

---

## 📁 Project Structure
📦 Timetable-Scheduling-Genetic-Algorithm
│
├── genetic_algorithm.ipynb # Jupyter Notebook with GA implementation
├── Timetable Scheduling.pdf # Problem description
└── README.md

---

## 🛠️ How to Run
1. Install required dependencies (e.g., `numpy`, `random`)
2. Open `genetic_algorithm.ipynb` in Jupyter Notebook
3. Run the notebook step-by-step
4. Tune GA parameters like population size, mutation rate, etc.

---

## 📊 Output
- A set of binary chromosomes representing conflict-free timetables
- Timetables with reduced or zero hard constraint violations
- Can be extended to generate a human-readable weekly schedule

---

## 📚 References
- Course material from Artificial Intelligence syllabus
- Genetic Algorithm structure inspired by classical GA implementation from textbooks

---

## 👨‍💻 Author
Faizan Dar   
