Global exception handler helps in catching all the exception in the web application or web services (any http implementation)

## Index
1. How to build a global exception handler
   1. Create and register global exception handler
   2. Improve error messing with additional information
   3. Create custom exception page for web apps
2. Create custom exception hierarchy
3. Best Practices

## 1. How to build a global exception handler

### 1.1 Create and register global exception handler
Global Exception Handler can be implemented in three ways:

A. Built in exception middleware
B. Custom exception middleware
C. IExceptionHandler (.net 8)

Each of the approaches broadly divided into two parts, create and register...

Quote: A good video summarizing all the three methods as a beginner
https://www.youtube.com/watch?v=ctzn56OaXfQ

#### Approach A:
#### Approach B:
#### Approach C: Implementing IExceptionHandler

Steps
1. Define IExceptionHandler
2. Perform service building with builder.Services
3. Register middleware

Implement global exception handler using IExceptionHandler and register

```
builder.Services.AddExceptionHandler<GlobalExceptionHandler>();
builder.Services.AddExceptionHandler<BadRequestExceptionHandler>();
builder.Services.AddExceptionHandler<NotFoundExceptionHandler>();
builder.Services.AddProblemDetails();
```

Multiple exception handlers can be chained to handle flowcontrol, but error handling is better for performance reasons

1. Use middleware

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

### 1.2 Improve error messing with additional information
Improve the exception information with ProblemDetails class
Note: https://www.youtube.com/watch?v=iv7fdvSKwAY&t=431s

Additionally implement custom problem details handler

### 1.3 Build Exception page
It is a good practice to implement a custom page to display exception information with Razor application

TBD:

## 2. Best Practices

