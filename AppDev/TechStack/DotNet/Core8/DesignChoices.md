- Current scope
  - Simple POC, with data entry screens, not much workflows, data retrieval etc.,
  - No discussion on the workflows or business processes

- Delivery model
  - 4 stages
    - Development @Brane
      - Code generation and testing will happen inside Brane environment (on Azure)
      - First demo will be conducted here
      - Defi to provide environmental & configuration details to be replaced at Brane end
      - Azure Level Configuration
        - B2C configuration settings
        - App configuration settings (TBD)
          - app-setting.json or Azure config repo
      - Database
        - Data model, Master data, LOV
        - Sample data or mockup scripts
    - Sandbox @Defi
      - Periodically deployments and testing
      - Access needed from Defi on following aspects
        - Complete environment to deploy
    - QA
      - As close to Defi production environment as possible
      - Deployment can be a joint exercise if Defi want it to be
        - Any challenges on the environmental configuration can be ironed out
      - 
    - Production
      - Completely up to Defi
  - A connection to this Defi will share a detailed pipeline documentation 

- Architecture
  - Application is generated based on the template that are tried and tested
  - Any requirements do not fit into the current template need to be design, developed and tested.
    - Given the timelines we prefer to keep things simple, unless pressing need
  - Architecture document is a standard document talking about the overall architecture outlook
    - Most of the things are significant here
  
  - System Architecture
    - Deployment
      - Well tested Docker file to be provided
        - Rootless docker as per Microsoft recommendations
    - Performance
      - 150 - 200 concurrent users
      - Auto scale provisioning

  - Micro Services (mS) Architecture
    - Solution to be complaint with mS architecture standards
    - Completely containerized as per Microsoft recommendations
    - Current functionality is one micro service, as docker container
    - Integration and testing on the mS fabric on Azure (TBD)
      - API gateway integration
      - fault tolerance, Circuit breakers
  
  - N-Tier Architecture
    - Frontend
      - Razor Page Microsoft Template
      - Keep it simple and pure
      - No mixing of MVC template as MS do not (clearly)recommend it.
      - UI components to be built using vanilla JavaScript
    - API
      - API layer shall be developing following Microsoft's Minimal API template
      - REST API as per OpenAPI 3.0 specification
      - Standard CRUD operations for each of the Domain entities shall be implemented
      - Addition functional API requirements are waited
      - Controller based API (???)
      - Entity centric CRUD API (???)
      - API security standards
        - JWT ???
    - Database
      - PostgreSQL or MS SQL Database
      - Initialization and seeding through SQL Script
      - DB Migration aspects (TBD)
        - Do not recommend as it need different levels of code cleanup and optimization 
  
  - Application Design Patters
    - Standard design practices to be followed, do not prefer over engineering unless you have any specific requirements
  
  - Security
    - OWASP Security (???)
  
  - Quality
    - Static Analysis (TBD)
      - SonarQube, report can be shared
    - Dynamic Analysis (TBD)

- Design
  - Elastic Search, does not see any need
  - Asynchronous functionality, does not see any need
  - Scalability
    - AKS will take care of, application is going to be performant
  - Logging
    - Standard .net 8 core logging services, logging provider can be configured including AzureInsights
    - Additionally log to Azure Monitor - Application Insights
    - OpenTelemetry, Kubernetes with Grafana or Helm are OTEL complaint, beyond that do you have any additional application centric requirements
      - Defi Telemetry architecture needs ???
      - App level telemetry data points to be captured ???
  - Caching
    - Redis, as it is purely form data storage do not see any need for data caching
    - Any frontend caching can be done through azure configuration, I do not see any need for application level caching
  - Globalization / Localization / Internationalization (what is the need?)
    - Keys coming from DB ???
    - Standard design practice is to provide language key-value pairs

- Functional
  - Data model to confirmed
  - Data workflow, business rules are yet to finalized
  - API fn requirements, contracts are yet to finalized
  - Data import functionality
  - Reports and matrices
  - UI Updated Screens
  - UI multiform requirements
    - Responsive Screens
  - Compliance Requirements???
  - Different user roles and permissions