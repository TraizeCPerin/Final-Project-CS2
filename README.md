# 📌 Project Proposal (Draft)

## 📝 Project Title 
Kinematics Calculator

---

## 🔍 Problem Statement  
When manually calculating motion, it can end up being prone to errors and time consuming. This project uses the kinematics.json dataset to compute for efficiently. This makes calculating motion faster, easier, and more understandable than manually doing the work

---

## 🎯 Project Objectives  
 1. Apply the kinematic equations of motion in a program. Like solving for the acceleration, velocity, and more.
 2. To design a code that can solve problems that involves kinematics

---

## ⚙️ Planned Features  
- Feature 1: Find the maximum height
- Feature 2: Compute the total horizontal distance covered
- Feature 3: find displacement
- Feature 4: find final position
- Feature 5: compute for the time


---

## ⌨️ Planned Inputs and Outputs  

- **Inputs** 
  - Scenario ID
  - x0 (initial x-position)
  - y0 (initial y-position)
  - v0 (initial velocity)
  - angle_deg
  - g (acceleration due to gravity)
    
- **Outputs**  
  - average velocity
  - acceleration due to gravity
  - maximum height reeached
  - total horizontal range
  - comparison results (which projectile traveled farther/higher)

## 🧠 Logic Plan  
Pseudocode: 
1. Load the projectile data from a JSON file or JSON variable.
2. For each scenario in the data, display the scenario data.
3. Read the time, x and y position and display the projectile’s position over time.
4. End the program when all scenarios are handled, or when the user exits.
