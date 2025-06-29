# 📘 API Documentation with Swagger in ASP.NET Core

**OpenAPI** is a powerful tool for generating and visualizing web API documentation automatically based on source code and XML comments. 
In **Visual Studio 2022**, Swagger integration is available out-of-the-box when creating ASP.NET Core web applications.

---

## 🔧 Enabling XML Documentation for Swagger

To use XML comments in Swagger, first enable **XML documentation file generation**:

### ✅ Step 1: Enable XML Comments in Project Settings

1. Right-click your project > **Properties**
2. Go to the **Build** tab
3. Enable **XML documentation file** output

---

### ✅ Step 2: Configure Swagger in `Program.cs`

Add the following configuration to register Swagger and connect the XML documentation:

```csharp
builder.Services.AddSwaggerGen(options =>
{
    var basePath = AppContext.BaseDirectory;
    var xmlPath = Path.Combine(basePath, "SomeProjectName.xml"); // name must match the XML output file name
    options.IncludeXmlComments(xmlPath, includeControllerXmlComments: true);

    options.SwaggerDoc("v1", new OpenApiInfo
    {
        Version = "v1",
        Title = "Some-Project-Name",
        Description = "ASP.NET Core Web API for the Some-Project-Name."
    });
});
```

> 📌 Ensure `"SomeProjectName.xml"` matches your actual project name and XML output filename.

---

## 🧩 Example: Documenting an API Controller

```csharp
/// <summary>
/// Users controller
/// </summary>
[ApiController]
[Authorize]
[Route("[controller]")]
public class UsersController : ControllerBase
{
    private UsersService _usersService;

    public UsersController(UsersService usersService)
    {
        _usersService = usersService;
    }

    /// <summary>
    /// Searches for user profiles by name
    /// </summary>
    /// <returns>
    /// A list of matching users
    /// </returns>
    /// <param name="name">
    /// The full or partial name to search for
    /// </param>
    [HttpGet("all/{name}")]
    public IActionResult GetUsersByName(string name)
    {
        var users = _usersService.GetUsersByName(name);
        return users == null ? NotFound() : Ok(users);
    }
}
```

This documentation will automatically appear in Swagger UI, displaying:

* A summary of the controller and its methods
* Descriptions of parameters and return types
* Authorization and routing information

---

## 📄 What You Get in Swagger UI

* An interactive webpage listing all your API endpoints
* Tooltips with descriptions from `<summary>`, `<param>`, and `<returns>` tags
* The ability to test endpoints directly within the UI

---

## 📚 Learn More

For more detailed Swagger usage in ASP.NET, visit:

👉 [Get started with Swashbuckle and ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-8.0&tabs=visual-studio)

---
