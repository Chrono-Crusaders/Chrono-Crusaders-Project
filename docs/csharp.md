# C\# Tutorial

## Basics

- Developed in the year 2000 by Microsoft.
- General-purpose programming language, known for being easy to learn while reamining powerful.
- C/ C++ like syntax.
- Primarily used with the .NET framework, which is supported on Windows, macOS and Linux.
- Statically typed: The type of a variable must be explicitly defined during its declaration. This often helps catch errors early, as many errors are detected at *compile time* rather than runtime.
- Strong emphasis on objects and components: Usage of encapsulation, inheritance, polymorphism  and modern tools like properties, events and delegates for building modular software.
- Applications: Enterprise applications, game development, backend services, cloud-based applications, mobile applications and web applications.

### Programming Paradigms

- Imperative
- Object-Oriented
- Event-Driven
- Functional
- Concurrent/ Asynchronous

### Key Features

- **Statically typed:** Variable types need to be defined at compile time.
- **Memory management:** Automatic garbage collection.
- **Code has no fixed structure:** Whitespaces does not affect the functionality of the code.

### Example Program

```csharp
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World");
        }
    }
}
```

### Example Godot Script

\<Placeholder\>

## Creating a Project

### Using the Shell

```bash
dotnet new console -n HelloWorld
cd ./HelloWorld
dotnet run
```

- *Console* is the desired project type.
- *HelloWorld* is the desired project name.
- *-n* enables to specify the project name.

### Project Types

| Type | Description |
| ---- | ---- |
| Console Application | a simple, text-based application |

## Comments and Documentation

### Comments

- Serve to make the code more understandable and maintainable.
- Especially important in larger projects with multiple members.

```csharp
// single-line comments

/* multi-line
   comment */
```

### Documentation

- XML documentation comments are used to document the code.
- Can be processed into external documentation by tools like Doxygen or used by IDE line documentation.
- Documentation gives insight into the usage and functionality of variables, parameters, classes and methods.

```csharp
/// <summary>
/// Example for standard output.
/// </summary>
/// <remarks>
/// author: Dominic
/// history: 2024-17-07
/// </remarks>
public class MyClass
```
