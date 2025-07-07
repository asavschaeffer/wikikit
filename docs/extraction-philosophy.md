# Extraction Philosophy: The WikiKit Way

> "LLMs are brilliant conversationalists but terrible archivists. WikiKit bridges that gap through surgical extraction discipline."

## Core Principle: Extraction Over Generation

The fundamental insight behind WikiKit is that LLM conversations already contain all the intelligence needed for comprehensive documentation. The challenge isn't generating new ideas—it's **systematically extracting and organizing what was actually discussed**.

🔄 **EVOLVED**: v2.0 Enhancement - Conversation Reality Handling

**Initially**: Assumed conversations were coherent, logical progressions  
**Changed to**: Handle messy reality of real conversations with contradictions, pivots, and half-formed ideas  
**Reason**: Real project conversations involve stakeholder disagreements, scope changes, and evolving understanding that must be captured systematically rather than forced into artificial coherence

Real conversations now handled include:

- **Contradictions and pivots**: "Actually, let's use React instead of Vue"
- **Half-formed ideas**: "We need some kind of analytics dashboard"
- **Scope trade-offs**: Moving features between MVP and Phase 2
- **Stakeholder disagreements**: Different team members wanting different approaches
- **Evolution over time**: Decisions changing as new information emerges

## The Three Pillars

### 1. Evidence Grounding

Every piece of extracted information must be traceable to the conversation:

```yaml
✅ VERIFIED: "We decided to use PostgreSQL" (with reasoning about ACID compliance)
📊 DERIVED: Real-time updates needed → Inferred from "data must always be current" + "users check hourly"
❌ GAP: No discussion of backup strategy
```

🔄 **EVOLVED**: v2.0 Enhancement - Evolution Tracking

**Added**: `🔄 EVOLVED` marker to capture how decisions changed throughout conversation
**Format**: `🔄 EVOLVED: Initially [X] → Changed to [Y] because [reason]`
**Value**: Preserves reasoning behind changes, which is often more valuable than final decisions

**Enhanced Evidence Hierarchy**:

- **Tier 1 - Verified**: Direct quotes, explicit decisions with clear context
- **Tier 2 - Derived**: Logical inference with evidence chain shown
- **Tier 3 - Evolved**: Decision changes tracked with reasoning
- **Tier 4 - Gaps**: Missing information explicitly marked vs. assumed

### 2. Systematic Organization

Transform scattered conversational intelligence into structured documentation by:

- **Temporal flattening**: Decisions made across hours appear in logical order
- **Cross-referencing**: Connections between ideas become explicit links
- **Gap mapping**: Missing information systematically identified
- **Dependency tracking**: Understanding what blocks what

🔄 **EVOLVED**: v2.0 Enhancement - Conflict Resolution Framework

**Added**: Systematic handling of conversation contradictions and ambiguities
**Pattern**: When contradictions exist, prioritize most recent/detailed statement, document evolution with evidence
**Benefit**: Handles reality that conversations change direction without losing valuable context

### 3. Fidelity Over Completeness

Better to extract exactly what was discussed than to create "complete" documentation filled with assumptions.

**Gap Marking vs Gap Filling**:

❌ **Wrong Approach** (Gap Filling):

```markdown
Authentication: Use JWT tokens with 24-hour expiry (industry best practice)
```

✅ **WikiKit Approach** (Gap Marking):

```markdown
❌ GAP: No authentication method discussed → Blocks security implementation
```

🔄 **EVOLVED**: v2.0 Enhancement - Enhanced Fidelity Requirements

**Added**: Explicit anti-hallucination instructions in all prompts
**Standard**: "Every [output element] must trace to conversation evidence. When information is missing, mark gaps explicitly rather than filling with assumptions."
**Impact**: Prevents plausible but undiscussed additions while maintaining comprehensive extraction

## The Quality Ladder

### Level 1: Conversation Capture

- Record what was actually said
- Preserve direct quotes and decisions
- Note who said what when

### Level 2: Pattern Recognition

- Connect related ideas across conversation
- Identify recurring themes
- Spot implicit requirements in pain point descriptions

### Level 3: Intelligent Organization

- Structure insights into implementation-ready formats
- Cross-reference related decisions
- Map dependencies and blockers

### Level 4: Gap Intelligence

- Identify what's missing for implementation
- Flag contradictions needing resolution
- Highlight assumptions that need validation

🔄 **EVOLVED**: v2.0 Enhancement - Dynamic Adaptation

**Added**: Level 5: Domain Intelligence

- **Capability**: Adapt extraction categories to conversation domain
- **Examples**: Healthcare → clinical workflows, Fintech → regulatory compliance
- **Benefit**: Makes WikiKit effective for any industry vs. fixed generic categories

## The Extraction Mindset

### For Prompt Authors

**Think Like an Archaeologist**: Carefully uncover and preserve conversation artifacts without adding your own interpretation

**Document the Dig**: Show your work—how did you connect conversation points A and B to reach conclusion C?

**Preserve Context**: The surrounding conversation context often contains the real insights

**Flag Uncertainties**: Better to say "unclear" than to guess and be wrong

🔄 **EVOLVED**: v2.0 Enhancement - Conversation Evolution Mindset

**Added**: **Track the Journey**: How decisions evolved is often more valuable than final decisions
**Practice**: Use `🔄 EVOLVED` to capture before/after states with reasoning
**Value**: Preserves the thinking process that created the decisions

### For Prompt Users

**Trust the Process**: Extraction fidelity over extraction completeness

**Review the Gaps**: Missing information is often more valuable than present information

**Validate Extraction**: Check that outputs accurately reflect your conversation experience

🔄 **EVOLVED**: v2.0 Enhancement - Reality Validation

**Added**: **Expect Messiness**: Real conversations have contradictions—good extraction captures this reality
**Practice**: Look for `🔄 EVOLVED` markers showing how thinking changed
**Benefit**: Better decisions through understanding the reasoning journey

## Anti-Patterns to Avoid

### The Helpful Hallucination

**Problem**: Adding plausible details that weren't discussed
**Example**: Assuming standard authentication patterns when none were mentioned
**Solution**: Mark gaps explicitly rather than filling them

### The Coherence Illusion

**Problem**: Making conversations seem more logical than they actually were
**Example**: Presenting final decisions without showing the messy path to get there
**Solution**: Use evolution markers to show decision journey

🔄 **EVOLVED**: v2.0 Enhancement - New Anti-Patterns

**Added**: The Contradiction Avoidance
**Problem**: Hiding or glossing over contradictory statements in conversation
**Example**: Picking one approach when multiple conflicting approaches were discussed
**Solution**: Document contradictions with resolution approach or mark as needing clarification

**Added**: The Assumption Injection
**Problem**: Filling conversation gaps with "industry best practices" not discussed
**Example**: Adding security requirements because "all apps need authentication"
**Solution**: Mark security as a gap requiring conversation rather than assuming requirements

## Quality Validation

### The Four Tests

1. **Traceability Test**: Can you link every extracted item back to conversation content?
2. **Implementation Test**: Could two engineers build the same thing from your extraction?
3. **Conversation Test**: Would participants recognize this as their actual discussion?
4. **Gap Test**: Are missing pieces explicitly marked rather than assumed?

🔄 **EVOLVED**: v2.0 Enhancement - Additional Quality Gates

**Added**: 5. **Evolution Test**: Are decision changes captured with reasoning?
**Added**: 6. **Conflict Test**: Are contradictions resolved or marked for clarification?

### Success Metrics

- **Extraction Fidelity**: 90%+ of conversation insights captured
- **Implementation Readiness**: Developers can start building immediately
- **Decision Clarity**: Every choice has clear rationale
- **Gap Visibility**: Missing information explicitly identified

🔄 **EVOLVED**: v2.0 Enhancement - Enhanced Metrics

**Added**: **Evolution Tracking**: Decision changes captured with evidence
**Added**: **Conflict Resolution**: Contradictions addressed systematically
**Added**: **Domain Adaptation**: Categories adapt to conversation context

## The Philosophy in Practice

### Before WikiKit

- Scattered insights across hours of discussion
- Key decisions buried in casual remarks
- Missing information assumed rather than identified
- Context lost when conversation ends

### After WikiKit v1.0

- Systematic extraction of conversation intelligence
- Explicit gap identification
- Structured organization for implementation
- Preserved context and reasoning

🔄 **EVOLVED**: After WikiKit v2.0

**Enhanced**: Conversation evolution tracking preserves decision journey
**Enhanced**: Conflict resolution handles real conversation messiness  
**Enhanced**: Dynamic adaptation works for any domain
**Enhanced**: Token efficiency allows richer conversation processing

### Example Evolution Tracking

```markdown
🔄 EVOLVED: Target Market Definition

- **Initially**: "Small businesses with 5-20 employees" (founder assumption)
- **Changed to**: "Growing startups with 20-100 employees" (after user research)
- **Trigger**: 80% of interview subjects were in larger range
- **Impact**: Changed entire product positioning and feature prioritization
```

## v2.0 Advanced Techniques

### Conversation Threading

Track related decisions across conversation timeline to understand decision evolution patterns.

### Stakeholder Voice Separation

Identify different perspectives within same conversation to capture stakeholder dynamics.

### Context Evolution Tracking

Capture how conversation context changed overall understanding and strategy.

### Domain-Adaptive Extraction

Generate categories specific to conversation domain (healthcare, fintech, gaming) rather than using only generic categories.

---

The extraction philosophy is what makes WikiKit fundamentally different from generation-based documentation tools. Master this mindset, and you transform from a conversation participant into a conversation archaeologist, preserving the intelligence for surgical implementation.

🔄 **EVOLVED**: v2.0 captures not just the intelligence, but the intelligent journey that created it.
