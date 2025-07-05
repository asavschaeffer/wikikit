name: generate_high_level_design_doc
version: 1.2
description: Comprehensive high-level design and system architecture document for software projects
output_type: markdown
output_file: high_level_design.md
instructions: |
  AUTONOMOUS DOCUMENT GENERATION:
  Analyze the complete conversation history to extract all relevant project details, technical decisions, 
  feature discussions, and architectural considerations mentioned so far. Synthesize this information 
  into a comprehensive high-level design document.
  
  EXTRACTION TARGETS:
  - App name, purpose, and core functionality from any descriptions
  - Technical stack preferences or requirements mentioned
  - User stories, features, or capabilities discussed
  - Performance, scalability, or architectural concerns raised
  - Integration requirements or external services mentioned
  - Security, compliance, or business requirements noted
  
  OUTPUT REQUIREMENTS:
  - Fill every section with specific, concrete information derived from the conversation
  - If certain technical details weren't discussed, make reasonable architectural decisions
  - Provide brief justifications for technology choices based on project requirements
  - Ensure the document serves as a actionable blueprint for development
  - Do not include placeholder text, meta-commentary, or requests for additional information
  - Output only the markdown document structure below

output_format: |
  # High-Level Design Document: {{app_name}}
  
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
  
  ## Future Considerations
  - **Phase 2 Features**: Planned enhancements and their architectural impact
  - **Technology Evolution**: Potential tech stack updates or migrations
  - **Scaling Roadmap**: How the architecture will evolve with growth

usage_note: |
  This prompt is designed for autonomous injection into LLM conversations. Simply paste the entire 
  YAML content into your chat after discussing your project ideas. The LLM will analyze the 
  conversation history and generate a complete high-level design document without requiring 
  additional input or context.
