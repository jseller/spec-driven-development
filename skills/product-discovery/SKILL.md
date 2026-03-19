# Product Discovery Skill

## Purpose

This skill helps you work backward from specifications to understand the user problems that justify building the solution. It analyzes conversations, interviews, and problem descriptions to extract structured insights about personas, jobs to be done, and valuable problems worth solving.

## When to Use This Skill

- Before writing a specification, to validate that a real problem exists
- When analyzing user research interviews or customer feedback
- To understand if a proposed solution addresses a valuable problem
- To connect user problems to potential software solutions
- As part of spec-driven development to ensure you're solving the right problem

## Input

The skill accepts any text describing problems or user conversations:
- Interview transcripts
- User conversation notes
- Problem descriptions
- Customer feedback
- Requirements workshop notes
- Any text where someone describes challenges they face

## Process

When you provide input to this skill, it will:

1. **Parse the input** - Extract key information from the conversation or description
2. **Identify personas** - Determine who is experiencing the problem and their context
3. **Extract Jobs To Be Done (JTBD)** - Understand what the persona is trying to accomplish
4. **Map problems to jobs** - Connect specific problems to the jobs they're trying to do
5. **Identify deliverables** - Determine what artifacts or outcomes the persona produces
6. **Identify recipients** - Understand who receives or benefits from these deliverables
7. **Rank problems by value** - Assess which problems have the most business impact
8. **Generate problem definition** - Create a clear articulation of the most valuable problems
9. **Provide evidence for specification** - Show the connection between user problems and solution value

## Output Format

The skill produces a structured analysis document:

```markdown
# Product Discovery Analysis

**Date**: [Analysis Date]
**Source**: [Brief description of input source]

---

## Persona: [Role/User Type]

**Context**: [Brief description of the persona's environment and constraints]

---

## Jobs To Be Done

↳ [Primary job the persona is trying to accomplish]
↳ [Secondary job]
↳ [Additional jobs...]

---

## Key Deliverables

↳ [What they need to produce] → [Who receives it]
↳ [Another deliverable] → [Its recipient]

---

## Problems Identified

### High Value Problems

↳ **[Problem 1]**
  - Impact: [Description of business/user impact]
  - Frequency: [How often this occurs]
  - Current workaround: [How they handle it today]
  - Value of solving: [Why this matters]

↳ **[Problem 2]**
  - Impact: [Description of business/user impact]
  - Frequency: [How often this occurs]
  - Current workaround: [How they handle it today]
  - Value of solving: [Why this matters]

### Medium Value Problems

↳ **[Problem 3]** - [Brief description and why it's medium priority]

### Low Value Problems

↳ **[Problem 4]** - [Brief description and why it's low priority]

---

## Problem Definition (For Specification)

**Primary Problem**: [1-2 sentence statement of the most valuable problem]

**Who has this problem**: [Specific persona(s)]

**When it occurs**: [Context/triggers]

**Current cost**: [What it costs them today - time, money, frustration, risk]

**Desired outcome**: [What success looks like]

---

## Evidence for Specification

### Why This Problem is Worth Solving

- [Evidence point 1 - quantitative if possible]
- [Evidence point 2 - qualitative impact]
- [Evidence point 3 - business value]

### Connection to Software Solution

- [How software could address this problem]
- [What capabilities would be needed]
- [Expected value creation]

### Validation Criteria

Before proceeding to specification, validate:
- [ ] Problem clearly identified and understood
- [ ] Persona and context well-defined
- [ ] Business value articulated
- [ ] Solution approach would address root cause
- [ ] Problem is valuable enough to justify solution effort

---

## Next Steps

**Recommended Action**: [Proceed to spec / Gather more info / Pivot approach]

**Reasoning**: [Why this recommendation]

**If proceeding to spec**: Use this analysis as input to `/speckit.specify` or kiro.dev to create a solution specification that addresses the identified problems.
```

## Usage Instructions

### Step 1: Prepare Your Input

Gather your source material:
- Interview notes or transcripts
- Customer feedback
- Problem descriptions
- Any text describing user challenges

### Step 2: Invoke the Skill

Provide your input to the Product Discovery skill. You can:
- Paste the full text of your research
- Provide a summary of key points from multiple sources
- Share specific problem statements you want to analyze

### Step 3: Review the Analysis

The skill will generate a structured analysis. Review it for:
- Accuracy of persona identification
- Completeness of problems identified
- Validity of value assessments
- Clarity of problem definition

### Step 4: Iterate if Needed

If the analysis is incomplete or unclear:
- Provide additional context
- Clarify specific aspects
- Add more source material
- Refine problem statements

### Step 5: Use for Specification

Once satisfied with the analysis, use the problem definition and evidence to:
- Create a specification with `/speckit.specify` 
- Use kiro.dev to write EARS requirements
- Draft a feature proposal
- Validate that your solution addresses real problems

## Quality Criteria

A good Product Discovery analysis should:

✓ Clearly identify at least one specific persona
✓ Extract 3-7 jobs to be done
✓ Identify at least 3 problems with value assessment
✓ Provide concrete evidence of problem value
✓ Connect problems to potential solutions
✓ Include validation criteria
✓ Make a clear recommendation for next steps

## Tips for Better Results

1. **Be specific**: Provide concrete examples and details from your research
2. **Include quotes**: Direct quotes from users are valuable evidence
3. **Share context**: Background about the persona's environment helps
4. **Note frequency**: How often problems occur matters for prioritization
5. **Mention costs**: Quantify impact when possible (time, money, risk)
6. **Capture emotions**: Frustration levels indicate problem severity
7. **Identify workarounds**: How people cope today reveals pain points

## Integration with Spec-Driven Development

This skill supports the spec-driven development process by:

1. **Validating Problem Value** - Ensures you're solving problems worth solving
2. **Providing Spec Input** - Generates clear problem statements for specifications
3. **Evidence-Based Development** - Connects solutions to real user needs
4. **Avoiding Over-Engineering** - Focuses on valuable problems, not interesting tech
5. **Supporting Iteration** - Clear problems make it easier to validate solutions

## Philosophy

From the Spec-Driven Development presentation:

> "You can't fully understand a problem until you start solving it"

This skill helps you understand problems *before* jumping to solutions, enabling you to:
- Find simple, elegant solutions by validating the problem first
- Keep problems in the backlog instead of solutions
- Spend time validating problems to avoid building the wrong thing
- Provide evidence that an idea could produce a valuable software product

---

**Ready to use?** Provide your user research, conversation notes, or problem descriptions to begin the Product Discovery analysis.