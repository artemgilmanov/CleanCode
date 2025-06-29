# 🏷 Recommended XML Documentation Tags in C\#

When working on real-world C# projects, methods and classes can become complex.
Proper documentation is essential to make code easier to understand, especially for junior developers.
C# supports **XML documentation comments** that provide structured and easily accessible information about code elements.

## ✍️ Standard vs. XML Comments

* `// This is a standard comment` — useful for inline or block explanations.
* `///` — used for **XML documentation comments**. Typing `///` above a method or class automatically inserts XML tags.

---

## ✅ Common XML Documentation Tags

### 1. `<summary>`

Describes **what a method, property, field, or class does**.

#### Example:

```csharp
/// <summary>
/// Calculates the sum of two integers.
/// </summary>
static int GetSumNumbers(int num1, int num2)
{
    return num1 + num2;
}
```

🔍 When hovering over the method, this summary appears in tooltips.

---

### 2. `<returns>`

Describes **what the method returns**.

#### Example:

```csharp
/// <summary>
/// Calculates the sum of two integers.
/// </summary>
/// <returns>
/// Integer result of the sum.
/// </returns>
static int GetSumNumbers(int num1, int num2)
{
    return num1 + num2;
}
```

🧠 Helps other developers understand the output of the method.

---

### 3. `<param>`

Describes each **parameter** of a method. Each parameter should have a separate `<param>` tag with a matching `name` attribute.

#### Example:

```csharp
/// <summary>
/// Calculates the sum of two integers.
/// </summary>
/// <returns>
/// Integer result of the sum.
/// </returns>
/// <param name="num1">
/// The first integer.
/// </param>
/// <param name="num2">
/// The second integer.
/// </param>
static int GetSumNumbers(int num1, int num2)
{
    return num1 + num2;
}
```

🎯 Tooltips will now display descriptions for method arguments when the method is used elsewhere.

---

## 🛠 Additional XML Documentation Tags

While `<summary>`, `<param>`, and `<returns>` are the most frequently used, there are many other tags available in C# XML documentation:

| Tag                   | Description                                                |
| --------------------- | ---------------------------------------------------------- |
| `<example>`           | Provides usage examples for the method/class.              |
| `<exception>`         | Documents exceptions that may be thrown.                   |
| `<remarks>`           | Adds additional information or implementation details.     |
| `<value>`             | Used in property documentation to describe the value.      |
| `<typeparam>`         | Describes a type parameter for generic methods or classes. |
| `<see>` / `<seealso>` | Adds links to related methods, classes, or docs.           |

---

## 📌 Summary

Using XML documentation:

* Improves **code readability** and **self-documentation**.
* Helps **team members understand** your code faster.
* Enhances **IntelliSense support** in Visual Studio.

Start with these three essential tags:

* `<summary>`
* `<returns>`
* `<param>`

And expand to other tags as your code and API complexity grows.

---
