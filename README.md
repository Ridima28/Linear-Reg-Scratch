# Linear Regression from Scratch using NumPy

A complete implementation of **Linear Regression** from scratch using only **NumPy**, without relying on machine learning libraries such as scikit-learn. This project demonstrates multiple approaches to solving linear regression and highlights how increasing vectorization significantly improves computational efficiency.

## 🚀 Project Overview

This repository implements Linear Regression in **four different ways**:

1. **Normal Equation (Analytical Solution)**
2. **Gradient Descent using 3 Loops**
3. **Gradient Descent using 2 Loops (Vectorized over Samples)**
4. **Gradient Descent using 1 Loop (Fully Vectorized)**

The primary objective of this project is to understand the mathematical foundations of Linear Regression while exploring how vectorization in NumPy leads to cleaner and faster implementations.

---

## 📚 Implementations

### 1. Normal Equation

Uses the closed-form solution to directly compute the optimal parameters without any iterative optimization.

**Formula**

$$w = (X^T X)^{-1} X^T y$$

**Advantages**

* No learning rate required
* Finds the exact optimal solution
* Very fast for small datasets

**Limitations**

* Computationally expensive for large feature sets
* Requires matrix inversion

---

### 2. Gradient Descent (3 Loops)

The most basic implementation where every computation is performed manually.

**Loop Structure**

* Outer loop → Epochs
* Middle loop → Training samples
* Inner loop → Features

This implementation closely follows the mathematical derivation of gradient descent and is ideal for understanding the algorithm step by step.

---

### 3. Gradient Descent (2 Loops)

Improves efficiency by vectorizing computations across all features while still iterating through each training sample.

**Loop Structure**

* Outer loop → Epochs
* Inner loop → Samples

This approach reduces computational overhead while maintaining readability.

---

### 4. Gradient Descent (1 Loop - Fully Vectorized)

The most optimized implementation using NumPy matrix operations.

**Loop Structure**

* Only one loop over epochs

All predictions, error calculations, gradients, and parameter updates are computed simultaneously using matrix multiplication.

This implementation closely resembles how modern machine learning libraries internally optimize numerical computations.

---

## 🛠 Technologies Used

* Python
* NumPy



---

## 🎯 Learning Outcomes

Through this project, I learned:

* Mathematical intuition behind Linear Regression
* Mean Squared Error (MSE) Loss
* Gradient computation from scratch
* Gradient Descent optimization
* Matrix multiplication using NumPy
* Vectorization techniques
* Performance improvements by reducing nested loops
* Writing efficient numerical code using NumPy

---

## 📈 Comparison

| Method           | Optimization         | Number of Loops | Speed |
| ---------------- | -------------------- | --------------- | ----- |
| Normal Equation  | Closed-form          | 0               | ⭐⭐⭐⭐  |
| Gradient Descent | Manual               | 3               | ⭐     |
| Gradient Descent | Partially Vectorized | 2               | ⭐⭐    |
| Gradient Descent | Fully Vectorized     | 1               | ⭐⭐⭐⭐  |

---

## 💡 Key Takeaway

This project demonstrates that the same Linear Regression algorithm can be implemented in multiple ways. By progressively replacing explicit loops with NumPy's vectorized operations, the code becomes significantly faster, more concise, and closer to the implementations used in modern machine learning frameworks.


## 📜 License

This project is open-source and available under the MIT License.
