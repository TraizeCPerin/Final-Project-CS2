# 📌 Project Proposal (Draft)

## 📝 Project Title 
Kinematics Calculator

---

## 🔍 Problem Statement  
Many students struggle with projectile motion because it involves multiple calculations for height, distance, speed, and time, which can be confusing and time-consuming. For example, predicting how far a basketball will travel when thrown at different angles, how high a soccer ball will rise, or how a javelin moves in a sports event can be difficult without a clear method. Comparing multiple projectiles to see which goes the farthest or highest adds even more complexity.

This problem is important because understanding projectile motion is a key part of learning physics and applying it in real-life situations like sports, engineering, and ballistics. Using a dataset of projectile scenarios stored in a JSON file, this project provides a tool that quickly calculates and compares motion parameters. It helps students visualize results, make connections between math and real-world motion, and explore physics in an interactive way.

---


## 🎯 Project Objectives  
- 1. To calculate and display key motion parameters (maximum height, total range, average velocity) for different projectiles so students can easily see how speed and angle affect motion.
- 2. To compare multiple projectile scenarios from the JSON dataset, helping users identify which projectile travels the farthest or reaches the highest point.
- 3. To visualize projectile positions over time using the sample data, making abstract physics concepts more understandable and relatable.
- 4. To provide a user-friendly tool that reduces tedious manual calculations, making learning physics faster and more interactive.
  

---
## ⚙️ Planned Features  
- Feature 1: Display the initial conditions of each projectile (v₀, angle, g, etc.).
- Feature 2: Display the projectile’s position over time using the sample data in the JSON file.
- Feature 3: Compute maximum height using the initial vertical velocity.
- Feature 4: Compute total horizontal range until the projectile lands.
- Feature 5: Compute average velocity (using displacement/time).
- Feature 6: Compare scenarios to determine which projectile travels the highest and which goes the farthest.
- Feature 7: Allow multiple feature selections per scenario without restarting the program.
- Feature 8: Handle invalid scenario IDs or feature inputs.


---

## ⌨️ Planned Inputs and Outputs  

- **Inputs** 
  - 1. Scenario ID
       - the user chooses which projectile to analyze (1, 2, or 3)

  - 2. Feature choice
       - the user chooses what calculation to view
      (e.g., max height, range, average velocity, comparison, etc.)
    
- **Outputs**  
  - 1. Initial conditions of the scenario
  - 2. Position data over time (x,y)
  - 3. Maximum height of the projectile.
  - 4. Total horizontal range
  - 5. Average velocity
  - 6. Comparison results
       -  which projectile traveled farther
       -  which reached the highest point

## 🧠 Logic Plan  
Pseudocode: 
START

INITIALIZE Firebase connection
SET database reference to /projectiles

FUNCTION max_height(v0, angle, g)
    COMPUTE using formula
    RETURN result

FUNCTION horizontal_range(v0, angle, g)
    COMPUTE using formula
    RETURN result

FUNCTION average_velocity(v0, angle, g)
    COMPUTE time of flight
    COMPUTE displacement
    RETURN displacement / time

LOOP main menu
    DISPLAY options:
        1 Display Scenarios
        2 Add Scenario
        3 Update Scenario
        4 Delete Scenario
        5 Features
        6 Exit

    INPUT choice

    IF choice = 1
        RETRIEVE all scenarios from Firebase
        DISPLAY scenario data

    ELSE IF choice = 2
        INPUT v0, angle, g
        COMPUTE max height, range, avg velocity
        SAVE to Firebase

    ELSE IF choice = 3
        INPUT scenario ID
        IF exists
            UPDATE values
            RECOMPUTE results
            SAVE changes
        ELSE
            SHOW "not found"

    ELSE IF choice = 4
        INPUT scenario ID
        IF exists
            DELETE from Firebase
        ELSE
            SHOW "not found"

    ELSE IF choice = 5
        OPEN feature menu
            - Compare scenarios
            - View full scenario

    ELSE IF choice = 6
        EXIT program

END LOOP

END
