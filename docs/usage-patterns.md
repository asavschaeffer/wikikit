# Usage Patterns: Real-World WikiKit Workflows

> "The best documentation system is the one that fits your actual workflow."

## Pattern 1: The Post-Brainstorm Extraction

### When to Use

- After a 1-3 hour brainstorming session
- When conversation naturally concludes
- Before context is lost or forgotten

### Workflow

```
1. Complete Natural Conversation
   ↓
2. Load project-summary-quick.yaml (lite prompt)
   ↓
3. Review extraction for completeness
   ↓
4. Identify which full prompts needed
   ↓
5. Run targeted full extractions
   ↓
6. Organize into documentation suite
```

### Real Example

```bash
# After discussing a task management app
cat prompts/lite/unified/project-summary-quick.yaml
# Paste into conversation

# Output reveals:
# - Decided on React + Node.js
# - Discussed real-time updates
# - No database decision made
# - Security not covered

# Next steps:
cat prompts/full/planning/technical-feasibility-adr.yaml
# Generates complete ADRs for tech stack

cat prompts/full/architecture/database-design.yaml
# Focuses on missing database decision
```

### Tips

- Don't wait too long after conversation (freshness matters)
- Start with lite prompt to avoid token overload
- Use gaps identified to guide next prompts

## Pattern 2: Progressive Documentation Building

### When to Use

- Large projects needing comprehensive docs
- When you have time for thorough extraction
- Building documentation for team handoff

### Workflow

```
Day 1: Planning Extraction
├── product-research-discovery.yaml
├── project-vision.yaml
└── technical-feasibility-adr.yaml

Day 2: Requirements Extraction
├── functional-requirements.yaml
└── non-functional-requirements.yaml

Day 3: Architecture Extraction
├── high-level-design.yaml
├── api-specifications.yaml
└── database-design.yaml

Day 4: Review & Fill Gaps
└── [targeted prompts for gaps]
```

### Real Example

```markdown
## Monday: After initial brainstorming

- Run product-research-discovery.yaml
- Output: Comprehensive market analysis, user personas
- Gaps noted: Specific performance requirements

## Tuesday: Requirements deep dive

- Discuss performance needs based on gaps
- Run functional-requirements.yaml
- Run non-functional-requirements.yaml
- Output: Complete requirements with performance targets

## Wednesday: Technical architecture

- Reference requirements in new conversation
- Discuss architecture approaches
- Run high-level-design.yaml
- Output: System architecture with component design

## Thursday: Gap filling

- Review all docs for "DATA GAP" markers
- Have targeted conversations on gaps
- Run specific prompts to fill gaps
```

### Tips

- Each day builds on previous extractions
- Fresh conversations prevent token overload
- Review gaps before next session

## Pattern 3: Iterative Refinement

### When to Use

- When first extraction misses important details
- Clarifying ambiguous decisions
- Improving documentation quality

### Workflow

```
1. Initial Extraction
   ↓
2. Review for Misses/Errors
   ↓
3. Add Clarifying Context
   "Also, when we discussed X, we meant Y"
   ↓
4. Re-run Same Prompt
   ↓
5. Compare Outputs
   ↓
6. Merge Best Parts
```

### Real Example

```markdown
## First Extraction Attempt

Run: technical-feasibility-adr.yaml
Result: Misses Kubernetes discussion, unclear on database choice

## Add Context

"To clarify our earlier discussion: when I mentioned 'container orchestration',
I was specifically referring to Kubernetes vs. ECS. Also, the database discussion
about 'needing flexibility' was about schema flexibility, not deployment flexibility."

## Second Extraction

Run: technical-feasibility-adr.yaml again
Result: Now includes Kubernetes vs. ECS ADR, clarifies MongoDB choice

## Final Output

Merge both extractions, keeping the best parts of each
```

### Tips

- Don't delete first extraction - compare them
- Be specific in clarifications
- Focus on missed decisions, not writing style

## Pattern 4: Team Knowledge Transfer

### When to Use

- Onboarding new team members
- Preparing for handoffs
- Creating shared understanding

### Workflow

```
1. Solo Brainstorming Session
   ↓
2. Extract Core Decisions
   ↓
3. Team Reviews Extraction
   ↓
4. Team Adds Missing Context
   ↓
5. Re-extract with Full Context
   ↓
6. Generate Implementation Docs
```

### Real Example

```markdown
## CTO's Solo Session

- 2-hour architecture brainstorming
- Run: project-vision.yaml, technical-feasibility-adr.yaml
- Share with team

## Team Review Meeting

Team identifies gaps:

- "What about mobile app?"
- "How do we handle EU compliance?"
- "What's the data retention policy?"

## Enhanced Session

CTO + Team discuss gaps, then:

- Run: requirements.yaml (now includes mobile)
- Run: security-architecture.yaml (covers compliance)
- Run: business-strategy.yaml (includes retention)

## Result

Complete documentation suite reflecting full team knowledge
```

### Tips

- First extraction reveals what solo brainstormer knows/doesn't know
- Team review catches critical gaps
- Final extraction captures collective intelligence

## Pattern 5: Continuous Documentation

### When to Use

- Long-running projects
- Evolving requirements
- Agile environments

### Workflow

```
Sprint 1:
├── Initial extraction
└── baseline-docs/

Sprint 2:
├── New conversation about changes
├── Run prompts with "UPDATE" context
└── updated-docs/

Sprint 3:
├── Continue pattern...
```

### Real Example

```markdown
## Sprint 1 (Project Start)

Full extraction suite → v1.0 docs

## Sprint 3 (Pivot to Microservices)

Conversation: "Based on user growth, we need to move from monolith to microservices"
Prompt prefix: "UPDATE: The following revises our earlier monolithic architecture decision..."
Run: technical-feasibility-adr.yaml
Output: New ADR-006 superseding ADR-001

## Sprint 5 (Add ML Features)

Conversation: Discuss ML pipeline needs
Run: New prompts + update existing
Result: ML-specific architecture docs + updated system design
```

### Tips

- Mark superseded decisions clearly
- Keep version history
- Reference previous docs in conversations

## Pattern 6: Quick Decision Capture

### When to Use

- Short focused discussions
- Single technical decisions
- Time-constrained situations

### Workflow

```
15-min discussion
    ↓
technical-decisions-quick.yaml
    ↓
Brief decision record
```

### Real Example

```markdown
## Quick Database Discussion

"Should we use Postgres or MySQL for the auth service?"
[10 minute pros/cons discussion]

## Run Lite Prompt

technical-decisions-quick.yaml

## Output (30 lines)

Decision: PostgreSQL for auth service
Reasons:

- Better JSON support for user preferences
- Team expertise
- Consistent with other services
  Next: Set up Postgres 14 with standard config
```

### Tips

- Don't overthink - capture fast
- Lite prompts perfect for this
- Can expand later if needed

## Anti-Patterns to Avoid

### ❌ The Token Bomb

Loading all prompts at conversation start, consuming 50k+ tokens before you begin

### ❌ The Perfect Documentation Trap

Endless cycles of extraction trying to get "perfect" output instead of "good enough"

### ❌ The Context Mixer

Running architecture prompts on business discussions or vice versa

### ❌ The Gap Ignorer

Seeing "DATA GAP" markers but not addressing them

### ❌ The Hallucination Enabler

Adding context like "also include industry best practices" that invites generation over extraction

## Choosing the Right Pattern

| If You Have...              | Use Pattern...             |
| --------------------------- | -------------------------- |
| Just finished brainstorming | Post-Brainstorm Extraction |
| A week for documentation    | Progressive Documentation  |
| Incomplete first extraction | Iterative Refinement       |
| New team members            | Team Knowledge Transfer    |
| Ongoing project             | Continuous Documentation   |
| Quick decision to capture   | Quick Decision Capture     |

## Advanced Techniques

### Prompt Chaining

```bash
# Output of one prompt feeds the next
extract_requirements.yaml → requirements.md
cat requirements.md + high_level_design.yaml → architecture.md
```

### Parallel Extraction

```bash
# Different team members run different prompts
Dev 1: technical-feasibility-adr.yaml
Dev 2: api-specifications.yaml
Dev 3: database-design.yaml
# Merge results
```

### Extraction Validation

```bash
# Run same prompt twice with different context framing
Context 1: "From a security perspective..."
Context 2: "From a performance perspective..."
# Compare outputs for completeness
```

## Success Metrics

### Good Extraction Session

- ✅ All key decisions captured
- ✅ Clear traceability to conversation
- ✅ Gaps explicitly identified
- ✅ Team can implement from docs
- ✅ No hallucinated requirements

### Poor Extraction Session

- ❌ Generic documentation
- ❌ Missing obvious decisions
- ❌ No gap identification
- ❌ Team needs clarification
- ❌ Invented "best practices"

---

_The best WikiKit workflow is the one you'll actually use. Start simple with post-brainstorm extraction, then expand as you see value. Remember: imperfect extraction beats perfect procrastination._
