# 🌟 WikiKit: AI Co-founder's Documentation Engine

> Transform scattered LLM brainstorming into surgical development blueprints

## 🎯 Project Vision

**The Problem**: LLMs generate brilliant ideas during brainstorming but leave you with fragments when you need to build. Context gets lost between conversations, great insights get buried, and "just build it" requests produce generic code instead of precise implementations.

**The Solution**: A systematic documentation suite that captures the full intelligence of your brainstorming sessions and transforms it into implementation-ready blueprints for surgical development.

## 🧠 Core Philosophy: Surgical Development

Instead of asking an LLM to "build an entire app," break it into manageable, well-defined tasks:

1. **"Create the file structure for the `user_management` service as outlined in the LLD."**
2. **"Generate the `user_model.py` and `user_repository.py` files based on the provided SQLAlchemy schema."**
3. **"Write the `auth_controller.py` code. It should handle the `/register` endpoint, accept JSON with `email` and `password`, call `user_service.create_user`, and return a JWT token on success."**

This approach requires **comprehensive documentation** that captures every architectural decision, design pattern, and implementation detail from your brainstorming sessions.

## 🏗️ Architecture: Two-Layer System

### Layer 1: YAML Superprompts (`/tree/main`)
Autonomous prompt injection system for extracting structured knowledge from LLM conversations:

- **Hybrid YAML Format**: Token-efficient structured parameters with markdown output templates
- **Cognitive Pressure Optimization**: Forces LLMs to exhaust processing capacity on specific document types
- **Extraction-Focused**: Transforms conversation intelligence into organized documentation
- **Wiki-Integrated**: Automatic cross-referencing and link generation

### Layer 2: GitHub Wiki Scaffold (`/wikikit.wiki`)
Pre-structured documentation framework that serves as the implementation foundation:

- **Document Suite Integration**: Each document feeds into and references others
- **Implementation-Ready**: Documents detailed enough for precise development requests
- **Cross-Referenced**: Automatic wiki linking creates navigable knowledge graph
- **Version Controlled**: Full documentation history and collaborative editing

## 📊 Current Progress

### ✅ Completed Technical Document Prompts
- **High-Level Design**: System architecture and component interaction specs
- **Low-Level Design**: Implementation blueprints with code patterns and class structures  
- **API Specifications**: Complete endpoint documentation with request/response schemas

### ✅ Completed Planning Document Prompts
- **Product Research & Discovery**: Market intelligence and strategic insight extraction

### 🔄 Sample Wiki Pages Generated
- High-Level Design scaffold with decision markers
- API Specifications example with realistic endpoint structures

## 🎯 Prompt Engineering Breakthroughs

### Core Design Principles
- **Preserves Cognitive Resources**: Focus LLM processing on thorough extraction, not new ideation
- **Maintains Fidelity**: Every insight traceable to conversation content with evidence markers
- **Creates Clean Launch Pads**: Documents enable strategic thinking in downstream processes
- **Avoids Hallucination**: Explicit boundaries between conversation evidence and logical inference

### Key Technical Innovations

#### 1. **Hybrid YAML Architecture**
```yaml
# Token-efficient structured parameters
extraction_targets:
  technical_implementations: "Use bcrypt for password hashing, JWT tokens with 24-hour expiry"
  
# Combined with markdown output templates
output_template: |
  # Document Structure with {{dynamic}} interpolation
```
**Result**: 25-40% token reduction while maintaining human readability

#### 2. **Dynamic Adaptation System**
```yaml
code_adaptation:
  language_detection: "Analyze conversation for tech stack and adapt ALL examples"
  framework_alignment: "Align examples with mentioned frameworks"
```
**Result**: Context-aware documentation that matches project technology choices

#### 3. **Explicit Role Assignment**
```yaml
role_assignment:
  primary_role: "You are an experienced [domain expert]"
  task_context: "Extract and organize [specific type] insights"
```
**Result**: Clear cognitive framework eliminates LLM confusion about analytical perspective

#### 4. **Evidence-Grounded Decision Markers**
```yaml
confidence_markers:
  direct_evidence: "Directly stated in conversation with supporting context"
  pattern_inference: "🔍 PATTERN: Synthesized from multiple conversation points"
  missing_critical_data: "❌ DATA GAP: Critical information not discussed"
```
**Result**: Transparent distinction between conversation facts and analytical inference

## 🚀 Strategic Impact

### For Individual Developers
- **Context Preservation**: Never lose architectural decisions or design rationale
- **Implementation Precision**: Request specific code implementations with full context
- **Knowledge Building**: Accumulate project intelligence across multiple LLM sessions

### For Development Teams  
- **Shared Understanding**: Single source of truth for all technical and strategic decisions
- **Onboarding Acceleration**: New team members get complete project context instantly
- **Cross-Functional Alignment**: Business strategy connects directly to technical implementation

### For Product Development
- **Research Intelligence**: Systematic capture of market insights and user feedback
- **Decision Traceability**: Clear reasoning chain from user needs to technical choices
- **Strategic Continuity**: Product vision remains consistent across development cycles

## 📋 Remaining Work

### 🔄 Priority 1: Core Planning Documents
- [ ] **Technical Feasibility & Architecture Decision Records**
- [ ] **Requirements Documentation** 
- [ ] **Non-Functional Requirements**
- [ ] **User Flows & Mockups**
- [ ] **Project Vision** (enhanced)
- [ ] **Elevator Pitch** (enhanced)

### 🔄 Priority 2: Implementation Support Documents  
- [ ] **Database Design** (extracted from LLD)
- [ ] **Security Architecture** (extracted and expanded)
- [ ] **Testing Strategy** (systematic QA approach)
- [ ] **Development Roadmap** (sprint planning and milestones)

### 🔄 Priority 3: Operational Documents
- [ ] **Deployment & Infrastructure** 
- [ ] **Monitoring & Observability**
- [ ] **Business Strategy** (enhanced)
- [ ] **Go-to-Market Strategy**

### 🔄 Priority 4: Scaffold Wiki Pages
- [ ] Generate scaffold pages for all document types
- [ ] Cross-reference validation and link optimization
- [ ] Template customization for different project types
- [ ] Integration testing with real project scenarios

## 🔬 Advanced Prompt Engineering Challenges

### Solved Challenges ✅
1. **Dynamic Tech Stack Adaptation**: Prompts now detect conversation technology and adapt all examples accordingly
2. **Scope Discipline**: Clear boundaries prevent feature creep and maintain document focus
3. **Evidence Grounding**: Transparent markers distinguish facts from inference
4. **Cognitive Resource Allocation**: LLM processing optimized for extraction over ideation

### Remaining Research Areas 🔬
1. **Data Synthesis vs Extraction Balance**: Optimal blend of conversation mining and expert analysis
2. **Cross-Document Consistency**: Ensuring architectural decisions propagate correctly across documents
3. **Iterative Refinement**: Updating documents as conversations evolve without losing context
4. **Quality Validation**: Automated checking for completeness and internal consistency

## 🛠️ Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/wikikit.git
   cd wikikit
   ```

2. **Choose Your Prompt**
   - Browse `/prompts` directory for document type needed
   - Copy entire YAML content for autonomous injection

3. **Inject Into LLM Conversation**
   - Paste YAML prompt after discussing your project ideas
   - LLM will analyze conversation history and generate structured document

4. **Populate Your Wiki**
   - Copy generated markdown into your project's GitHub wiki
   - Follow cross-references to build complete documentation suite

## 🤝 Contributing

This documentation system evolves through real-world usage. Contributions welcome:

- **Prompt Improvements**: Better extraction patterns and decision markers
- **New Document Types**: Additional document types for specialized needs  
- **Integration Examples**: Real project case studies and implementation patterns
- **Quality Analysis**: Testing prompts against actual development scenarios

## 📄 License

MIT License - Build better software through better documentation.

---

**Status**: Work in Progress | **Next Focus**: Technical Feasibility & ADR prompt development

*"The quality of your documentation determines the precision of your development."*
=======
# 🌟 WikiKit: Transform LLM Conversations into Surgical Development Blueprints

> A systematic approach to capturing conversation intelligence and transforming it into implementation-ready documentation — with zero loss of context

---

## 🎯 The Problem We Solve

You've just spent 3 hours brainstorming with an LLM. You've explored architectures, discussed trade-offs, and made key technical decisions. But now you're left with:

* 💬 Hours of rich discussion — hard to reference later
* 🔍 Key decisions buried in dozens of scattered replies
* 📋 No structured documentation to build from
* 🔄 Critical context lost when the conversation ends

**WikiKit solves this** by providing extraction-focused prompts that transform conversation history into comprehensive, implementation-ready documentation.

---

## 🧠 Core Philosophy: Extraction Over Generation

WikiKit prompts are **information organizers**, not idea generators. They systematically extract and structure the intelligence already present in your conversations, creating documentation so detailed that development becomes surgical:

> Instead of:

```txt
"Build me a user authentication system"
```

> You can say:

```txt
"Implement the JWT-based authentication flow specified in ADR-001,
 using the bcrypt parameters from Security Architecture section 3.2"
```

---

## 📦 What's Inside

### 🎯 Lite Prompts (30-50 lines)

Fast extraction when context windows are tight:

* `technical-decisions-quick.yaml` – Key technology choices
* `feature-list-quick.yaml` – Core functionality summary
* `project-summary-quick.yaml` – Everything in one shot
* *Token-efficient for laggy conversations*

### 📚 Full Prompts (300-500 lines)

Comprehensive documentation with FAANG-level rigor:

* `technical-feasibility-adr.yaml` – Complete ADRs with risk analysis
* `functional-requirements.yaml` – IEEE 830 standard requirements
* `high-level-design.yaml` – System architecture with C4 models
* *Use when you need production-ready documentation*

### 🔧 Shared Components

Reusable patterns ensuring consistency:

* `decision-markers.yaml` – Standardized markers (✅ VERIFIED, ⚠️ RISK, etc.)
* `extraction-patterns.yaml` – Common extraction targets
* `prompt-wizardry.yaml` – Quality activation techniques

### 📑 Document Types Supported

**Planning Phase**
→ Product Research & Discovery
→ Project Vision
→ Elevator Pitch
→ Technical Feasibility & ADRs

**Requirements**
→ Functional Requirements
→ Non-Functional Requirements
→ User Flows & Mockups

**Architecture**
→ High-Level Design
→ Low-Level Design
→ API Specifications
→ Database Design
→ Security Architecture

**Implementation**
→ Development Roadmap
→ Testing Strategy
→ Deployment Infrastructure
→ Monitoring & Observability

**Business**
→ Business Strategy
→ Go-to-Market Strategy

---

## 🎭 Prompt Engineering Techniques

### Pattern Activation

Our prompts use specific phrases to activate high-quality patterns in LLM training data:

* "Principal Software Architect at Netflix/Google/Amazon scale"
* "Following IEEE 830 standards"
* "Production-ready implementation"
* "EXHAUST YOUR FULL PROCESSING CAPACITY"

### Cognitive Framing

* 🧠 **Role Precision**: Not just "engineer" but "senior backend engineer specializing in distributed systems"
* 🏗️ **Quality Context**: "Building for millions of users" vs "building an app"
* 🔍 **Systematic Thinking**: Step-by-step protocols prevent shortcuts

### Evidence Grounding

Every prompt enforces evidence traceability:

```yaml
confidence_markers:
  verified: "✅ VERIFIED: Explicitly stated in conversation"
  derived: "📊 DERIVED: Logically inferred from [specific evidence]"
  gap: "❌ DATA GAP: Critical information not discussed"
```

---

## 🔁 Usage Patterns

### 📈 Progressive Enhancement

```txt
💡 → ✂️ → 🧪 → 🏗️
Lite Prompt → Gap Review → Targeted Prompts → Final Docs
```

### 📤 Post-Conversation Extraction

```txt
🗣️ → ⏹️ → 📦 → 🧱
Natural Chat → Stop → Load Prompts → Doc Suite
```

### 🔁 Iterative Refinement

```txt
📦 → 🔍 → ✏️ → 📦
Extract → Review → Clarify → Re-extract
```

---

## 🗂️ Directory Structure

```txt
wikikit/
├── prompts/
│   ├── full/          # Comprehensive prompts (300-500 lines)
│   ├── lite/          # Quick extraction (30-50 lines)
│   ├── shared/        # Reusable components
│   └── workflows/     # Multi-prompt sequences
├── wiki-scaffolds/    # Example outputs
├── tools/             # Automation utilities
└── docs/              # Guides and philosophy
```

---

## ⚠️ Important Considerations

### Context Window Management

* Full prompts consume 5-10k tokens each
* Use lite prompts when conversation is already long
* Consider starting fresh conversations for each major document

### Quality vs Speed Trade-offs

* **Lite prompts**: Quick insights, may miss nuance
* **Full prompts**: Complete extraction, slower processing
* Choose based on your immediate needs

### Extraction Fidelity

* WikiKit extracts what was discussed, not what should have been
* Gaps in conversation become gaps in documentation
* Use "DATA GAP" markers to identify what needs discussion

---

## 🔬 Advanced Techniques

### Intermediate Extraction

Some prompts support phased extraction:

```yaml
extraction_phases:
  - raw_extraction: "List all mentioned items"
  - organization: "Group into categories"  
  - synthesis: "Generate final document"
```

### Prompt Chaining

Output from one prompt can seed another:

```bash
# 1. Extract requirements
# 2. Feed requirements into technical feasibility
# 3. Use feasibility to guide architecture design
```

### Dynamic Adaptation

Prompts adapt to your tech stack:

* Mention "using React" → Examples use React
* Discuss "PostgreSQL" → SQL examples throughout
* Reference "microservices" → Distributed patterns

---

## 🤝 Contributing

WikiKit improves through real usage. We welcome:

### Prompt Improvements

* Better extraction patterns
* Clearer decision markers
* More efficient token usage

### New Document Types

* Specialized domains (mobile, ML, blockchain)
* Industry-specific compliance docs
* Team process documentation

### Usage Examples

* Successful extraction patterns
* Multi-prompt workflows
* Integration with development tools

---

## 📈 Roadmap

### Near Term
- [ ] Non-Functional Requirements prompt
- [ ] User Flows & Mockups prompt
- [ ] Development Roadmap prompt
- [ ] Testing Strategy prompt
- [ ] Elevator Pitch prompt

### Medium Term
- [ ] Complete remaining full prompts (Database Design, Security Architecture, etc.)
- [ ] Create lite versions for all document types
- [ ] Wiki scaffold templates for each document type
- [ ] Prompt selector tool ("Which prompt do I need?")

### Long Term
- [ ] Shared components library
- [ ] Workflow automation tools
- [ ] CLI tool for prompt injection
- [ ] VSCode/Cursor extension
- [ ] Multi-conversation synthesis

---

## 📄 License

MIT License — Build better software through better documentation.

---

**Status**: Work in Progress | **Next Focus**: Non-Functional Requirements prompt

>*"The quality of your documentation determines the precision of your development."*
>
> <div align="center">— Claude 4 Sonnet</div>
