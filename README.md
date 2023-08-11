# Model of Enrollment 🎓 📊

A detailed model to understand and predict student enrollment for postgraduate programs based on various factors. Dive in to explore how different parameters affect the enrollment decisions of students!

---

## 🌟 Overview

We're aiming to craft a mathematical model that's rooted in real-world conditions but also accounts for hypothetical scenarios, providing a comprehensive understanding of the enrollment landscape.

---

## 🎯 Preconditions:
- 🪑 100 slots available for the master's program.
- 💰 15 of those slots are funded (budgeted).

---

## 🤔 Assumptions:
- 🎓 The number of students applying for the master's program is estimated to be between 1/3 and 1/4 of those who obtain a bachelor's degree.
- 📈 Predominantly, those who were in the upper part of the ranking will enroll in the master's program. Expected ratio is approximately 80/20.

---

## 🎯 Target:
- 🖥️ To create a mathematical model for the enrollment of the IT Software Development stream, which can be later verified.

---

## 📜 Parameters (Hypothetically Based):
- 📌 Initially, we will consider the model as a linear combination of elementary functions.
- ➡️ We will transition to more complex variants later.

---

## 🛠 Model:

### 1. Desire to Join Masters 🎓❤️:
Let the "desire" to join the master's be represented as:
    $$w=\sum_{i\in S} \log{f(i)}$$

Where `f(i)` denotes the success metric in the i-th semester.

> If `w` ≤ 0, the student does not go to the master's.

### 2. Group Equalization Coefficient 🧮:
Given the uneven distribution of groups, we introduce an equalization coefficient. For instance, groups 5-10 have a weight of c = 0.9 during enrollment.

### 3. Average Rating Position 🌟:
Extract insights from historical data to compute an average ranking position:
    
$$P = \sum_{i\in S}\frac{S[i]}{|S|}$$

### 4. Average Grade Calculation 📚:
Determine the student's average grade:
    
$$X = \sum_{i\in S}\frac{R[i]}{|S|}$$

> Note: S represents the set of semesters.

### 5. Success Metric 🏆:
Defining success:
    
$$J = e^{\frac{f(i)}{X}}$$

### 6. Random Variable 🎲:
Capture the student's enrollment uncertainty:
    
$$ u=-tR\pi e^{\pi}, 0 \le R \le 1 $$

### 7. Foreign University Enrollment Temptation ✈️:
Higher grades might tempt students to enroll abroad:
    
$$ M = -\frac{2^{\frac{X}{tP}}}{P} $$

---

## 📝 Resulting Equation:

$$A = w u + J + M$$

Here, `A` represents the final enrollment decision based on all the factors discussed above.

---

