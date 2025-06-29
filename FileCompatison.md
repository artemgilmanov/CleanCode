# 🧾 File Comparison in Visual Studio

Visual Studio includes a **built-in file comparison tool**, similar to external programs like **WinMerge**, allowing you to compare code between files, branches, or versions (as in Git diffs).

---

## 🔍 When to Use

* Refactoring duplicate methods
* Comparing two versions of a file
* Identifying changes across environments or branches
* Merging logic from similar implementations

---

## 📂 How to Compare Files in Visual Studio

1. In **Solution Explorer**, **right-click** on the first file you want to compare.
2. Select **"Compare With..."**
3. Choose the **second file** you want to compare.
4. Visual Studio will open a **side-by-side comparison view**, highlighting:

   * Inserted lines (usually green)
   * Deleted lines (usually red)
   * Modified lines (usually yellow or orange)

---

## 🎯 Benefits

* No need for third-party tools like **WinMerge**
* Integrated with your solution, Git history, and source control
* Ideal for **code deduplication**, **refactoring**, and **reviewing changes**

---

## ✅ Tip

You can also launch comparisons from **Team Explorer** or through the **Command Window** with:

```bash
Tools.DiffFiles <file1> <file2>
```

Or use `vsdiffmerge.exe` directly if needed outside the IDE.

---
