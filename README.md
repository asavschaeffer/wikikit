# 🌟 WikiKit: Transform LLM Conversations into Surgical Development Blueprints

> A systematic approach to capturing conversation intelligence and transforming it into implementation-ready documentation

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

* Full prompts consume 1-3k tokens each
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

**Status**: Work in Progress | **Next Focus**: Improve LLD prompt to avoid overengineering

>*"The quality of your documentation determines the precision of your development."*
>
> <div align="center">— Claude 4 Sonnet</div>
