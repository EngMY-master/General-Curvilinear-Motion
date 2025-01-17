# General-Curvilinear-Motion-Analysis

This Python script performs calculations for curvilinear motion based on user-provided functions for position, velocity, or acceleration. The program supports various cases of motion and computes critical values like velocity, acceleration, and their magnitudes.

## Theory

Curvilinear motion involves movement along a curved path. The motion can be described using:

1. **Position Functions**:
   - `x(t)` and `y(t)`: Define the object's position as a function of time.

2. **Velocity Components**:
   - `v_x = dx/dt`: The rate of change of position in the x-direction.
   - `v_y = dy/dt`: The rate of change of position in the y-direction.

   The magnitude of velocity is:
   ```
   v = sqrt(v_x^2 + v_y^2)
   ```

3. **Acceleration Components**:
   - `a_x = d(v_x)/dt`: The rate of change of velocity in the x-direction.
   - `a_y = d(v_y)/dt`: The rate of change of velocity in the y-direction.

   The magnitude of acceleration is:
   ```
   a = sqrt(a_x^2 + a_y^2)
   ```

4. **Relationships Between x and y**:
   - When position is given as `y(x)`, derivatives with respect to `x` are used to compute velocity and acceleration components.

---

## How to Use

### 1. Run the Program
Ensure you have Python installed with the following libraries:
- SymPy

Install missing dependencies using:
```bash
pip install sympy
```
Run the script in any Python environment.

### 2. Provide Inputs
Inputs are provided as dictionaries with the following keys:
- `x_func`: Position function in the x-direction as a function of time `t`.
- `y_func`: Position function in the y-direction as a function of `x` or `t`.
- `v_x_func`: Velocity function in the x-direction as a function of time `t`.
- `v_y_func`: Velocity function in the y-direction as a function of time `t`.
- `x_pos`: Specific x-coordinate value (used to compute `y` or other properties).
- `y_pos`: Specific y-coordinate value (used to compute `x` or other properties).
- `v_x` or `v_y`: Constant velocity in the respective direction.
- `t_val`: Specific time at which to evaluate results.

### 3. Follow the Test Cases
Several test cases are included in the script to demonstrate usage.

---

## Outputs
The program computes:
- Velocity components `v_x`, `v_y`.
- Acceleration components `a_x`, `a_y`.
- Magnitudes of velocity `v` and acceleration `a`.
- Derived relationships between `x` and `y` where applicable.

---

## Example Usage

### Example Input
```python
case = {
    'x_func': '8*t',
    'y_func': 'x**2/10',
    't_val': 2
}
```

### Example Output
```plaintext
--- Case 1 ---
v_x: 8
a_x: 0
x_pos: 16
y_pos: 25.6
v_y: 12.8
a_y: 0
v_magnitude: 15.231546211727817
a_magnitude: 0
```

---
