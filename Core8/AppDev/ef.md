

Add database references

```
dotnet add package Microsoft.EntityFrameworkCore.InMemory
```

```
dotnet add package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore
```


Migrations

- update EF tools
dotnet tool update --global dotnet-ef

- Set environment
dotnet ef database update -- --environment Production

- Create intiali migration
dotnet ef migrations add InitialDoctorDb

- Update the database
dotnet ef database update

- Generate scaffolding from database
dotnet ef dbcontext scaffold