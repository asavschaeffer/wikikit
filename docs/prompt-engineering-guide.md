# Prompt Engineering Guide: WikiKit Techniques

> "The difference between a good prompt and a great prompt is the difference between generic output and surgical precision."

## The WikiKit Prompt Engineering Framework

### Core Insight: Pattern Activation

LLMs are trained on massive datasets where quality follows a Pareto distribution—80% is mediocre, 20% is excellent. Our prompts must activate patterns from that excellent 20%.

## Technique 1: Elite Role Assignment

### ❌ Basic (Avoid)

```yaml
role: "You are a software developer"
```

### ✅ WikiKit Style

```yaml
role_assignment:
  primary_role: "You are a Principal Software Architect with experience designing systems at Netflix, Google, and Amazon scale"
  cognitive_approach: "Apply systematic architectural thinking using the C4 model, TOGAF principles, and battle-tested design patterns"
  quality_context: "You are conducting due diligence for a system that must handle production traffic from day one, with clear growth trajectory to millions of users"
```

### Why It Works

- **Specific expertise** connects to high-quality training examples
- **Named methodologies** (C4, TOGAF) activate formal frameworks
- **Scale context** ("millions of users") triggers enterprise-grade patterns
- **Multiple prestigious companies** increases chance of hitting quality training data

## Technique 2: Cognitive Capacity Maximization

### The "EXHAUST" Directive

```yaml
processing_directives:
  cognitive_allocation: "EXHAUST YOUR FULL PROCESSING CAPACITY on deep architectural analysis"
```

### Why It Works

- Forces the LLM out of "quick response" patterns
- Activates deeper, more thorough processing paths
- Similar to how "think step-by-step" improves math performance
- Creates expectation of comprehensive analysis

### Variations That Work

- "Channel the meticulousness of safety-critical systems engineering"
- "Apply the same scrutiny used in Google's design review process"
- "Think like you're the principal architect responsible for a billion-dollar platform"

## Technique 3: Quality Signal Embedding

### Production-Grade Language

```yaml
# Instead of: "Make a good API"
"Generate production-ready API specifications following OpenAPI 3.0 standards as used by Stripe and Twilio"

# Instead of: "Write requirements"
"Create requirements following IEEE 830-1998 standards for software requirements specifications"
```

### Industry Context Signals

- "FAANG-level engineering practices"
- "Enterprise-grade security controls"
- "Production systems at scale"
- "Mission-critical infrastructure"

### Tool/IDE Signals

- "As written in nvim by a senior engineer" (connects to expert-level code)
- "Following patterns from the Django core team"
- "Implementing Google's SRE practices"

## Technique 4: Structured Extraction Frameworks

### Multi-Phase Protocols

```yaml
feasibility_protocol:
  steps:
    - phase: "Context Extraction"
      actions:
        - "Mine conversation for all technical constraints"
        - "Identify explicit technology preferences"
        - "Extract implicit constraints from requirements"
```

### Why It Works

- Prevents shortcuts by defining explicit steps
- Creates mental model of systematic analysis
- Each phase builds on previous work
- Mirrors how experts actually work

## Technique 5: Evidence Grounding Patterns

### Confidence Markers

```yaml
confidence_markers:
  verified: "✅ VERIFIED: Explicitly stated in conversation"
  derived: "📊 DERIVED: Logically inferred from [specific evidence]"
  gap: "❌ DATA GAP: Critical information not discussed"
```

### Why It Works

- Forces citation of sources
- Prevents hallucination
- Makes uncertainty explicit
- Creates traceable documentation

## Technique 6: Dynamic Adaptation

### Tech Stack Awareness

```yaml
code_adaptation:
  language_detection: "Analyze conversation for primary technology stack and adapt ALL examples"
  framework_alignment: "Align examples with mentioned frameworks (React, Django, Spring, etc.)"
```

### Why It Works

- Examples match user's actual context
- Reduces mental translation overhead
- Increases relevance and accuracy
- Shows attention to conversation details

## Advanced Techniques

### 1. Expertise Stacking

```yaml
"Channel the expertise of:
- Martin Fowler for architectural patterns
- Kent Beck for code quality
- Leslie Lamport for distributed systems
- The Google SRE team for operations"
```

### 2. Anti-Pattern Warnings

```yaml
"Avoid the common pitfalls seen in failed projects:
- Over-engineering (enterprise fizzbuzz)
- Under-specifying (hope-driven development)
- Cargo-culting (copy-paste architecture)"
```

### 3. Reference Anchoring

```yaml
"Following the architectural rigor seen in:
- Uber's microservice migration
- Netflix's chaos engineering
- Amazon's service-oriented architecture"
```

### 4. Cognitive Priming

```yaml
"Before beginning, take a moment to:
- Consider the full conversation context
- Identify key architectural decisions
- Map technical constraints to solutions
- Plan your extraction approach"
```

## Prompt Debugging Techniques

### When Outputs Are Too Generic

- Add more specific role context
- Include named methodologies or standards
- Reference specific companies or projects
- Add scale or complexity indicators

### When Outputs Miss Information

- Break into multiple extraction phases
- Add explicit extraction targets
- Include "look for X, Y, Z" instructions
- Use multi-pass approaches

### When Outputs Hallucinate

- Strengthen evidence requirements
- Add citation instructions
- Include "only from conversation" constraints
- Use confidence markers

## The WikiKit Prompt Formula

```yaml
[Elite Role Assignment]
+ [Cognitive Capacity Directive]
+ [Quality Signal Embedding]
+ [Structured Extraction Framework]
+ [Evidence Grounding Requirements]
+ [Dynamic Adaptation Rules]
= WikiKit Prompt
```

## Examples of Prompt Evolution

### Version 1 (Basic)

```yaml
instructions: "Extract technical decisions from the conversation"
```

### Version 2 (Improved)

```yaml
instructions: "As a senior architect, extract all technical decisions with rationale"
```

### Version 3 (WikiKit Level)

```yaml
role_assignment:
  primary_role: "You are a Principal Software Architect with experience at FAANG companies"

processing_directives:
  cognitive_allocation: "EXHAUST YOUR FULL PROCESSING CAPACITY on systematic extraction"

extraction_protocol:
  steps: [detailed multi-phase approach]

evidence_requirements:
  citation: "Every decision must reference conversation source"
```

## Measuring Prompt Effectiveness

### Quality Indicators

- **Specificity**: Outputs reference actual conversation content
- **Completeness**: All relevant information extracted
- **Organization**: Logical structure emerges from chaos
- **Traceability**: Clear links from output to source
- **Gap Detection**: Missing information explicitly noted

### Red Flags

- Generic advice not tied to conversation
- Missing obvious decisions from chat
- Hallucinated details not discussed
- Poor organization or structure
- No gap identification

## Future Directions in Prompt Engineering

### Emerging Patterns

1. **Prompt Chains**: Output of one feeds the next
2. **Conditional Branches**: Different paths based on extraction results
3. **Meta-Prompts**: Prompts that generate prompts
4. **Validation Loops**: Self-checking extractions

### Research Areas

- Optimal prompt length vs. effectiveness
- Role assignment impact measurement
- Extraction fidelity optimization
- Cross-model prompt portability

## Prompt Engineering Principles

1. **Specificity beats brevity**
2. **Structure enables accuracy**
3. **Evidence prevents hallucination**
4. **Expertise activation improves quality**
5. **Systematic approaches reduce misses**
6. **Clear boundaries prevent scope creep**

---

_Great prompts aren't just instructions—they're cognitive frameworks that guide LLMs to their best performance. Master these techniques, and your extractions will consistently achieve surgical precision._
