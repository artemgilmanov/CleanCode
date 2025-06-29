# 🧭 Code Navigation Tools in Visual Studio: Bookmarks & Task List

When working on large codebases, it's essential to track important lines of code and unfinished work efficiently. 
Visual Studio provides built-in tools to **bookmark** code and **track tasks** using special comments.

---

## 🔖 Bookmarks in Visual Studio

### 📌 What are Bookmarks?

Bookmarks let you "mark" lines in your code—like placing a bookmark in a book—so you can quickly return to them later.

### ➕ How to Add/Remove a Bookmark

1. **Place your cursor** on the desired line.
2. Click the **"Toggle a bookmark"** button in the toolbar
   *or*
   Press **Ctrl + K, K**
   (press the same shortcut again to remove it)

### 📚 View All Bookmarks

To view and manage bookmarks:

* Use the **Bookmark Window** (`View > Bookmark Window`)
* Or click the **Bookmark icon** on the toolbar

From the Bookmark window, you can:

* Navigate to the **next/previous** bookmark
* **Add**, **delete**, or **rename** bookmarks
* **Group** bookmarks by folder or file

---

## 📝 Task List Comments

The **Task List** in Visual Studio allows you to track special comments in your code that act like to-do items.

### 🧷 Supported Tags

| Tag      | Purpose                                                         |
| -------- | --------------------------------------------------------------- |
| `TODO`   | Marks tasks that should be completed later                      |
| `UNDONE` | Highlights partially completed work or changes to revisit       |
| `HACK`   | Indicates quick fixes or workarounds that need proper solutions |

### 🧪 Example

```csharp
app.UseHttpsRedirection(); // TODO: Implement edge case validation
app.UseStaticFiles();      // UNDONE: Add error handling
app.UseRouting();          // HACK: Temporary fix, improve later
```

> ✅ Note: `TODO` and `UNDONE` are functionally similar—both flag tasks requiring attention.

### 📄 View the Task List

1. Go to `View > Task List`
2. The **Task List** window shows all matching comments across the solution
3. Clicking an item in the list navigates directly to the relevant line

---

## 🚀 Summary

| Feature       | Benefit                                        |
| ------------- | ---------------------------------------------- |
| **Bookmarks** | Navigate quickly to key lines of code          |
| **Task List** | Track actionable comments like TODOs and HACKs |

These tools help streamline **code review**, **debugging**, and **feature planning**, especially in complex projects.

---
