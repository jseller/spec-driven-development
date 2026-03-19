# Spec-Driven-Development
presentation slides and samples

- **spec-driven-development/** - Presentation from the volta preso on spec-driven development
- **skills/** - Reusable skills for product development workflows
  - **product-discovery/** - Product discovery and problem validation skill

## Skills

### Product Discovery

**Location**: `skills/product-discovery/`

**Purpose**: Analyze user conversations and problem descriptions to extract structured insights before writing specifications.

**What it does**:
- Identifies personas and their context
- Extracts Jobs To Be Done (JTBD)
- Maps problems to jobs
- Identifies key deliverables and recipients
- Ranks problems by business value
- Generates problem definitions for specifications
- Provides evidence that a problem is worth solving

**When to use**:
- Before writing a specification
- When analyzing user research or customer feedback
- To validate that a proposed solution addresses a valuable problem
- As part of spec-driven development to ensure you're solving the right problem

**How to use**:

1. **Prepare your input** - Gather interview notes, customer feedback, or problem descriptions
2. **Invoke the skill** - Provide your research text to the Product Discovery skill
3. **Review the analysis** - Check persona identification, problems identified, and value assessments
4. **Iterate if needed** - Add context or clarify aspects as needed
5. **Use for specification** - Use the problem definition as input to `/speckit.specify` or kiro.dev

**Output**: A structured Product Discovery Analysis document that includes:
- Persona identification with context
- Jobs To Be Done
- Key deliverables and recipients
- Problems ranked by value (High/Medium/Low)
- Problem definition suitable for specification
- Evidence for why the problem is worth solving
- Validation criteria
- Recommended next steps

**Example workflow**:

```bash
# 1. Read the skill documentation
cat skills/product-discovery/SKILL.md

# 2. Prepare your user research input (interview transcripts, feedback, etc.)

# 3. Provide input to the Product Discovery skill
# The skill will analyze the input and generate a structured analysis

# 4. Review the generated Product Discovery Analysis

# 5. Use the problem definition to create a specification
# - Use /speckit.specify with the problem definition
# - Or use kiro.dev to write EARS requirements
# - Or draft a feature proposal
```

**Integration with SpecKit**:

The Product Discovery skill output can be used directly as input for:
- `/speckit.specify` - To create feature specifications
- `/speckit.clarify` - To refine problem understanding
- kiro.dev - To write structured EARS requirements

**Quality Criteria**:

A good Product Discovery analysis should:
- ✓ Clearly identify at least one specific persona
- ✓ Extract 3-7 jobs to be done
- ✓ Identify at least 3 problems with value assessment
- ✓ Provide concrete evidence of problem value
- ✓ Connect problems to potential solutions
- ✓ Include validation criteria
- ✓ Make a clear recommendation for next steps

## Philosophy

From the Spec-Driven Development presentation:

> "You can't fully understand a problem until you start solving it"

These skills help you:
- Validate problems before jumping to solutions
- Keep problems in the backlog instead of solutions
- Spend time validating problems to avoid building the wrong thing
- Provide evidence that an idea could produce a valuable software product

## Resources

- **Presentation**: See `spec-driven-development/presentation.md` for the full Spec-Driven Development presentation
- **SpecKit**: See `../mercanlyapp/speckit/` for specification workflow tools
- **Kiro**: Visit [kiro.dev](https://kiro.dev) for EARS requirements syntax

