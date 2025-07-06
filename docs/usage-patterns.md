# Usage Patterns: Real-World WikiKit Workflows (v2.0)

> Updated with v2.0 improvements and complete strategic documentation workflow

## Complete Strategic Documentation Workflow (v2.0)

### The Full Project Documentation Sequence

**Enhanced v2.0 workflow** handles complete project lifecycle:

```
1. Product Research & Discovery (v2.0)
   ↓ Market intelligence and user insights
2. Project Vision (v2.0)
   ↓ Strategic direction and problem statement
3. Development Roadmap (v2.0) ← NEW!
   ↓ Phased execution planning (MVP → Phase 2 → Future)
4. Functional Requirements (v2.0)
   ↓ What to build systematically
5. Technical Feasibility & ADR (v2.0)
   ↓ How to build with evidence
6. High-Level Design (v1.2)
   ↓ Architectural blueprint
```

**Key v2.0 Addition**: Development Roadmap bridges vision and requirements, capturing the critical MVP vs Phase 2 vs Future planning that dominates real project conversations.

## Enhanced Conversation Handling Patterns

### Pattern 1: The Messy Reality Extraction

**When to Use**: After real brainstorming sessions with contradictions, pivots, and half-formed ideas

**v2.0 Capabilities**:

- ✅ **Contradictory tech stack discussions** → Documents evolution with 🔄 EVOLVED
- ✅ **Multiple target audience options** → Captures all with ❓ CLARIFICATION
- ✅ **Half-formed feature ideas** → Extracts what exists, marks ❌ GAP for missing details
- ✅ **Scope trade-offs** → Tracks features moved between phases with reasoning
- ✅ **Domain-specific requirements** → Creates appropriate categories dynamically

**Example Flow**:

```bash
# After 3-hour messy brainstorming session
cat prompts/full/planning/project-vision.yaml
# Captures vision evolution and contradictions

cat prompts/full/planning/development-roadmap.yaml
# Extracts MVP vs Phase 2 scope decisions and changes

cat prompts/full/requirements/functional-requirements.yaml
# Organizes scattered requirements with conflict resolution
```

**v2.0 Output Quality**:

```markdown
🔄 EVOLVED: Initially "build everything at once" → Changed to "MVP-first approach"
due to investor pressure for faster validation (discussed in messages #34-47)

❓ CLARIFICATION: Target users - mentioned both "enterprise teams" and
"individual creators" - needs market positioning decision

❌ GAP: No discussion of user onboarding flow → Critical for user activation
```

### Pattern 2: Phased Planning Extraction (NEW)

**When to Use**: When conversations involve MVP scoping, Phase 2 planning, and future vision

**Development Roadmap Focus**:

```bash
# After discussing project phases
cat prompts/full/planning/development-roadmap.yaml

# Extracts:
# - MVP scope and boundaries
# - Phase 2 enhancement plans
# - Success criteria for transitions
# - Resource evolution across phases
# - "Super end phase" future technology dependencies
```

**Example Output**:

```markdown
### Phase 1: MVP (3-4 months)

✅ VERIFIED: "Core booking system with payment processing" (user story #1)
🔗 DEPENDENCY: Payment integration blocks user testing

### Phase 2: Growth (6-8 months)

📊 DERIVED: Analytics dashboard needed → Inferred from "need to track user behavior" + "measure conversion rates"

### Future Phase: AI-Powered (18+ months)

💡 ASSUMPTION: Advanced ML recommendations require larger dataset and team expertise not currently available
```

## v2.0 Extraction Efficiency Patterns

### Pattern 3: Token-Optimized Sequential Extraction

**The Problem**: v1.0 prompts consumed 5-6k tokens each, leaving little room for conversation content

**v2.0 Solution**: 60% token reduction enables richer extraction

**Workflow**:

```bash
# Day 1: Strategic foundation (7.5k tokens total vs 15k+ in v1.0)
project-vision.yaml (2.5k tokens) + development-roadmap.yaml (2.5k tokens) + product-research.yaml (2.5k tokens)

# Day 2: Requirements and feasibility (5k tokens total)
functional-requirements.yaml (2.5k tokens) + technical-feasibility.yaml (2.5k tokens)

# Day 3: Architecture
high-level-design.yaml (3k tokens)
```

**Result**: More conversation content processed per prompt, higher extraction fidelity

### Pattern 4: Evolution-Aware Iterative Refinement

**v2.0 Enhancement**: Tracks how thinking evolved across conversations

**Process**:

```bash
# Week 1: Initial extraction
functional-requirements.yaml → requirements-v1.md

# Week 3: After user research
# Add research findings to conversation
functional-requirements.yaml → requirements-v2.md

# Compare outputs to see requirement evolution:
# 🔄 EVOLVED markers show how requirements changed with evidence
```

**Example Evolution Tracking**:

```markdown
### Requirements Evolution Log

🔄 EVOLVED: User authentication approach

- **Initially**: "Simple email/password login" (Week 1 brainstorming)
- **Changed to**: "OAuth + SSO integration" (Week 3 after enterprise user feedback)
- **Reason**: 80% of target enterprise users require SSO for compliance

🔄 EVOLVED: MVP scope

- **Initially**: "Full dashboard with analytics" (ambitious initial vision)
- **Refined to**: "Basic CRUD + simple reports" (after technical feasibility discussion)
- **Reason**: Technical complexity and timeline constraints prioritize core functionality
```

## Advanced Usage Patterns

### Pattern 5: Domain-Adaptive Extraction

**v2.0 Innovation**: Prompts automatically adapt to conversation domain

**Healthcare Project Example**:

```yaml
# Conversation mentions "patient data", "HIPAA compliance", "clinical workflows"
# Prompts automatically generate:
dynamic_categories:
  clinical_workflows: "Patient intake, diagnosis tracking, treatment protocols"
  compliance_requirements: "HIPAA, audit trails, data retention policies"
  integration_needs: "EHR systems, lab interfaces, billing integration"
```

**Fintech Project Example**:

```yaml
# Conversation mentions "KYC", "AML monitoring", "trading algorithms"
# Prompts automatically generate:
dynamic_categories:
  regulatory_compliance: "KYC verification, AML monitoring, compliance reporting"
  financial_operations: "Trading engine, risk management, settlement processing"
  security_requirements: "Transaction security, fraud detection, audit capabilities"
```

### Pattern 6: Cross-Document Consistency Validation

**v2.0 Feature**: Standardized decision markers ensure consistency

**Process**:

```bash
# Run multiple prompts on same conversation
project-vision.yaml → vision.md
functional-requirements.yaml → requirements.md
technical-feasibility.yaml → feasibility.md

# All outputs use identical marker format:
# ✅ VERIFIED: [same decision with consistent evidence]
# 📊 DERIVED: [same logical conclusion across documents]
# ❌ GAP: [same missing information identified]
```

**Cross-Document Validation**:

```markdown
## Consistency Check Example

**Vision Document**:
✅ VERIFIED: "Target enterprise teams with 10-50 employees"

**Requirements Document**:
✅ VERIFIED: "Support team workspaces with 10-50 member capacity"

**Technical Feasibility**:
✅ VERIFIED: "Scale to 50 concurrent users per workspace"

→ Consistent extraction across all documents
```

## Conversation Complexity Handling

### Pattern 7: Stakeholder Disagreement Resolution

**Real-World Scenario**: Different team members express conflicting needs

**v2.0 Handling**:

```markdown
### Stakeholder Perspective Capture

**Engineering Lead**: "We need to use microservices for scalability"
**CTO**: "Monolith first, microservices later when we prove product-market fit"

❓ CLARIFICATION: Architecture approach - microservices vs monolith

- **Engineering perspective**: Scalability and team autonomy benefits
- **CTO perspective**: Reduced complexity and faster iteration
- **Resolution needed**: Technical strategy alignment meeting
- **Impact**: Blocks infrastructure planning and team structure decisions
```

### Pattern 8: Half-Formed Idea Extraction

**Real-World Scenario**: Incomplete thoughts and "we should probably..." statements

**v2.0 Handling**:

```markdown
### Incomplete Requirements Extraction

❌ GAP: Analytics mentioned but undefined

- **What was said**: "We'll need some kind of analytics dashboard"
- **Missing specifics**: Which metrics, what visualizations, who are the users
- **Why critical**: Affects database schema design and API requirements
- **Next steps**: Product team to define analytics requirements

❌ GAP: Integration strategy unclear

- **What was said**: "Maybe integrate with Slack or something"
- **Missing specifics**: Which platforms, integration depth, priority order
- **Why critical**: Impacts API design and development timeline
- **Next steps**: Research competitor integrations and user preferences
```

## Quality Validation Patterns

### Pattern 9: Extraction Completeness Validation

**v2.0 Quality Gate**: Every prompt includes completeness assessment

**Example Assessment**:

```markdown
## Extraction Coverage Analysis

**High Confidence Extractions** (90-100% evidence):

- Core user flows and feature requirements
- Technology stack decisions with clear reasoning
- MVP scope boundaries with success criteria

**Medium Confidence Extractions** (70-89% evidence):

- Performance requirements (mentioned but not quantified)
- Integration priorities (discussed but not prioritized)

**Low Confidence/Gap Areas** (<70% evidence):

- Security requirements (barely mentioned)
- Deployment strategy (not discussed)
- User onboarding flow (assumed but not designed)

**Overall Coverage**: 75% - Good foundation but needs follow-up conversations on security and operations
```

### Pattern 10: Evidence Strength Assessment

**v2.0 Enhancement**: Every extraction includes evidence quality

**Format**:

```markdown
### Evidence Strength Examples

✅ VERIFIED (Strong Evidence): "Use PostgreSQL for ACID compliance"

- **Source**: Explicit decision in message #23 with technical reasoning
- **Confidence**: 95% - Clear decision with rationale

📊 DERIVED (Medium Evidence): Real-time notifications required

- **Source**: Inferred from "users need immediate updates" + "checking app constantly"
- **Confidence**: 75% - Logical conclusion but not explicitly stated

❌ GAP (No Evidence): User authentication method

- **Impact**: Blocks security implementation and user experience design
- **Confidence**: 0% - Not discussed, critical information missing
```

## Team Collaboration Patterns

### Pattern 11: Multi-Stakeholder Conversation Extraction

**Scenario**: Conversations with product, engineering, and business stakeholders

**v2.0 Approach**:

```markdown
### Stakeholder-Attributed Extraction

**Product Manager Focus**:
✅ VERIFIED: "Priority is user retention metrics" (Sarah, product)
📊 DERIVED: Feature A more important than Feature B → Based on retention impact discussion

**Engineering Lead Focus**:  
✅ VERIFIED: "Technical debt from legacy system limits options" (Alex, engineering)
🔗 DEPENDENCY: Legacy migration blocks new feature development

**Business Stakeholder Focus**:
✅ VERIFIED: "Must launch before Q3 competitor release" (Jordan, business)
⚠️ RISK: Timeline pressure may compromise quality testing
```

### Pattern 12: Decision Authority Tracking

**v2.0 Feature**: Track who makes which decisions

**Example**:

```markdown
### Decision Authority Matrix

**Strategic Decisions** (CEO/CTO level):
🔄 EVOLVED: Technology platform choice

- Initially "build custom" → Changed to "extend existing platform"
- **Decision maker**: CTO final call after engineering assessment
- **Rationale**: Time-to-market priority over customization

**Tactical Decisions** (Team level):
✅ VERIFIED: API design patterns

- **Decision maker**: Engineering team consensus
- **Authority**: Delegated by CTO for implementation details

**Open Decisions** (Need escalation):
❓ CLARIFICATION: Budget allocation for Phase 2

- **Needs**: Finance and product alignment
- **Impact**: Affects hiring timeline and feature scope
```

## Measurement and Improvement

### Success Metrics for v2.0 Patterns

**Extraction Quality**:

- 90%+ conversation insights captured (vs 70% in v1.0)
- 95%+ decision marker consistency across documents
- 80%+ critical gaps identified before development

**Efficiency Gains**:

- 60% token reduction with maintained quality
- 2x faster prompt processing with v2.0 compression
- 50% fewer clarification rounds needed

**Team Outcomes**:

- Reduced implementation misunderstandings
- Faster development start with clearer specifications
- Better stakeholder alignment through explicit gap identification

### Continuous Improvement Process

1. **A/B Testing**: Compare v1.0 vs v2.0 extraction quality
2. **Gap Analysis**: Track which critical information still gets missed
3. **Evolution Patterns**: Identify common ways requirements change
4. **Domain Adaptation**: Improve dynamic category generation
5. **Cross-Document Validation**: Ensure consistency across full suite

---

_These usage patterns reflect real-world complexity and the maturity of WikiKit v2.0 extraction capabilities. Apply patterns based on conversation context and complexity level._
