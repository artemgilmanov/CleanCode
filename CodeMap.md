# Code Map

A **Code Map** is literally a map of your project code. It helps visualize the structure and dependencies in your solution, making it easier to understand complex projects.

> **Note:** Code Map is available only in **Visual Studio Enterprise Edition**. When installing, make sure to include the **Code Map** component.

---

### How to open a Code Map

In your solution, right-click on the **Solution** in Solution Explorer and select:
**Show on Code Map**

---

### What you see

You’ll get a schematic map showing the projects in your solution as blocks:

* Each block (project) can be expanded with a plus button to see its internal dependencies.
* You can drill down from projects to namespaces, classes, and methods.
* In a large project, it’s usually best to focus only on a relevant area rather than expanding everything.

---

### Using Code Map in debugging or exploring

Suppose you want to analyze a method in an online store app that adds a product to a user's wishlist.

* Right-click the method in the code editor and select **Show on Code Map**.
* You will see the structure around this method.

A green arrow marks your current location in the code. Moving your cursor in the code or double-clicking on blocks in the map highlights the corresponding places.

---

### Exploring dependencies

* Click **Refetch Children** on a project or controller node to see methods it calls and other referenced classes.
* You may see that the method calls two repositories: one to get a product by ID, and another to add it to the user’s favorites.
* Right-click the method and select **Show Fields This References** to see what fields it uses.
* Select **Show Methods This Calls** to see other methods called inside.

Visual Studio automatically draws arrows and maps these relationships — this is not a manual drawing.

---

### Tracking interface implementations

If the method calls an interface method (e.g., `AddAsync`), you can:

* Right-click the interface method and select **Find All References**.
* You’ll find the class that implements this interface, such as `FavoriteDbRepository`.
* Then you can do **Show Methods This Calls** again to see the repository’s internal logic.

---

### Final view

By following this chain, you’ll end up at the database model (e.g., `FavoriteProduct` entity).

This way, the Code Map gives you a complete, visual trace from the controller method down to the database model:

```
Controller method → Repository calls → DB Model
```

---

### Summary

* Code Map is a powerful tool for understanding code flow and dependencies.
* It’s especially useful for debugging or onboarding in large projects.
* You can navigate back and forth between code and map seamlessly.
* Use features like **Show Methods This Calls**, **Show Fields This References**, and **Find All References** to explore deeply.

---
