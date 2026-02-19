# AI Overview - Read Below

<img width="964" height="909" alt="Screenshot 2026-02-19 175514" src="https://github.com/user-attachments/assets/8c6605f1-7999-4e22-8540-4d0e907629e1" />


This project includes **three AI implementations**, each driven by its own Behavior Tree.

---

## 1️⃣ Farmer – First Version

The first Farmer implementation is fully functional, but the logic is verbose and relies on workarounds to integrate the EQS system properly.

- Uses workaround-based EQS handling  
- Logic is less optimized  
- Disabled by default in the scene  

To test it:
- Assign `AIPC_Farmer` to the corresponding character.

⚠️ Note: Due to its search radius, it may detect objects belonging to the second Farmer. Testing this version is therefore not recommended.

---

## 2️⃣ Farmer – Improved Version

The second Farmer is the refined and production-ready implementation.

Improvements include:

- Cleaner and more maintainable logic  
- Proper use of **EQS queries (Use of custom EQS asset)**  
- Custom **Decorators** to handle logic flow more efficiently  
- No reliance on workarounds  

This version can also fill the entire farming field without causing the Behavior Tree to break.

To stress-test it:
- Increase the **Growth Time** value inside `BP_PlantEnhanced`.

---

## 3️⃣ Turret

The turret implements a simple logic system, as required.

In the scene:
- The purple cube represents an enemy.
- It continuously lerps back and forth to demonstrate turret targeting behavior.

No multi-enemy logic was implemented, as it was not part of the requirements.
