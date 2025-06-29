# 🛠️ Debugging an Application in Visual Studio

## 🔎 Example Code

We'll work with a `Student` class and a method `GetTopStudents` that filters students with scores above 85.

```csharp
public class Student
{
    public int Id { get; set; }
    public string Name { get; set; }
    public int Score { get; set; }
}

public class Program
{
    public static void Main()
    {
        var students = new List<Student>()
        {
            new Student { Id = 1, Name = "Alice", Score = 91 },
            new Student { Id = 2, Name = "Bob", Score = 78 },
            new Student { Id = 3, Name = "Charlie", Score = 88 },
            new Student { Id = 4, Name = "Diana", Score = 65 }
        };

        var topStudents = GetTopStudents(students);

        foreach (var student in topStudents)
        {
            Console.WriteLine(student.Name);
        }
    }

    public static List<Student> GetTopStudents(List<Student> students)
    {
        var topStudents = new List<Student>();
        foreach (var student in students)
        {
            if (student.Score > 85)
            {
                topStudents.Add(student);
            }
        }
        return topStudents;
    }
}
```

---

## 📍 Breakpoint

* A **breakpoint** is a line in the code where execution will pause so you can inspect variables.
* Shortcut: `F9` (toggle on/off)

---

## 🧪 Start Debugging

* Press `F5` to run the project in **Debug Mode**.
* Execution will pause at your breakpoint, and you'll see local variables in the **Locals** window:

  * View object details
  * Modify values at runtime
  * Click **View** to open data in a table-like format (sortable/filterable/exportable)

---

## 📋 Debugging Controls

| Command                 | Description                                               | Shortcut           |
| ----------------------- | --------------------------------------------------------- | ------------------ |
| **Step Over**           | Executes the current line without going into method calls | `F10`              |
| **Step Into**           | Goes into the method on the current line                  | `F11`              |
| **Step Out**            | Exits the current method and returns to the caller        | `Shift + F11`      |
| **Continue**            | Resumes execution until the next breakpoint               | `F5`               |
| **Show Next Statement** | Shows where the program is currently paused               | `Alt + *` (Numpad) |

---

## 🎯 Conditional Breakpoint

* Right-click a breakpoint → **Conditions**
* Example: `student.Name == "Charlie"`
  → The program will only stop if this condition is true.

---

## 📌 Breakpoint Management

* View all breakpoints: `Ctrl + Alt + B`

---

## 🧭 Run to a Specific Line

* Hover over a line → click ▶ **Run to Click**
* The debugger runs all code up to that line and pauses there.

---

## 📚 Call Stack Window

* Open via: `Debug → Windows → Call Stack` or `Ctrl + Alt + C`
* Shows the method call history (who called what).
* Helps trace how you got to the current line of execution.

---
