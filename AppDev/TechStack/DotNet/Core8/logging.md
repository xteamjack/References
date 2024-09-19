Different types of Logging

- Http Logging
- Application Logging

## Http Logging

Track and log different http request and responses

1. Register standard logging
```
builder.Services.AddHttpLogging(logging =>
{
    logging.LoggingFields = HttpLoggingFields.All;

    // Log request and response segments
    logging.RequestHeaders.Add("sec-ch-ua");
    logging.ResponseHeaders.Add("MyResponseHeader");

    // Log various media encoding
    logging.MediaTypeOptions.AddText("application/javascript");

    // Log when Req, Res limit exceed
    logging.RequestBodyLogLimit = 4096;
    logging.ResponseBodyLogLimit = 4096;
    logging.CombineLogs = true;
});
```

```
app.UseHttpLogging();
```

Set logging configuration

```
"Microsoft.AspNetCore.HttpLogging.HttpLoggingMiddleware": "Information"
```

2. Build logging interceptors

```
builder.Services.AddHttpLoggingInterceptor<CustomHttpLoggingInterceptor>();
```


```
internal sealed class CustomHttpLoggingInterceptor : IHttpLoggingInterceptor
{
    public ValueTask OnRequestAsync(HttpLoggingInterceptorContext logContext)
    {
        ...
        return default;
    }

    public ValueTask OnResponseAsync(HttpLoggingInterceptorContext logContext)
    {
        ...
        return default;
    }

    private void RedactPath(HttpLoggingInterceptorContext logContext)
    {
        ...
    }

    private void RedactRequestHeaders(HttpLoggingInterceptorContext logContext)
    {
        ...
    }

    private void EnrichRequest(HttpLoggingInterceptorContext logContext)
    {
        ...
    }

    private void RedactResponseHeaders(HttpLoggingInterceptorContext logContext)
    {
        ...
    }

    private void EnrichResponse(HttpLoggingInterceptorContext logContext)
    {
        ...
    }
}

```

3. Add logging to an endpoint

```
app.MapGet("/metrics", () => "Metrics!")
    // Custom logging for the endpoint
    .WithHttpLogging(HttpLoggingFields.ResponsePropertiesAndHeaders);
```

## Web Application Logging
Application functionality level logging

1. Register logging providers

```
builder.Logging.ClearProviders();
builder.Logging.AddConsole();
```

2. ID logging into respective classes and start logging

```
public Doctor(ISieveProcessor sieveProcessor, PrimaryDbContext context, ILogger<IDoctor> logger)
```

```
_logger.LogInformation("Data fetched for Doctor " + filtered.Count + " record(s)",
    DateTime.UtcNow.ToLongTimeString());
```



Levels of logging:
Trace = 0, Debug = 1, Information = 2, Warning = 3, Error = 4, Critical = 5, and None = 6.

Different Providers???


Different Logging Managers

- ASP.NET logging
  - Comes by default with Aspire .Net
- NLog
- SeriLogging
- 