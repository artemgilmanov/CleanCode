# 📄 Code Formatting and Cleanup Guide (Visual Studio)

This guide describes how to configure and use Visual Studio's **Code Cleanup** tool with the most useful rules to maintain clean and consistent C# code.

---

## 🔧 Setting Up the Code Cleanup Tool

You can open the **Code Cleanup** tool as following:
* By right-clicking on the **Solution** in Solution Explorer and selecting "Analize and Code Cleanup".
* Configure **Profile 2** with custom cleanup rules, while **Profile 1** remains with default settings.

To check the description all rules refer to: https://learn.microsoft.com/en-us/visualstudio/ide/code-styles-and-code-cleanup?view=vs-2022&pivots=programming-language-dotnet#code-styles-in-the-options-dialog-box

> 💡 To run Code Cleanup manually using Profile 2, press `Ctrl + K + E`.

---

## ✏️ Recommended Cleanup Rules (for Profile 2)

### 1. **Format Document**

* Applies formatting rules (indentation, spacing, etc.).
* Shortcut: `Ctrl + K + D`.

### 2. **Remove Unnecessary Imports or Usings**

* Removes unused `using` directives (highlighted in gray).

### 3. **Sort Imports or Usings**

* Alphabetically sorts `using` directives.

### 4. **Remove Unused Variables**

* Deletes unused variables (highlighted in gray).

### 5. **Add 'this' or 'Me' Qualification**

* Removes unnecessary `this` keyword where not required.

### 6. **Add Accessibility Modifiers**

* Adds `private` modifier by default if no access modifier is specified.

### 7. **Order Modifiers**

* Ensures modifiers follow .NET standard order:

  ```
  public, private, protected, internal, file, static, extern, new, virtual, abstract, 
  sealed, override, readonly, unsafe, required, volatile, async
  ```

### 8. **Remove Unnecessary Casts**

* Eliminates unnecessary type casts (e.g., `(int)0` when not needed).

### 9. **Apply Object/Collection Initialization Preferences**

* Converts verbose object initialization to compact initializer syntax.

### 10. **Apply String Interpolation Preferences**

* Replaces concatenations or redundant `.ToString()` with string interpolation.

### 11. **Apply Compound Assignment Preferences**

* Converts expressions like `x = x + 5` to `x += 5`.

### 12. **Apply Auto-Property Preferences**

* Converts full property with private backing field into auto-implemented property.

### 13. **Apply Coalesce Expression Preferences**

* Simplifies null-check expressions (e.g., `x == null ? y : x` → `x ?? y`).

### 14. **Apply Conditional Expression Preferences**

* Converts simple `if-else` logic into ternary operator (`? :`) where applicable.

### 15. **Add Required Braces for Single-Line Control Statements**

* Adds braces to single-line `if`, `for`, `while`, etc., to improve readability and maintainability.

---

## ⚙️ Run Code Cleanup on File Save

You can configure Visual Studio to automatically run code cleanup on save:

> Navigate to:
> `Tools` → `Options` → `Text Editor` → `Code Cleanup`
> Enable “Run Code Cleanup on Save” for your chosen profile.

---

## ✅ Summary of Included Cleanup Options

| Rule Name                                      | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- |
| Add required braces for single-line statements | Adds `{}` braces to improve clarity            |
| Add accessibility modifiers                    | Explicitly sets access level (e.g., `private`) |
| Add 'this' or 'Me' qualification               | Removes unnecessary `this`                     |
| Apply object/collection initialization         | Uses inline initializers                       |
| Apply string interpolation preferences         | Converts to string interpolation               |
| Apply compound assignment preferences          | Uses `+=`, `-=`, etc.                          |
| Apply auto property preferences                | Uses auto-properties                           |
| Apply coalesce expression preferences          | Uses `??` operator                             |
| Apply conditional expression preferences       | Uses ternary `? :` operator                    |
| Format document                                | Applies code formatting                        |
| Sort Imports or usings                         | Sorts `using` directives alphabetically        |
| Order modifiers                                | Fixes modifier order to .NET standards         |
| Remove unnecessary casts                       | Deletes redundant type casts                   |
| Remove unused variables                        | Deletes unused variables                       |
| Remove unnecessary Imports or usings           | Deletes unused `using` directives              |

---
