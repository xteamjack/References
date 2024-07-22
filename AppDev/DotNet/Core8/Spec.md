- UI
  - Microfront ends
  - CDN
- Architecture and Design
  - Microservices
    - Gateway
    - Registry
    - Circuit Breaker
  - Patterns
    - MVC
    - CQRS
  - Data and storage
    - Repository pattern
- Others
  - Url encoding or encryption to hide details in url
- API
- Security
  - Authentication
    - Custom forms authentication
    - Azure AD auth
      - with domain restriction - only people from allowed domains can login
    - Register oAuth users into a registered account
      - Register with AD then link google, facebook, twitter, ... accounts into the registered account
  - Authorization
  - Hardening
    - CORS
- Database
  - Generic
    - Database creation and seeding
      - Application Centric
      - Script based to decouple the db seeding from base application
  - Working with multiple databases (MSSQL, PostgreSQL, MySQL)
    - Switch the database through configuration settings

  - EF Core
  - LinQ Centric
  - Concurrency
  - Distributed Transactions
- Instrumentation
  - Health monitoring
  - Logging
  - Audit Trail
- Deployment
  - CI CD Pipeline
    - Jenkins integration
  - Docker containers
    - App config abstraction 
      - thru docker file
      - thru azure config store
    - CDN config abstraction
    - File store abstraction for attachment, uploaded images etc


Priority Listing
- Data Activities
  - Doctor data CRUD, Sort, Filter etc.,
  - Doctor data validations
  - 
- Basic health monitoring with live check, metrics dashboard
- Exception management with API, exception hierarchy
- Exception management for UI
- Configuration Management
- Authentication with B2C API
- Authentication with B2C Vue
- Authorization of users
- API authorization, JWT or other tokens
- End point authorization, public, by user, by group / role
- CORS implementation
- Logging with simple Log4J
- Logging to centralized infra
- Logging to Elastic Stack

- C#
  - Additional Features
    - Smart Enums
      - https://www.youtube.com/watch?v=CEZ6cF8eoeg
  - Plugin Framework
    - https://www.youtube.com/watch?v=g4idDjBICO8
  - Functional Programming
    - Discriminating Unions
      - https://www.youtube.com/watch?v=q_tH3njpAFc
      - OneOf<>: https://www.youtube.com/watch?v=7z-xjijYfcI

- Messaging
  - Kafka
  - RabbitMQ
  - Wolverine
    - https://www.youtube.com/watch?v=p1gsK69m94Y

API Patterns
- Controller Driven
- Minimal API
- Fast API

API Designing
- REST
  - All standards verbs :GET, POST, PUT, DELETE, OPTIONS, HEAD, PATCH, HATEOAS
  - Best Practices: Naming, Versioning, Header etc.,
    - https://www.youtube.com/watch?v=A8t5LSxVJFM
    - https://www.youtube.com/watch?v=HBH6qnj0trU
  - Hypermedia
    - https://www.youtube.com/watch?v=JNuk66FVSM0
  - Concurrency
    - Optimistic Concurrency: Etag
      - https://www.youtube.com/watch?v=2Nk3kCCyu3A&t=538s
- Error Management
  - RFC 9457 - Standard approach to return error information
    - https://www.youtube.com/watch?v=4NfflZilTvk
- Idempotence

Caching
- Http response caching
  - E-tags
- Caching Frameworks
  - Fusion Cache
- Distributed caching with Redis using ICacheProvider
  - Implement cache expiry on time (sliding | fixed), content size, 
  - Distributed cache with Cached Repository

Globalization, Localization
- Localization with resource files
- Database centric resource keys
- Culture configuration and setup

Data Management
- Datastore
  - MySQL, PostgreSQL, MS SQL
  - Redis as primary database
    - https://www.youtube.com/watch?v=GgyizgXwXAg
  - Elasticsearch
  - MongoDB
- CRUD Operations
  - Fast bulk insert operation
    - https://www.youtube.com/watch?v=U6-k0TZL_Sw&t=3s
- Data Validators
  - ASP.NET Core default validation rules
  - Fluent validation rules
- POCO DTO Mapping
  - Use Auto mapper
  - Other Mapper objects
- Design Patterns
  - Repository Pattern
- Secrecy
  - Encrypt data for sensitive fields

Open Telemetry 
- Signals - Traces, Metrics and Logs
- Implementation, with Aspire, Grafana, Prometheus
  - https://www.youtube.com/watch?v=HrRrJ5wTtdk
  - https://www.youtube.com/watch?v=nFU-hcHyl2s
- Distributed Tracing
  - https://www.milanjovanovic.tech/blog/introduction-to-distributed-tracing-with-opentelemetry-in-dotnet

HealthChecks
- Move health checks to open telemetry
- Custom performance metrics
  - https://www.youtube.com/watch?v=8kDugxr3Hdg

Logging
- Logging with different logging providers
  - Seri log and Log4Net
- Logging with ELK stack

Containerization
- Kubernetes
  - Minikube, Dashboard
  - Deploy apps to Kubernetes
    - https://www.youtube.com/watch?v=E8ilDMg7Dak
- Docker
- Podman
- Azure
  - Aspire Template Deploy to Azure https://www.youtube.com/watch?v=HYe6y1kBuGI

Application Templates
- Microsoft Aspire Template
- DDD Clean Architecture Template

Authentication & Authorization
- https://www.youtube.com/watch?v=4cFhYUK8wnc&list=PLYpjLpq5ZDGtJOHUbv7KHuxtYLk1nJPw5&index=1

- Different type of authentication
  - Cookie
  - Bearer Tokens
  - oAuth
  - SAML
  - Entra ID
  - Key Cloak
- API authentications (Types)
  - JWT
  - Other?

MicroServices Infra
- API Gateway
  - Ocelot
  - C# Name resolution

Service Interfaces
- REST
- gRPC
- WebSockets
- SignalR
- WebHooks
- Message Queues (Kafka, RabbitMQ, etc)

Error and Exceptions
- Efficient way to avoid exceptions and pass errors through result objects
  - https://www.youtube.com/watch?v=WCCkEe_Hy2Y
- Railway oriented programming, efficient way of handling errors
  - https://www.youtube.com/watch?v=C1oGnDEnS14
- Cross cut aspect oriented programming

Architecture Patterns
- DDD
- Clean Architecture
- MVP
- CQRS
- Vertical Slice Architecture
- Aspect Oriented Cross Cuts

Messaging Services
- Mass Transit
- NServiceBus

Testing 
- Load Testing - k6
  - https://www.youtube.com/watch?v=r-Jte8Y8zag
- Performance Testing
  - https://www.youtube.com/watch?v=xlqcT4NSrZw&t=126s
- Benchmarking
  - Benchmark.net https://www.youtube.com/watch?v=5iCUqNS9OdI
- Contract Testing
  - Pact.net Testing

Build Management
- Docker
  - Multistage Dockers