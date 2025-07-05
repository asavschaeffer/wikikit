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
  
  SCOPE DISCIPLINE:
  - IN SCOPE: System architecture, component design, technology stack, data flow, integration patterns
  - OUT OF SCOPE: Detailed requirements (→ Requirements doc), business strategy (→ Business Strategy doc), 
    user interface details (→ User Flows & Mockups doc), API endpoints (→ API Specifications doc)
  - REDIRECT out-of-scope items to their appropriate documents with clear references
  
  AUTONOMOUS EXTRACTION:
  Analyze the complete conversation history to extract all architectural and technical design information.
  Extract every technical detail, constraint, preference, and architectural consideration mentioned.
  
  DECISION DOCUMENTATION:
  - For explicit technical decisions: Document the choice and rationale
  - For incomplete/undecided items: Mark as "⚠️ DECISION NEEDED" with context
  - For debates/alternatives: Document as "🔄 UNDER CONSIDERATION" with options
  - For missing critical info: Mark as "📝 REQUIRES SPECIFICATION" 
  
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
  - **Requirements Document**: Core functional requirements that drive this architecture
  - **Non-Functional Requirements**: Performance, scalability, and reliability constraints
  - **User Flows & Mockups**: UI/UX patterns that inform frontend architecture decisions
  - **API Specifications**: Detailed endpoint definitions (will expand on the API design outlined here)
  - **Low-Level Design**: Implementation details for each component described here
  - **Business Strategy**: Business requirements that influence technical decisions
  
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
  1. **User Input**: Description of main user action
  2. **Frontend Processing**: What happens in the UI
  3. **API Request**: What gets sent to backend
  4. **Backend Processing**: Server-side logic and validations
  5. **Data Operations**: Database reads/writes
  6. **Response**: What gets returned to user
  
  ### Background Processing Flow
  1. **Trigger**: What initiates background processing
  2. **Queue/Job**: How work gets queued and processed
  3. **Processing**: What happens during background execution
  4. **Completion**: How results are stored/communicated
  
  ## Deployment & Infrastructure
  - **Environment Strategy**: Dev, staging, production setup
  - **CI/CD Pipeline**: Build, test, and deployment process
  - **Infrastructure**: Server architecture, containerization, orchestration
  - **Monitoring**: Health checks, logging, error tracking, metrics
  
  ## Risk Assessment
  - **Technical Risks**: Potential technical challenges and mitigation strategies
  - **Scalability Risks**: Growth-related concerns and solutions
  - **Security Risks**: Main security considerations and protections
  - **Operational Risks**: Deployment, maintenance, and support challenges
  
  ## Open Architectural Decisions
  Track unresolved design decisions that require further analysis:
  
  ### ⚠️ DECISIONS NEEDED
  - [List any technical decisions that need to be made based on conversation gaps]
  
  ### 🔄 UNDER CONSIDERATION  
  - [List any architectural alternatives or trade-offs being evaluated]
  
  ### 📝 REQUIRES SPECIFICATION
  - [List any missing technical specifications needed for complete architecture]
  
  ## Future Architectural Evolution
  - **Phase 2 Features**: Planned enhancements and their architectural impact
  - **Technology Evolution**: Potential tech stack updates or migrations
  - **Scaling Roadmap**: How the architecture will evolve with growth

usage_note: |
  This prompt is designed for autonomous injection into LLM conversations. Simply paste the entire 
  YAML content into your chat after discussing your project ideas. The LLM will analyze the 
  conversation history and generate a complete high-level design document without requiring 
  additional input or context.
