
## Global Exception Hander

1. Implement global exception handler using IExceptionHandler and register

```
builder.Services.AddExceptionHandler<GlobalExceptionHandler>();
builder.Services.AddExceptionHandler<BadRequestExceptionHandler>();
builder.Services.AddExceptionHandler<NotFoundExceptionHandler>();
builder.Services.AddProblemDetails();
```

Multiple exception handlers can be chained to handle flowcontrol, but error handling is better for performance reasons

2. Use middleware

```
if (app.Environment.IsDevelopment())
{
    app.UseDeveloperExceptionPage();
}
else
{
    app.UseExceptionHandler("/Error");
}
```

## Build Exception page