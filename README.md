# .NET Clean Architecture template

A layered .NET 6 sample from the Clean Architecture sub-group of Folio3's .NET EMG (an internal engineering
group; I led the sub-group in 2022), used as reference material for our knowledge-sharing and code-review sessions.

One business layer serves three front ends (Web API, console and Windows Forms), and a data factory switches the
data layer between **ADO.NET** and **Entity Framework Core** without changing the layers above it.

| Project | Role |
|---|---|
| `CleanArchitecture.API` | ASP.NET Core Web API |
| `CleanArchitecture.Console`, `CleanArchitecture.WindowsForms` | Other front ends over the same business layer |
| `CleanArchitecture.Business` | Services and DTOs |
| `CleanArchitecture.Data` | Entities and repository contracts |
| `CleanArchitecture.DataFactory` | Picks the data-access implementation |
| `CleanArchitecture.ADO`, `CleanArchitecture.EF` | ADO.NET and EF Core repositories |

Credit: built together with the members of the .NET EMG Clean Architecture sub-group.
