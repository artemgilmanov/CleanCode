# 🔥 Frequently Used Hotkeys (Visual Studio & Windows)

### 💻 **General & Code Editing**

* **`Win + V`** – *Clipboard History (Windows 10+)*
  Access and choose from multiple copied items — very helpful when switching between code snippets.

* **`Ctrl + K, C`** – *Comment selected code*

* **`Ctrl + K, U`** – *Uncomment selected code*

* **`Ctrl + K, D`** – *Format Document*
  Automatically fixes indentation and spacing.

* **`Ctrl + K, E`** – *Run Code Cleanup*
  Applies predefined code cleanup rules.

* **`Ctrl + R, G`** – *Remove and sort unused `using` directives*

* **`Ctrl + G`** – *Go to a specific line number*

* **`Ctrl + Shift + B`** – *Build the solution*

---

### 🔍 **Navigation & Debugging**

* **`Ctrl + T`** – *Go To Everything*
  Quickly find files, classes, methods, symbols, etc.

* **`Ctrl + F12`** – *Go to definition* (jumps to method or class implementation)

* **`Shift + F12`** – *Find all references* (where a method or variable is used)

* **`Ctrl + -`** – *Go back* (return to previous cursor position)

* **`Ctrl + Alt + B`** – *Open Breakpoints Window*

---

### 📂 **Code Folding**

* **`Ctrl + M, O`** – *Collapse all methods* in the file

* **`Ctrl + M, L`** – *Expand all methods*

---

### 🔧 **Beginner-Friendly Editing Tricks**

* **`Tab`** – *Indent selected lines to the right*

* **`Shift + Tab`** – *Indent left*

* **`Ctrl + Shift + ←/→`** – *Select entire words instead of letter-by-letter*

* **`Alt + Left Click + drag`** – *Multi-line caret*
  Type or edit across multiple lines at once.

* **`Shift + Del`** – *Delete the current line*

---

### ✅ **New Example: Using Some Hotkeys Together**

Suppose you’re refactoring code and you find some duplicate logic:

```csharp
var userList = GetUsers();
foreach (var user in userList)
{
    Console.WriteLine(user.Email);
}
```

You can:

* Use `Ctrl + K, C` to comment this block temporarily.
* Use `Ctrl + T` to quickly find the `GetUsersFromDatabase` method.
* Use `Ctrl + -` to return to your last edit.
* Use `Ctrl + R, G` to clean up `using` directives.
* Use `Ctrl + K, D` to auto-format the refactored block.

---
