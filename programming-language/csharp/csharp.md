---
applyTo: "**/*.cs"
---

# Project Coding Standards for C# and .NET

## Naming Conventions

- Use **PascalCase** for class names, methods, public properties, and constants
- Use **camelCase** for local variables and parameters
- Prefix interfaces with `I` (e.g., `ILogger`, `IService`)
- Private fields may use `_camelCase` if consistent project-wide
- Avoid Hungarian notation and unnecessary abbreviations

## Layout & Formatting

- Use **four spaces** for indentation (no tabs)
- Place **opening braces on a new line**
- Prefer **file-scoped namespaces** for new code
- Place `using` statements **outside** the namespace
- Group class members by visibility: public → protected → internal → private

## Language Usage

- Use `var` when the type is obvious; otherwise, use explicit types
- Use **expression-bodied members** only when it improves readability
- Prefer **string interpolation** over `string.Format`
- Use `nameof()` instead of hardcoded strings
- Use **nullable reference types** and nullability annotations (`string?`, etc.)

## Async & Exception Handling

- Use `async`/`await`; avoid `.Result` or `.Wait()`
- Use `ConfigureAwait(false)` in libraries
- Do not use exceptions for control flow
- Catch specific exceptions, not generic `Exception`

## Project Structure

- Use the `dotnet new` CLI to scaffold:
  - `dotnet new webapi -n CleanApiTemplate`
- Suggested folders:
  - `Controllers/`
  - `Models/`
  - `Services/`
  - `Repositories/`
- Structure follows clean separation of concerns

## Example

```csharp
public interface IOrderService
{
    Task<bool> PlaceOrderAsync(OrderDto order);
}

public class OrderService : IOrderService
{
    public async Task<bool> PlaceOrderAsync(OrderDto order)
    {
        if (order == null) throw new ArgumentNullException(nameof(order));
        // Simulated async logic
        await Task.Delay(100);
        return true;
    }
}
```
