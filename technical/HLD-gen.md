name: generate_high_level_design_doc
version: 1.2
description: Comprehensive high-level design and system architecture document for software projects
output_type: markdown
output_file: high_level_design.md
instructions: |
  DOCUMENT SUITE CONTEXT:
  This prompt generates the HIGH-LEVEL DESIGN DOCUMENT as part of a comprehensive project documentation suite.
  Other documents in the suite include: Project Vision, Elevator Pitch, Requirements, Non-Functional Requirements,
  User Flows & Mockups, Low-Level Design, API Specifications, Business Strategy, Operational Planning, and Glossary.
  
  MAXIMUM COGNITIVE ALLOCATION:
  EXHAUST YOUR FULL PROCESSING CAPACITY on this specific document type. Push every available cognitive resource
  toward creating the most comprehensive, detailed, and architecturally sound high-level design possible.
  Think deeply about system architecture, component interactions, technology trade-offs, and design patterns.
  
  WIKI LINK AUTHORITY:
  You have FULL AUTHORITY to create GitHub Wiki links throughout this document. Create links proactively:
  - OUTBOUND LINKS: Link to more detailed documents (e.g., [[Low-Level-Design]], [[API-Specifications]])
  - INBOUND EXPECTATIONS: Use language that anticipates links from higher-level docs (e.g., "As defined in [[Requirements]]...")
  - CROSS-REFERENCES: Link to related sections in sibling documents (e.g., [[User-Flows#checkout-process]])
  - STUB LINKS: Create links to documents that don't exist yet but should (e.g., [[Database-Schema]], [[Security-Implementation]])
  
  LINK PATTERNS:
  - Use descriptive link text: [[Low-Level-Design#user-service-implementation]]
  - Reference specific sections when relevant: [[API-Specifications#authentication-endpoints]]
  - Create semantic anchors: [[Non-Functional-Requirements#performance-targets]]
  - Link to glossary terms: [[Glossary#microservice]]
  
  AUTONOMOUS EXTRACTION:
  Analyze the complete conversation history to extract all architectural and technical design information. Focus on:
  - Explicit technical decisions (e.g., "We'll use React for the frontend")
  - Constraints (e.g., budget limits, timeline deadlines, compliance requirements)
  - User preferences (e.g., "I prefer a cloud-hosted solution", "Must be mobile-first")
  - Architectural considerations (e.g., "It needs to handle 10,000 users daily", "Real-time updates required")
  - Performance requirements (e.g., response times, uptime expectations)
  - Integration needs (e.g., third-party APIs, existing systems)
  - Security concerns (e.g., data privacy, authentication methods)
  Synthesize these into a cohesive design, filling logical gaps with well-reasoned assumptions.
  
  DECISION DOCUMENTATION:
  - For explicit technical decisions: Document the choice and rationale (e.g., "Chose PostgreSQL for its ACID compliance and team familiarity")
  - For incomplete/undecided items: Mark as "⚠️ DECISION NEEDED" with context (e.g., "⚠️ DECISION NEEDED: SQL vs. NoSQL - need to evaluate scalability trade-offs")
  - For debates/alternatives: Document as "🔄 UNDER CONSIDERATION" with options (e.g., "🔄 UNDER CONSIDERATION: In-memory caching (Redis) vs. distributed caching (Memcached)")
  - For missing critical info: Mark as "📝 REQUIRES SPECIFICATION" (e.g., "📝 REQUIRES SPECIFICATION: Authentication token expiration policy") 
  
  OUTPUT REQUIREMENTS:
  - Maximum depth and detail within the high-level design scope
  - Zero placeholder text - every section must contain substantive content or decision markers
  - Actionable architectural blueprint for development teams
  - Clear cross-references to other documents in the suite
  - Output only the markdown document structure below

output_format: |
  # High-Level Design Document: {{app_name}}
  
  > **Document Suite Status**: ~~Project Vision~~ | ~~Elevator Pitch~~ | ~~Requirements~~ | ~~Non-Functional Requirements~~ | ~~User Flows & Mockups~~ | **HIGH-LEVEL DESIGN** | Low-Level Design | API Specifications | Business Strategy | Operational Planning | Glossary
  
  ## Cross-References & Dependencies
  - **[[Requirements]]**: Core functional requirements that drive this architecture
  - **[[Non-Functional-Requirements]]**: Performance, scalability, and reliability constraints
  - **[[User-Flows-and-Mockups]]**: UI/UX patterns that inform frontend architecture decisions
  - **[[API-Specifications]]**: Detailed endpoint definitions (will expand on the API design outlined here)
  - **[[Low-Level-Design]]**: Implementation details for each component described here
  - **[[Business-Strategy]]**: Business requirements that influence technical decisions
  
  ## Executive Summary
  Brief overview of the application, its primary purpose, target users, and key value proposition.
  
  ## Design Goals & Principles
  List 3-5 core architectural and design principles that guide technical decisions:
  - **[Principle Name]**: Brief explanation and why it matters for this project
  - **[Principle Name]**: Brief explanation and why it matters for this project
  
  ## System Overview
  Describe the system's major components and their interactions. Include:
  - User interaction patterns and entry points
  - Core business logic placement (frontend vs backend)
  - External service integrations
  - Data flow and state management approach
  - Key architectural patterns used (MVC, microservices, etc.)
  
  ## Tech Stack Decision Matrix
  | Layer            | Technology Choice | Justification |
  |------------------|-------------------|---------------|
  | Frontend         |                   |               |
  | Backend/API      |                   |               |
  | Database         |                   |               |
  | Authentication   |                   |               |
  | File Storage     |                   |               |
  | Caching          |                   |               |
  | Hosting/Deploy   |                   |               |
  | Monitoring       |                   |               |
  
  *Guidance*: When selecting technologies, evaluate based on scalability (handles growth), performance (response times), cost (licensing fees), team familiarity (expertise available), and project constraints. Provide a brief justification for each choice based on project requirements extracted from the conversation.
  
  ## Architecture Components
  
  ### Frontend Architecture
  - **Framework & Structure**: Main framework, routing, state management
  - **Key Components**: Major UI components and their responsibilities
  - **Client-Side Logic**: What processing happens in the browser
  - **Performance Considerations**: Bundle size, lazy loading, caching strategies
  
  ### Backend Architecture
  - **API Design**: RESTful/GraphQL structure, versioning strategy
  - **Service Layer**: Business logic organization and key services
  - **Data Access**: ORM/database interaction patterns
  - **Background Jobs**: Async processing, queues, scheduled tasks
  
  ### Data Architecture
  - **Database Schema**: Key entities and relationships
  - **Data Flow**: How data moves through the system
  - **Caching Strategy**: What gets cached and where
  - **Data Validation**: Input validation and data integrity measures
  
  ### External Integrations
  - **Third-Party APIs**: Services integrated and their purposes
  - **Webhooks**: Incoming/outgoing webhook handling
  - **File Processing**: Upload, storage, and processing workflows
  - **Email/Notifications**: Communication systems
  
  ## Security & Compliance
  - **Authentication Flow**: User login/logout process
  - **Authorization**: Role-based access control and permissions
  - **Data Protection**: Encryption, PII handling, data retention
  - **API Security**: Rate limiting, input validation, CORS policies
  
  ## Performance & Scalability
  - **Expected Load**: User base, traffic patterns, peak usage
  - **Scaling Strategy**: Horizontal vs vertical scaling approach
  - **Bottlenecks**: Identified performance constraints and mitigation
  - **Caching Strategy**: Application, database, and CDN caching
  
  ## System Architecture Diagram
  Create a Mermaid diagram that reflects the system's architecture based on the conversation. Include:
  - User interfaces (e.g., web app, mobile app, admin dashboard)
  - APIs (e.g., RESTful endpoints, GraphQL services, WebSocket connections)
  - Core services (e.g., business logic components, microservices)
  - Data stores (e.g., databases, caches, file storage, message queues)
  - External integrations (e.g., payment gateways, third-party APIs, social logins)
  - Relationships (e.g., data flow, dependencies, async communication)
  
  Tailor the diagram to your specific project architecture:
  ```mermaid
  graph TB
    subgraph "User Interface"
      UI[Web App / Mobile App]
    end
    
    subgraph "API Layer"
      API[Application API]
      AUTH[Auth Service]
    end
    
    subgraph "Business Logic"
      BL[Core Services]
      BG[Background Jobs]
    end
    
    subgraph "Data Layer"
      DB[(Primary Database)]
      CACHE[(Cache Layer)]
      FILES[File Storage]
    end
    
    subgraph "External Services"
      EXT1[External API 1]
      EXT2[External API 2]
    end
    
    UI --> API
    API --> AUTH
    API --> BL
    BL --> DB
    BL --> CACHE
    BL --> FILES
    BL --> EXT1
    BL --> EXT2
    BG --> DB
    BG --> EXT1
  ```
  
  ## Data Flow Scenarios
  
  ### Primary User Journey
  Example: User shopping on an e-commerce app
  1. **User Input**: User searches for "headphones"
  2. **Frontend Processing**: UI displays search field and sends query
  3. **API Request**: GET /search?q=headphones
  4. **Backend Processing**: Search service queries database with filters
  5. **Data Operations**: Retrieve product data from database, check inventory
  6. **Response**: JSON list of headphones returned to UI with pagination
  
  *Create a similar flow based on your project's main user interaction*
  
  ### Background Processing Flow
  Example: Order confirmation email
  1. **Trigger**: User completes checkout process
  2. **Queue/Job**: Order ID added to email queue via message broker
  3. **Processing**: Email service generates confirmation using template engine
  4. **Completion**: Email sent via SMTP, delivery status logged in database
  
  *Create a similar flow for your project's background processes*
  
  ## Deployment & Infrastructure
  - **Environment Strategy**: Define dev, staging, and production setups (e.g., "Dev uses SQLite, Production uses PostgreSQL cluster")
  - **CI/CD Pipeline**: Specify tools (e.g., GitHub Actions, Jenkins) and steps (build → test → security scan → deploy)
  - **Infrastructure**: Detail server setup (e.g., AWS EC2, Kubernetes pods), containerization (e.g., Docker, container orchestration)
  - **Monitoring**: Include health checks (uptime monitoring), logging (e.g., ELK stack, CloudWatch), error tracking (e.g., Sentry), and performance metrics (e.g., Prometheus/Grafana)
  
  ## Risk Assessment
  - **Technical Risks**: Example: "Framework deprecation - mitigate by choosing stable, well-supported tools with active communities"
  - **Scalability Risks**: Example: "Traffic spikes during peak usage - mitigate with auto-scaling groups and load balancing"
  - **Security Risks**: Example: "Data breaches exposing user information - mitigate with encryption at rest/transit and regular security audits"
  - **Operational Risks**: Example: "Deployment failures causing downtime - mitigate with blue-green deployments and automated rollback strategies"
  - **Dependency Risks**: Example: "Third-party API outages - mitigate with circuit breakers and fallback mechanisms"
  
  ## Open Architectural Decisions
  Track unresolved design decisions that require further analysis:
  
  ### ⚠️ DECISIONS NEEDED
  - [List any technical decisions that need to be made based on conversation gaps]
  
  ### 🔄 UNDER CONSIDERATION  
  - [List any architectural alternatives or trade-offs being evaluated]
  
  ### 📝 REQUIRES SPECIFICATION
  - [List any missing technical specifications needed for complete architecture]
  
  ## Future Architectural Evolution
  - **Phase 2 Features**: Planned enhancements and their architectural impact (e.g., "Add mobile app support - requires API versioning and responsive backend")
  - **Technology Evolution**: Potential tech stack updates or migrations (e.g., "Migrate to GraphQL from REST for better mobile performance")
  - **Scaling Roadmap**: How the architecture will evolve with growth (e.g., "Move to microservices architecture when reaching 100,000+ daily active users")
  - **Technical Debt**: Identified areas for future refactoring (e.g., "Replace monolithic auth system with dedicated identity service")

usage_note: |
  This prompt is designed for autonomous injection into LLM conversations. Simply paste the entire 
  YAML content into your chat after discussing your project ideas. The LLM will analyze the 
  conversation history and generate a complete high-level design document without requiring 
  additional input or context.
