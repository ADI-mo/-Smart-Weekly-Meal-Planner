
# Smart Weekly Meal Planner

**A Smart System for Weekly Meal Planning, Pantry Management, and Cost Optimization**

---

## 1. Background and Motivation
Daily meal planning is repetitive and time-consuming, often leading to food waste and higher costs.  
The challenge is even greater when considering additional constraints such as:

- **Dietary and religious laws:** (Kosher – separation between meat and dairy)
- **Dietary preferences:** (Vegetarian / Vegan)
- **Limited preparation time:** Adapting to a busy lifestyle.
- **Efficient use of inventory:** Utilizing existing pantry items to reduce waste.

Most existing solutions address only one aspect (recipes, shopping, or nutrition) rather than providing an integrated, automated, personalized solution. This project aims to fill that gap.

---

## 2. Project Objectives
This project develops a Python-based system that:

- **Automatically generates** a balanced weekly meal plan.
- **Respects dietary and religious constraints** (Kosher).
- **Adapts to user lifestyle** (Time, Budget, Participants).
- **Utilizes existing pantry inventory** when available to prevent over-buying.
- **Produces an optimized shopping list** with estimated costs based on real-world data.

---

## 3. User Configuration and Personalization
Users can dynamically adjust multiple parameters to see how they affect the weekly menu and shopping list:

### 🥩 Kosher Rules
- Enable or disable Kosher validation.
- Ensure meat and dairy are never combined in the same meal.
- Allow meat and dairy on the same day in separate meals.

### 🥗 Dietary Preferences
- **Standard / Vegetarian / Vegan.**
- Recipes not matching the selected preference are automatically excluded.

### ⏱️ Preparation Time
- Set maximum preparation time per meal.
- Balance simple and complex meals across the week.

### 💰 Estimated Budget & Data Sync
- Calculates total cost using official **Central Bureau of Statistics (CBS)** data.
- **Auto-Update:** The system can check for the latest government price datasets upon execution.

### 👥 Number of Participants
- Automatically scales ingredient quantities and shopping lists.
- Directly affects the total cost estimation.

---

## 4. System Overview
The system runs as an automated multi-stage pipeline:

1. **Load Data:** Import recipes, pantry inventory, and price data.
2. **Classification:** Automatically categorize recipes (Main / Side / One-Pot) using keyword heuristics.
3. **Filtering:** Apply user constraints (Kosher, Time, Vegan, etc.).
4. **Generation:** Build a balanced weekly menu.
5. **Optimization:** Compare required ingredients vs. pantry stock (Quantity-based).
6. **Output:** Generate `weekly_menu.txt`, `shopping_list.txt`, and `cost_estimate.txt`.

---

## 5. Out-of-the-Box Functionality
The system **does not require manual user input** to function.  
A default recipe dataset is provided at: `data/recipes.json`.

This allows immediate execution and full feature demonstration. Adding personal recipes or detailed pantry inventory is **optional**, providing value for advanced users without being a barrier for new ones.

---

## 6. System Architecture
The system is modular, following the **Separation of Concerns** principle:

* **Data Layer:** JSON and CSV files (recipes, pantry, price data).
* **Business Logic Layer:** Classification, menu generation, Kosher validation, and cost calculation.
* **Presentation Layer:** User-friendly **GUI** (built with Tkinter/PyQt) and a **CLI** for automation.

---

## 7. Installation and Dependencies

### Requirements
- Python 3.9 or higher
- Internet connection (Optional, for real-time price updates)

### Install Dependencies
```bash
pip install -r requirements.txt

```

**Required Libraries:**

* `pandas`: For CSV and data processing.
* `requests`: To fetch official CBS datasets.
* `python-dateutil`: For date handling and validation.
* `Tkinter`: (Usually pre-installed) for the Graphical User Interface.

---

## 8. Required vs. Optional Components

| Component | Required | Optional | Notes |
| --- | --- | --- | --- |
| Default recipe dataset | ✅ | ❌ | Provided with the project |
| Adding personal recipes | ❌ | ✅ | User customization |
| Kosher rules | ❌ | ✅ | Enabled/Disabled via settings |
| Dietary preferences | ❌ | ✅ | Standard / Vegetarian / Vegan |
| Price estimation | ❌ | ✅ | Requires price data from CBS |
| Pantry Inventory | ❌ | ✅ | Supports quantity-based subtraction |
| GUI | ❌ | ✅ | User-friendly visual interface |

---

## 9. Innovation and Value

* **Integration with official, real-world price data (CBS).**
* **Non-trivial dietary logic:** Handling Kosher meal separation automatically.
* **Graceful handling of incomplete data:** Works with or without a pantry file.
* **Automated Lifecycle:** From meal planning to shopping and budgeting in one click.

---

## 10. Conclusion

Smart Weekly Meal Planner demonstrates systematic thinking, modular design, and practical automation. It bridges the gap between digital recipe management and real-world kitchen logistics.

*Developed as part of the [COURSE NAME] course at [UNIVERSITY NAME].*

```

---

### מה השלב הבא?
כדי שהפרויקט יהיה מוכן ב-100%, כדאי לייצר את הקבצים הבאים בתיקיית ה-`data` שלך:
1.  **`recipes.json`**: המאגר ההתחלתי.
2.  **`inventory.json`**: דוגמה למזווה (אפשר להשאיר ריק `{}` כברירת מחדל).
3.  **`prices.csv`**: קובץ מחירים ראשוני.


```
