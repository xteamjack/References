- ASP .net core documentation
  - https://learn.microsoft.com/en-us/aspnet/core/?view=aspnetcore-8.0

- ASP.Net Core Fundamentals
  - https://learn.microsoft.com/en-us/aspnet/core/fundamentals/?view=aspnetcore-8.0&tabs=windows
  - Configuration Management
  - Error and Exception
    - https://learn.microsoft.com/en-us/aspnet/core/web-api/handle-errors?view=aspnetcore-8.0
    - https://medium.com/@malarsharmila/leveraging-iexceptionhandler-for-effective-error-handling-in-asp-net-core-8-0-5e994ed4e9b4
  - .net core 8 api security implementation
  - Logging and Tracing
    - ELK stack
      - https://tohidhaghighi.medium.com/logging-with-elasticsearch-kibana-asp-net-core-and-docker-ca70bde6b56a
    - Window Default
      - https://learn.microsoft.com/en-us/aspnet/core/fundamentals/logging/?view=aspnetcore-8.0
    - Http Logging
      - https://learn.microsoft.com/en-us/aspnet/core/fundamentals/http-logging/?view=aspnetcore-8.0
  - Monitoring and Telemetry
    - Otel
      - Logging and Analysis with Otel and Loki
        - https://addozhang.medium.com/efficient-application-log-collection-and-analysis-using-opentelemetry-and-loki-baf04bc4a8a2
    - Prometheus and Grafana 
      - https://medium.com/@faulybsb/net-8-api-with-prometheus-and-grafana-29003adafd43
    - Tracing
      - https://learn.microsoft.com/en-us/dotnet/core/diagnostics/distributed-tracing-concepts?view=aspnetcore-8.0
  - Minimal API with CQRS
    - https://tohidhaghighi.medium.com/goodbye-controllers-hello-minimal-apis-ed16ccb4e6a2
  - CQRS and Clean Architecture
    - https://medium.com/@EdsonMZ/implementing-the-cqrs-and-mediator-pattern-in-a-net-8-web-api-8c0319a4525c
    - Sorting, filtering and pagination
      - https://www.youtube.com/watch?v=X8zRvXbirMU

- Web Development 
  - Razor Page Quick Start
    - https://learn.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/razor-pages-start?view=aspnetcore-8.0&tabs=visual-studio

- Instrumentation
  - Health checks
    - https://medium.com/@jeslurrahman/implementing-health-checks-in-net-8-c3ba10af83c3
    - https://mahedee.net/Application-health-monitoring-using-asp.net-core/
- Data Management
  - EF and Razor
    - https://learn.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-8.0&tabs=visual-studio-code#asynchronous-code
    - Seeding
 
  - EF and MVC
    - https://learn.microsoft.com/en-us/aspnet/core/data/ef-mvc/?view=aspnetcore-8.0
    - 1:m, n:m relationships
  - Generic Repository
    - https://www.youtube.com/watch?v=QUuCqOyfJs8
  - Generic Repository without EF
    - https://www.youtube.com/watch?v=a1Sbmv0qPpw
  - Unit of Work
    - https://www.youtube.com/watch?v=NNT0-6moCJM
  - Azure Table
    - https://www.youtube.com/watch?v=w3OWlnOgjF8
  - Expression Pattern
    - https://www.youtube.com/watch?v=7nM7E-c7vYw
  - AutoMapper to map Model to DTO
  - Helpers
    - Sorting, filtering and pagination
      - https://medium.com/@rashad_m/mastering-filtering-and-pagination-in-asp-net-core-and-react-js-part-1-591b10a65993
      - IRepository implementation https://www.youtube.com/watch?v=BybOuj3hYUw
      - sieve processor: Ready to use try this
        - https://www.youtube.com/watch?v=9a0ppipDOgI
  - Bulk Operations
    - https://mahedee.net/utilizing_bulk_operations_with_entity_framework_and_aspnet_core/
  - Audit Trail
    - https://mahedee.net/Step-by-Step-Guide-to-Integrating-Audit-Trail-in-ASPNET-Core-Using-ADONET/
  - Concurrency
    - https://mahedee.net/concurrency_management_in_aspnet_core_applications_with_entity_framework/
  - Elastic Search CRUD
    - https://www.youtube.com/watch?v=_VEe-XksRlY


- Security
  - Auth
    - Identity Framework
      - https://learn.microsoft.com/en-us/training/modules/secure-aspnet-core-identity/?view=aspnetcore-8.0
  - OIDC
  - Azure B2C
    - https://learn.microsoft.com/en-us/azure/active-directory-b2c/secure-rest-api?tabs=windows&pivots=b2c-user-flow
  - RestTokens
    - https://medium.com/@bruno-bernardes-tech/how-to-implement-jwt-authentication-in-asp-net-core-269f258f19be
  - Web API

- Internationalization
  - Localization from DB
    - https://www.ezzylearning.net/tutorial/asp-net-core-localization-from-database

- CICD
  - Containerization - Docker
  - Orchestrate with Docker Swamp
  - Monitoring
    - Monitoring Docker with Grafana, Loki, and Promtail
      - https://abhiraj2001.medium.com/monitoring-docker-containers-with-grafana-loki-and-promtail-4302a9417c0d
  - Kubernetes and AKS

- Middleware
  - https://learn.microsoft.com/en-us/aspnet/core/fundamentals/middleware/?view=aspnetcore-8.0
  - Testing
  - Response Caching

- API
  - MVC
    - https://medium.com/@chandrashekharsingh25/build-a-restful-web-api-with-net-8-44fc93b36618
  - API - Both controller centric and Minimal API
    - https://learn.microsoft.com/en-us/aspnet/core/fundamentals/apis?view=aspnetcore-8.0
  - API authorization with Identity and Access Management
    - https://learn.microsoft.com/en-us/aspnet/core/security/authentication/identity-api-authorization?view=aspnetcore-8.0
  - API Key Security Implementation
    - https://www.infoworld.com/article/3705948/how-to-improve-api-security-in-aspnet-core.html
  - API Key Security Middleware
    - https://www.infoworld.com/article/3701888/how-to-use-api-keys-to-secure-web-apis-in-aspnet-core.html
  - JWT for ASP .Net Core
    - https://medium.com/@sajadshafi/jwt-authentication-in-c-net-core-7-web-api-b825b3aee11d
    - https://medium.com/@bruno-bernardes-tech/understanding-security-with-jwt-authentication-authorizatgion-and-tokens-in-apis-6a406c460daf
    - https://medium.com/@bruno-bernardes-tech/how-to-implement-jwt-authentication-in-asp-net-core-269f258f19be
  - Rate Limiting
    - https://www.infoworld.com/article/3442946/how-to-implement-rate-limiting-in-aspnet-core.html
  - Rate Limiting Middleware
    - https://learn.microsoft.com/en-us/aspnet/core/performance/rate-limit?view=aspnetcore-8.0
  - Versioning
    - https://medium.com/@EdsonMZ/web-api-versioning-in-net-core-6a33d6780a41
  - Refit, invoke external API
    - https://medium.com/net-core/using-refit-in-net-0843bb199987

- Other
  - Url Rewriting
    - https://learn.microsoft.com/en-us/aspnet/core/fundamentals/url-rewriting?view=aspnetcore-8.0

- Microservices
  - https://dotnet.microsoft.com/en-us/learn/microservices

- Testing
  - Unit Testing
    - https://learn.microsoft.com/en-us/aspnet/web-api/overview/testing-and-debugging/unit-testing-with-aspnet-web-api

- C# Programming
  - Dispose Pattern
    - https://medium.com/@kmorpex/7-most-common-mistakes-in-c-programming-%EF%B8%8F-904f05800be3


Bloggers

- https://www.youtube.com/@dotnetrealworldexample/videos
  - All .Net and other advanced concepts on app development
- https://www.youtube.com/@Ardalis/videos
  - Master class on lots of C# aspects


Architecture
- Clean Architecture template
  - https://www.youtube.com/watch?v=NTg7tZrNRhQ