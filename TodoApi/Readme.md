✅ Todo API - Minimal API con ASP.NET Core
Esta es una Minimal API construida con ASP.NET Core y Entity Framework Core. Permite gestionar una lista de tareas (Todo list), incluyendo operaciones CRUD básicas: crear, leer, actualizar y eliminar tareas.

🚀 Tecnologías Utilizadas
*** .NET 8 / .NET 7 ***

*** ASP.NET Core Minimal API ***

*** Entity Framework Core (In-Memory DB) ***

*** C# ***

📁 Estructura del Proyecto
/TodoApi
│
├── Program.cs       // Configura la API y define los endpoints
├── Todo.cs          // Modelo de datos
└── TodoDb.cs        // DbContext de Entity Framework

🔧 Configuración y Ejecución
### Clona el repositorio
```git clone https://github.com/tuusuario/todoapi.git```
```cd todoapi```
### Ejecuta el proyecto
```dotnet run```
La API estará disponible por defecto en:
http://localhost:5000 o https://localhost:5001

📌 Endpoints
🔍 GET /todoitems/
Obtiene todas las tareas.
[
  { "id": 1, "name": "Aprender C#", "isComplete": false },
  ...
]
➕ POST /todoitems/
Crea una nueva tarea.

Body:
{
  "name": "Estudiar Minimal APIs",
  "isComplete": false
}
🧠 Modelo de Datos
public class Todo
{
    public int Id { get; set; }
    public string? Name { get; set; }
    public bool IsComplete { get; set; }
}

🗃️ Base de Datos
Se utiliza una base de datos en memoria (InMemoryDatabase) solo para fines de desarrollo y pruebas. No se requiere ninguna configuración adicional.
builder.Services.AddDbContext<TodoDb>(opt => 
    opt.UseInMemoryDatabase("TodoList"));

