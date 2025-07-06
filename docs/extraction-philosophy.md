# Extraction Philosophy: The WikiKit Way

> "LLMs are brilliant conversationalists but terrible archivists. WikiKit bridges that gap."

## Core Principle: Extraction Over Generation

The fundamental insight behind WikiKit is that LLM conversations already contain all the intelligence needed for comprehensive documentation. The challenge isn't generating new ideas—it's systematically extracting and organizing what was already discussed.

### Why Extraction Matters

1. **Fidelity to Decisions**: What you actually discussed is what matters, not what an LLM thinks you should have discussed
2. **Traceability**: Every documented decision can be traced back to conversation evidence
3. **Gap Identification**: Extraction reveals what wasn't discussed, highlighting areas needing attention
4. **Context Preservation**: The nuances and reasoning from your conversation are preserved

### The Extraction Mindset

When using WikiKit prompts, remember:

- **You are mining, not manufacturing**
- **Evidence over inference**
- **Structure over creativity**
- **Completeness over elegance**

## The Three Pillars of Extraction

### 1. Evidence Grounding

Every piece of extracted information must be traceable to the conversation:

```yaml
✅ VERIFIED: "We decided to use PostgreSQL" (directly stated)
📊 DERIVED: Multiple mentions of ACID requirements point to relational DB need
❌ DATA GAP: No discussion of backup strategy found
```

This prevents the common LLM pitfall of confidently stating things that were never discussed.

### 2. Systematic Organization

Scattered conversational intelligence becomes structured documentation:

- **Temporal flattening**: Decisions made across hours of conversation appear in logical order
- **Topic clustering**: Related ideas discussed separately get grouped together
- **Hierarchy emergence**: Flat conversation becomes nested document structure
- **Cross-referencing**: Connections between ideas become explicit links

### 3. Completeness Over Perfection

WikiKit prioritizes capturing everything over creating perfect prose:

- **Redundancy is OK**: Better to capture something twice than miss it
- **Rough edges reveal truth**: Awkward extraction often indicates unclear discussion
- **Gaps are features**: Missing information is valuable signal
- **Verbosity serves purpose**: Comprehensive beats concise for implementation docs

## Extraction vs. Generation: A Critical Distinction

### What Extraction Looks Like

```markdown
## Technical Decisions Extracted

- Database: PostgreSQL chosen (mentioned 3 times)
  - Reason: "need ACID compliance" (user message #14)
  - Concern: "worried about scaling" (user message #27)
  - ❌ DATA GAP: No specific version discussed
```

### What Generation Looks Like (Avoid This)

```markdown
## Recommended Technical Stack

- Database: PostgreSQL 15 with read replicas
  - Implements industry best practices for scaling
  - Includes automated backup strategy
  - Features comprehensive monitoring
```

The second example adds plausible details that weren't discussed—helpful perhaps, but not faithful to the conversation.

## The Extraction Quality Ladder

### Level 1: Surface Extraction

- Captures explicit statements
- Lists decisions made
- Notes major topics discussed

### Level 2: Contextual Extraction

- Includes reasoning behind decisions
- Captures concerns and trade-offs
- Links related discussions

### Level 3: Deep Extraction

- Identifies patterns across conversation
- Surfaces implicit assumptions
- Maps decision dependencies
- Highlights contradictions

### Level 4: Meta Extraction

- Reveals conversation dynamics
- Identifies decision-making patterns
- Exposes knowledge gaps
- Suggests follow-up areas

## Common Extraction Challenges

### Challenge 1: Scattered Context

**Problem**: Important details spread across many messages
**Solution**: Multi-pass extraction with cross-referencing

### Challenge 2: Implicit Decisions

**Problem**: Decisions made without explicit statement
**Solution**: Pattern recognition with DERIVED markers

### Challenge 3: Evolving Positions

**Problem**: Opinions change throughout conversation
**Solution**: Temporal tracking with latest position noted

### Challenge 4: Mixed Abstraction Levels

**Problem**: High-level strategy mixed with implementation details
**Solution**: Layered extraction into appropriate documents

## Extraction Best Practices

### For Prompt Authors

1. **Define clear extraction targets**: What specific information should be pulled?
2. **Create evidence requirements**: How should sources be cited?
3. **Build in gap detection**: What missing info should be flagged?
4. **Layer extraction phases**: Raw → Organized → Synthesized

### For Prompt Users

1. **Run extraction promptly**: Fresh conversations extract better
2. **Review intermediate outputs**: Catch misses early
3. **Iterate when needed**: Add clarifications and re-extract
4. **Trust the gaps**: Missing info is valuable signal

## The Philosophy in Practice

WikiKit's extraction philosophy transforms this:

```
"Yeah, we should probably use some kind of queue for that...
RabbitMQ is good. Or maybe Redis? Depends on if we need
persistence. Actually, for our use case, Redis pub/sub might
be enough since we discussed real-time updates earlier."
```

Into this:

```markdown
### Message Queue Decision

**Status**: 🔍 DECISION REQUIRED
**Options Discussed**:

- RabbitMQ: Mentioned as "good" option
- Redis pub/sub: Suggested for real-time use case
  **Decision Factors**:
- Persistence requirement: ❌ DATA GAP - not determined
- Real-time updates: ✅ VERIFIED - required (see earlier discussion)
  **Next Steps**: Clarify persistence requirements to finalize choice
```

## Evolution of Extraction

As WikiKit matures, extraction can become:

1. **More intelligent**: Better pattern recognition across conversations
2. **More connected**: Extraction that builds on previous documents
3. **More automated**: Tools that assist the extraction process
4. **More validated**: Extraction that self-checks for completeness

But the core philosophy remains: **We are archaeologists of conversation, not architects of imagination.**

---

_The extraction philosophy is what makes WikiKit different. While other tools generate plausible documentation, WikiKit reveals what was actually discussed—gaps, contradictions, and all._
