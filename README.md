# Robot-to-convert-food-warehouse-into-automated-warehouse
*Robot Arm Working Envelope – Execution Algorithm*

## Project: Mechanical Task – Robot Arm Zones

---

### Definitions of Zones and Colors:

- **Operation Zone**:
- **Color**: Green
- **Description**: Represents the maximum area where the robotic arm is allowed to move.
- **dimension**: 200 units

- **Working Zone**:
- **Color**: Orange
- **Description**: Represents the safe and effective area for the arm to operate.
- **Radius dimension**: 106 units

- **Dead Zone**:
- **Color**: Red
- **Description**: Represents a restricted inner area near the center that the arm must not enter due to safety and collision concerns.
- **Radius dimension**: 50 units

- **Arm Length**: 46 units (Maximum reach of the arm)

---

## Task Objective

The goal of this task is to define the robot arm’s movement zones inside the warehouse and apply an execution algorithm to ensure the arm operates within the safe boundaries.

---

## Execution Algorithm (Plain Steps)

1. Calculate the distance from the center to the target point using the formula:
`distance = √(x² + y²)`

2. If the distance is greater than 200:
- Output: "Target is outside the operation zone"
- Stop the operation

3. If the distance is less than 50:
- Output: "Target is inside the dead zone – movement not allowed"
- Stop the operation

4. If the distance is greater than 106:
- Output: "Target is outside the working zone"
- Stop the operation

5. If the distance is greater than 46:
- Output: "Target is out of reach – the arm cannot reach this position"
- Stop the operation

6. If none of the above apply:
- Move the arm to the target (x, y)
- Output: "Movement successful to the target position"

---

## Final Note

A 3D model was included using Tinkercad to visually demonstrate the different motion zones:
- Green area (Operation Zone)
- Orange area (Working Zone)
- Red area (Dead Zone)

This model helps visualize the boundaries and ensure correct implementation.
