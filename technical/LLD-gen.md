name: generate_low_level_design_doc
version: 1.0
description: Detailed low-level design and implementation specification for software projects
output_type: markdown
output_file: low_level_design.md
instructions: |
  DOCUMENT SUITE CONTEXT:
  This prompt generates the LOW-LEVEL DESIGN DOCUMENT as part of a comprehensive project documentation suite.
  Other documents in the suite include: Project Vision, Elevator Pitch, Requirements, Non-Functional Requirements,
  User Flows & Mockups, High-Level Design, API Specifications, Business Strategy, Operational Planning, and Glossary.
  
  MAXIMUM COGNITIVE ALLOCATION:
  EXHAUST YOUR FULL PROCESSING CAPACITY on implementation-level architectural details. Push every available 
  cognitive resource toward creating the most comprehensive, detailed, and code-ready design possible.
  Think deeply about class structures, data models, algorithms, design patterns, error handling, and performance optimizations.
  
  SCOPE DISCIPLINE:
  - IN SCOPE: Class diagrams, method signatures, data schemas, algorithms, design patterns, file structures, 
    database design, error handling, validation logic, caching strategies, security implementation
  - OUT OF SCOPE: Business requirements → [[Requirements]], high-level architecture → [[High-Level-Design]], 
    API endpoint definitions → [[API-Specifications]], user interface flows → [[User-Flows-and-Mockups]]
  - REDIRECT out-of-scope items with wiki links to their appropriate documents
  
  WIKI LINK AUTHORITY:
  You have FULL AUTHORITY to create GitHub Wiki links throughout this document. Create links proactively:
  - OUTBOUND LINKS: Link to implementation details (e.g., [[API-Specifications#user-endpoints]], [[Database-Schema]])
  - INBOUND EXPECTATIONS: Reference higher-level docs (e.g., "As specified in [[High-Level-Design#user-service]]...")
  - CROSS-REFERENCES: Link to related implementation sections (e.g., [[Security-Implementation#password-hashing]])
  - STUB LINKS: Create links for detailed specs (e.g., [[Database-Migrations]], [[Unit-Test-Plans]])
  
  LINK PATTERNS:
  - Implementation-specific: [[Database-Schema#user-table]], [[Error-Handling#validation-exceptions]]
  - Code organization: [[File-Structure#service-layer]], [[Design-Patterns#repository-pattern]]
  - Technical details: [[Performance-Optimization#query-caching]], [[Security-Implementation#jwt-validation]]
  
  AUTONOMOUS EXTRACTION:
  Analyze the complete conversation history to extract all implementation-level information. Focus on:
  - Specific technical implementations mentioned (e.g., "Use bcrypt for password hashing")
  - Data structure requirements (e.g., "Users have profiles with multiple addresses")
  - Performance specifications (e.g., "Search results under 200ms", "Handle 1000 concurrent users")
  - Security implementation details (e.g., "JWT tokens with 24-hour expiry")
  - Business logic rules (e.g., "Orders expire after 15 minutes in cart")
  - Integration patterns (e.g., "Webhook retries with exponential backoff")
  - Error handling requirements (e.g., "Graceful degradation when payment service is down")
  - Validation rules (e.g., "Email format validation", "Password complexity requirements")
  Synthesize these into detailed implementation specifications with code-ready precision.
  
  DECISION DOCUMENTATION:
  - For explicit implementation decisions: Document with code examples (e.g., "Use Repository pattern for data access - see UserRepository class below")
  - For incomplete/undecided items: Mark as "⚠️ IMPLEMENTATION NEEDED" with context (e.g., "⚠️ IMPLEMENTATION NEEDED: Caching strategy for user sessions - Redis vs. in-memory")
  - For performance trade-offs: Document as "🔄 OPTIMIZATION PENDING" with options (e.g., "🔄 OPTIMIZATION PENDING: Database indexing strategy - analyze query patterns first")
  - For missing technical specs: Mark as "📝 CODE SPECIFICATION REQUIRED" (e.g., "📝 CODE SPECIFICATION REQUIRED: Error logging format and severity levels")
  
  OUTPUT REQUIREMENTS:
  - Maximum implementation depth with code-ready specifications
  - Include method signatures, class structures, and data schemas
  - Provide specific algorithms and design pattern implementations
  - Zero placeholder text - every section must contain actionable implementation details
  - Create immediate development blueprints for engineering teams
  - Output only the markdown document structure below

usage_note: |
  This prompt is designed for autonomous injection into LLM conversations. Simply paste the entire 
  YAML content into your chat after discussing technical implementation details. The LLM will analyze 
  the conversation history and generate a complete low-level design document without requiring 
  additional input or context.

output_format: |
  # Low-Level Design Document: {{app_name}}
  
  > **Document Suite Status**: ~~[[Project-Vision]]~~ | ~~[[Elevator-Pitch]]~~ | ~~[[Requirements]]~~ | ~~[[Non-Functional-Requirements]]~~ | ~~[[User-Flows-and-Mockups]]~~ | ~~[[High-Level-Design]]~~ | **LOW-LEVEL DESIGN** | [[API-Specifications]] | [[Business-Strategy]] | [[Operational-Planning]] | [[Glossary]]
  
  ## Cross-References & Dependencies
  - **[[High-Level-Design]]**: System architecture and component breakdown that this design implements
  - **[[Requirements]]**: Functional requirements driving these implementation decisions
  - **[[Non-Functional-Requirements]]**: Performance and scalability constraints for implementation
  - **[[API-Specifications]]**: External interface contracts that these components must fulfill
  - **[[Database-Schema]]**: Detailed data model specifications (will expand on entities outlined here)
  - **[[Security-Implementation]]**: Detailed security protocols and implementation patterns
  
  ## Implementation Overview
  Detailed breakdown of how the system architecture translates into concrete code structures, focusing on:
  - Service layer organization and responsibilities
  - Data access patterns and repository implementations
  - Business logic encapsulation and validation strategies
  - Error handling and exception management
  - Performance optimization and caching strategies
  
  ## System Architecture Implementation
  
  ### Service Layer Design
  **Pattern**: Document the architectural pattern used (e.g., Domain-Driven Design, Layered Architecture, Hexagonal Architecture)
  
  #### Core Services
  | Service Name | Responsibilities | Dependencies | Key Methods |
  |--------------|------------------|--------------|-------------|
  |              |                  |              |             |
  
  *Guidance*: List each service with specific responsibilities, what it depends on, and its primary public methods. Include error handling patterns and transaction boundaries.
  
  ### Data Access Layer
  **Pattern**: Repository Pattern / Active Record / Data Mapper
  
  #### Repository Implementations
  ```
  Example: UserRepository interface and implementation structure
  - get_by_id(user_id) -> User | None
  - get_by_email(email) -> User | None  
  - save(user) -> User
  - delete(user_id) -> bool
  - find_by_criteria(filters) -> List[User]
  ```
  
  *Create similar structures for each entity based on conversation requirements*
  
  ## Data Model Implementation
  
  ### Entity Relationships
  Create detailed entity relationship descriptions with:
  - Primary and foreign key relationships
  - Constraint definitions and validation rules
  - Index strategies for performance
  - Migration considerations
  
  ### Database Schema Design
  #### Core Entities
  **User Entity Example:**
  ```sql
  CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    email VARCHAR(255) UNIQUE NOT NULL,
    password_hash VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    email_verified BOOLEAN DEFAULT FALSE,
    last_login TIMESTAMP,
    profile_id INTEGER REFERENCES user_profiles(id)
  );
  
  CREATE INDEX idx_users_email ON users(email);
  CREATE INDEX idx_users_last_login ON users(last_login);
  ```
  
  *Create similar schemas for each entity discussed in the conversation*
  
  ### Data Validation Rules
  - **Input Validation**: Email format, password complexity, field lengths
  - **Business Rules**: Age restrictions, quantity limits, status transitions
  - **Data Integrity**: Referential constraints, check constraints, unique requirements
  
  ## Business Logic Implementation
  
  ### Core Algorithms
  Document specific algorithms needed for business operations:
  
  #### Example: Order Processing Algorithm
  ```
  1. Validate cart items (inventory check, pricing verification)
  2. Calculate totals (subtotal, tax, shipping, discounts)
  3. Process payment (authorization, capture, error handling)
  4. Update inventory (atomic decrement with rollback)
  5. Create order record (with transaction boundaries)
  6. Send confirmation (async with retry logic)
  ```
  
  *Create similar algorithmic breakdowns for your project's core processes*
  
  ### Design Patterns Implementation
  
  #### Factory Pattern Example
  ```python
  class ServiceFactory:
      @staticmethod
      def create_payment_processor(provider: str) -> PaymentProcessor:
          if provider == "stripe":
              return StripeProcessor(api_key=settings.STRIPE_KEY)
          elif provider == "paypal":
              return PayPalProcessor(client_id=settings.PAYPAL_CLIENT_ID)
          else:
              raise UnsupportedPaymentProvider(f"Provider {provider} not supported")
  ```
  
  #### Observer Pattern for Events
  ```python
  class OrderEventManager:
      def __init__(self):
          self.subscribers = []
      
      def subscribe(self, event_type: str, handler: callable):
          self.subscribers.append((event_type, handler))
      
      def publish(self, event_type: str, data: dict):
          for event, handler in self.subscribers:
              if event == event_type:
                  handler(data)
  ```
  
  *Document patterns specific to your project's requirements*
  
  ## Security Implementation Details
  
  ### Authentication Flow
  ```
  1. User Login Request (email/password)
  2. Credential Validation (bcrypt password verification)
  3. JWT Token Generation (with user claims and expiry)
  4. Token Response (secure HTTP-only cookie + CSRF token)
  5. Subsequent Requests (JWT validation middleware)
  6. Token Refresh (sliding expiration or refresh token rotation)
  ```
  
  ### Authorization Implementation
  ```python
  class RoleBasedAccessControl:
      def __init__(self, user: User):
          self.user = user
          self.permissions = self._load_permissions()
      
      def can(self, action: str, resource: str = None) -> bool:
          required_permission = f"{action}:{resource}" if resource else action
          return required_permission in self.permissions
      
      def require(self, action: str, resource: str = None):
          if not self.can(action, resource):
              raise InsufficientPermissions(f"User lacks {action} on {resource}")
  ```
  
  ### Data Protection Measures
  - **Encryption at Rest**: Database field encryption for PII (name, address, phone)
  - **Encryption in Transit**: TLS 1.3 for all API communications
  - **Password Security**: bcrypt with cost factor 12, password history tracking
  - **Session Management**: JWT with 24-hour expiry, secure storage patterns
  
  ## Performance Optimization Strategies
  
  ### Caching Implementation
  ```python
  class CacheManager:
      def __init__(self, redis_client):
          self.redis = redis_client
          self.default_ttl = 3600  # 1 hour
      
      def cache_user_profile(self, user_id: int, profile: dict):
          key = f"user_profile:{user_id}"
          self.redis.setex(key, self.default_ttl, json.dumps(profile))
      
      def get_user_profile(self, user_id: int) -> dict | None:
          key = f"user_profile:{user_id}"
          cached = self.redis.get(key)
          return json.loads(cached) if cached else None
  ```
  
  ### Database Query Optimization
  - **Index Strategy**: Composite indexes for common query patterns
  - **Query Patterns**: N+1 prevention with eager loading
  - **Connection Pooling**: Maximum 20 connections with 5-second timeout
  - **Read Replicas**: Route read-only queries to replica databases
  
  ### Async Processing Design
  ```python
  class TaskQueue:
      def __init__(self, broker_url: str):
          self.celery = Celery('app', broker=broker_url)
      
      @self.celery.task(bind=True, max_retries=3)
      def send_email(self, user_id: int, template: str, context: dict):
          try:
              user = UserRepository.get_by_id(user_id)
              EmailService.send(user.email, template, context)
          except EmailServiceError as exc:
              self.retry(countdown=60 * (2 ** self.request.retries))
  ```
  
  ## Error Handling & Resilience
  
  ### Exception Hierarchy
  ```python
  class ApplicationError(Exception):
      """Base exception for application errors"""
      pass
  
  class ValidationError(ApplicationError):
      """Raised when input validation fails"""
      def __init__(self, field: str, message: str):
          self.field = field
          self.message = message
          super().__init__(f"{field}: {message}")
  
  class BusinessRuleError(ApplicationError):
      """Raised when business rules are violated"""
      pass
  
  class ExternalServiceError(ApplicationError):
      """Raised when external service calls fail"""
      def __init__(self, service: str, status_code: int, message: str):
          self.service = service
          self.status_code = status_code
          super().__init__(f"{service} error ({status_code}): {message}")
  ```
  
  ### Circuit Breaker Implementation
  ```python
  class CircuitBreaker:
      def __init__(self, failure_threshold: int = 5, timeout: int = 60):
          self.failure_threshold = failure_threshold
          self.timeout = timeout
          self.failure_count = 0
          self.last_failure_time = None
          self.state = "CLOSED"  # CLOSED, OPEN, HALF_OPEN
      
      def call(self, func, *args, **kwargs):
          if self.state == "OPEN":
              if time.time() - self.last_failure_time > self.timeout:
                  self.state = "HALF_OPEN"
              else:
                  raise CircuitBreakerOpenError("Service unavailable")
          
          try:
              result = func(*args, **kwargs)
              self._on_success()
              return result
          except Exception as e:
              self._on_failure()
              raise
  ```
  
  ### Retry Mechanisms
  - **Exponential Backoff**: 1s, 2s, 4s, 8s, 16s maximum intervals
  - **Jitter**: Random delay up to 20% to prevent thundering herd
  - **Dead Letter Queue**: Failed messages after max retries
  - **Idempotency**: All operations designed to be safely retryable
  
  ## File Structure & Organization
  
  ### Project Structure
  ```
  src/
  ├── controllers/          # HTTP request handlers
  │   ├── auth_controller.py
  │   ├── user_controller.py
  │   └── order_controller.py
  ├── services/             # Business logic layer
  │   ├── auth_service.py
  │   ├── user_service.py
  │   └── order_service.py
  ├── repositories/         # Data access layer
  │   ├── user_repository.py
  │   └── order_repository.py
  ├── models/              # Data models and entities
  │   ├── user.py
  │   └── order.py
  ├── utils/               # Shared utilities
  │   ├── validation.py
  │   ├── encryption.py
  │   └── cache.py
  ├── middleware/          # Request/response middleware
  │   ├── auth_middleware.py
  │   └── error_handler.py
  └── config/              # Configuration management
      ├── database.py
      └── settings.py
  ```
  
  ### Module Dependencies
  Create dependency graphs showing:
  - Controller → Service → Repository → Model flow
  - Circular dependency prevention strategies
  - Interface definitions for dependency injection
  
  ## Testing Strategy Implementation
  
  ### Unit Test Patterns
  ```python
  class TestUserService:
      def setup_method(self):
          self.user_repo = Mock(spec=UserRepository)
          self.email_service = Mock(spec=EmailService)
          self.user_service = UserService(self.user_repo, self.email_service)
      
      def test_create_user_success(self):
          # Arrange
          user_data = {"email": "test@example.com", "password": "secure123"}
          self.user_repo.get_by_email.return_value = None
          self.user_repo.save.return_value = User(id=1, email="test@example.com")
          
          # Act
          result = self.user_service.create_user(user_data)
          
          # Assert
          assert result.id == 1
          self.user_repo.save.assert_called_once()
          self.email_service.send_welcome.assert_called_once()
  ```
  
  ### Integration Test Patterns
  - **Database Integration**: Test repository implementations with real database
  - **API Integration**: Test controller endpoints with test client
  - **External Service**: Test with mock external services and contract tests
  
  ## Implementation Decision Log
  
  ### ⚠️ IMPLEMENTATION NEEDED
  - [List any technical implementation decisions that need to be made]
  
  ### 🔄 OPTIMIZATION PENDING  
  - [List any performance optimizations being evaluated]
  
  ### 📝 CODE SPECIFICATION REQUIRED
  - [List any missing technical specifications needed for implementation]
  
  ## Performance Targets & Monitoring
  
  ### Response Time Targets
  - **API Endpoints**: 95th percentile under 200ms
  - **Database Queries**: Individual queries under 50ms
  - **Cache Operations**: Under 5ms for Redis operations
  - **Background Jobs**: Email delivery within 30 seconds
  
  ### Monitoring Implementation
  ```python
  class PerformanceMonitor:
      def __init__(self, metrics_client):
          self.metrics = metrics_client
      
      def time_operation(self, operation_name: str):
          def decorator(func):
              def wrapper(*args, **kwargs):
                  start_time = time.time()
                  try:
                      result = func(*args, **kwargs)
                      self.metrics.histogram(f"{operation_name}.duration", 
                                           time.time() - start_time)
                      self.metrics.increment(f"{operation_name}.success")
                      return result
                  except Exception as e:
                      self.metrics.increment(f"{operation_name}.error")
                      raise
              return wrapper
          return decorator
  ```
  
  ## Deployment Implementation Details
  
  ### Database Migration Strategy
  ```python
  class Migration_001_CreateUsers:
      def up(self):
          return """
          CREATE TABLE users (
              id SERIAL PRIMARY KEY,
              email VARCHAR(255) UNIQUE NOT NULL,
              password_hash VARCHAR(255) NOT NULL,
              created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
          );
          CREATE INDEX idx_users_email ON users(email);
          """
      
      def down(self):
          return "DROP TABLE users;"
  ```
  
  ### Configuration Management
  ```python
  class Settings:
      def __init__(self):
          self.database_url = os.getenv("DATABASE_URL", "postgresql://localhost/app")
          self.redis_url = os.getenv("REDIS_URL", "redis://localhost:6379")
          self.jwt_secret = os.getenv("JWT_SECRET_KEY")
          self.email_api_key = os.getenv("EMAIL_API_KEY")
          
          # Validate required settings
          if not self.jwt_secret:
              raise ConfigurationError("JWT_SECRET_KEY environment variable required")
  ```
  
  ### Health Check Implementation
  ```python
  class HealthCheckController:
      def __init__(self, db_pool, redis_client):
          self.db = db_pool
          self.redis = redis_client
      
      async def health_check(self):
          checks = {
              "database": await self._check_database(),
              "redis": await self._check_redis(),
              "external_apis": await self._check_external_services()
          }
          
          all_healthy = all(checks.values())
          status_code = 200 if all_healthy else 503
          
          return {"status": "healthy" if all_healthy else "unhealthy", 
                  "checks": checks}, status_code
  ```
