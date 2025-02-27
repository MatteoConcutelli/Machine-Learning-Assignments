# Machine Learning Projects  
*Robot Kinematics & Autonomous Car Racing*  
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.12-orange)](https://www.tensorflow.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0-red)](https://pytorch.org/)

---

## 🦾 Project 1: Robot Kinematics Learning  
*Forward/Inverse Kinematics with ML*  
[[Report]](/Robot Kinematics/HW1_RobotKinematic.pdf) [[Code]](robot_kinematics/)

### Key Features
- Solved FK for 2DOF/3DOF/5DOF robots using 3 distinct approaches:
  - **RBF Kernel + Linear Regression** (2DOF)
  - **Gradient Boosting** (3DOF)
  - **Deep Neural Network** (5DOF)
- Jacobian matrix analysis (Frobenius norm = 2.995 vs analytical)
- Hyperparameter optimization with grid search

### Performance Summary
| DOF | Model                | Position Error | Orientation Error |
|-----|----------------------|----------------|-------------------|
| 2   | RBF + Linear Reg     | 1.78e⁻⁷ MSE    | 1.69e⁻⁶ MSE       |
| 3   | Gradient Boosting    | 6.11e⁻⁵ MSE    | 0.29 MSE          |
| 5   | Neural Network       | 0.0088 MAE     | 0.588°            |

---

## 🏎️ Project 2: Autonomous Car Racing  
*Image-to-Action Classification*  
[[Report]](HW2_CarRacing.pdf) [[Code]](car_racing/)

### Key Features
- 5-class CNN for racing control:
  - Input: 96x96x3 RGB images
  - Output: Steering/gas/brake actions
- Action space modeling:
  ```python
  ACTIONS = {
      0: 'No action',
      1: 'Steer left',
      2: 'Steer right', 
      3: 'Accelerate',
      4: 'Brake'
  }
