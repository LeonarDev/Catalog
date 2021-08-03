# .NET 5 REST API

Creating a REST API end-to-end from scratch using the latest .NET 5 innovations and Visual Studio Code. 
Written in C#.

- Entity, Repository, Controller GET
- Dependency Injection, DTOSs
- POST, PUT, DELETE
- Persisting Entities with MongoDB
- Tasks, Async and Await
- Secrets and Health Checks
- Docker
- Kubernetes
- Unit Testing and TDD


## Notes

### Record Types
- Use for immutable objects
- With-expressions support
- Value-based equality support:
  ```c#
  Item portion1 = new() { Name = "Portion", Price = 9 };
  Item portion2 = new() { Name = "Portion", Price = 9 };
  bool areEqual = portion1 == portion2; // = true

  Item portion3 = portion1 with { Price = 15 };
  areEqual = portion1 == portion3; // = false
    ```

<br>

### init (properties)
- It allows the definition of a value only during startup:
  ```c#
  public int Id { get; init; }
  // public int Id { get; private set; } // Here we have to introduce a constructor
  ```