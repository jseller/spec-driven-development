---
marp: true
theme: default
paginate: true
backgroundColor: #fff
---

# Specification - Driven - Development

Using Specs to build software products

Jonathan Seller: Software Developer \(25 Years Startups & Scale\-ups\)

Principal Software Engineer: Building GraphRAG system at big data corp

# Spec-Driven Development

Not about using AI as components in the stack\.

About using AI to build software: containers\, components\, logic

\- efficiency of using requirements and specs

\- prompts and context\, claude\.md\, markdown

\- personal\, team development flows with specs

\- agentic development\, with specs

---

# Hype vs. Reality

\- the hype is very scattered\, we are still figuring this out

\- programmed 4 million lines? Building an os?

\- saved 50\,000 hours \(more hours that exist\)

\- or horrible code “doesn’t work at all”\, going in circles

\- deleting files\, security holes\, exposed tokens

\- The creation buzz is real\, but easy to create more complexity than you need

\-  __how much is enough or effective__

---

# Field Observations

• Tools are fleeting\, changing; core concepts and new problems are emerging

• Reality: AI is a very useful assistant/pair programmer\, but context is the bottleneck\. High cognitive load: it is a different kind of tired

• Risks: Siloed development builds complexity in isolation

• Ownership: Who fixes the production bug at 3 AM?

Customer Cost: “we aren’t paying that”

---

# The Economics of AI Dev

• Token Economics: Moving from VC\-subsidized usage to real costs

Vc funded party won’t last\, cost is about 10x current cost

• Human Constraints: Can Marketing and Sales ingest 10x code velocity?

Users can only tolerate so much change

• Workflow Shift: Generating fixes faster than we can estimate them

Not validation outcomes\, but still measuring effort \(loc\, etc\)

---

# Context

• Understanding context

memory and remembering useful parts

using 70% of the window seems ideal for accuracy and recall

Intelligence with limited memory: people expect you to remember conversations\, don’t expect LLM to do that

• Context Rot: The need for compaction and summarization

Clear and understand to not confuse

• Solution: Small\, cheap models with high\-quality context do very well

---

# Structured Prompting

• Outcome\-Oriented: Ask for reasoning and logic\, not just code

• Prompting Evolution: Currently in the 'HTML 3\.2' era

• Skills & Patterns: Using packages like DSPy to add structure

• Strategy: don’t ask twice\, ask for reason and logic

ask it why\, or provide 2 options and pick the winner

Chain of Thought \( just one thought\)

---

# Problem Solving as you go

• You can't fully understand a problem until you start solving it

• Foundations: Understand problems and solution requirements

• Problem\-First Backlog: Solve the most valuable problems in small chunks

Problems are for the backlog\, if backlog has solutions\, just replace with the problem that was supposed to solve. 

Spend time validating problem to find simple\, elegant solution

---

# Iterative Problem Solving

• The Loop: Understand → Plan → Execute → Review

Complete all steps\, most just churn on the third step

• Reasoning Models: Declare the outcome\, not the steps

People can reason as well\. 

• Automation: Generate the boring\, “Don't have time for” stuff\. Great for writers block\, but ruthlessly delete and simplify

• Selection: The primary dev skill is now choosing the correct context

---

# Specs and Requirements are formalized language

Every domain has a spec language\, a common language

\- cooking has recipes\, software has requirements

\- Any function: RFP for purchasing\, Financial reports\, accounting

What is the most efficient way to make something?

Size of spec is relative to complexity of what is built

Conversation\, Pictures \(mock\-ups\)\, and recipes

\- what is more efficient? Making and trying 10 meals or getting it right with one try?

---

# Efficiency of Requirements

• Every Domain has a Spec: Recipes\, RFP\, Financials\, Requirements

• The Bridge: Something that describes 'what' is being made

Talking about what you are making and not how\.

• Verification: Define 'just enough' so that the outcome is verifiable\. Define just enough that you can verify to cut down on noisy iterations

---

# Cleaning the Mental Workspace with Specs

• Messy Context = Messy Results: Confusion stems from cluttered sessions

Try not to keep everything in your head\, write it down

• Engineering Vibes: Conversation\-driven dev results in 'Hackathon Prototypes'

• Structure: Use specs to organize the LLM's memory\, and more isn’t better

\- confusion in LLM response is from messy context\. Will take path of least resistance

\- how much can a memory hold

\- how to structure memory?

---

# Using Specs and designing Architecture

• Avoid Big Design/Big Plan up Front at all costs

Avoid any big effort up front \(design\, plan\)

Understand how to learn faster together\, Learn faster\, and review rather than planning longer

• Time\-Boxing: Start with a one\-page spec and revisit during release

__Work backwards from this definition__

• Contracts: Implement to the contract\, don't design the implementation

Living documents\. They are never finished\, they aren’t supposed to be

---

# Professional Development has some Discipline

• The Sweet Spot: No design hurts; too much design paralyzes

Architecture > Engineering > Programming

\- Start with a time\-boxed one\-pager

\- Define the contracts\, implement to the contract\,  do not design the implementation

\- Design with intent, or design will just happen coincidentally.

\- Most delays are people/organization/communication problems\. “Move fast and break things” is just being sloppy and very much depends on what kind of software you are making

---

# Rules for Cursor & Claude, etc

• Canonical Examples: Build 'Source of Truth' code templates first

LLM is good to take a sample and then apply same sample

• Less is More: Auto\-generated files and directory listings bloat context

avoid prose\, be very terse

• Instruction Following: Use \.md files for high\-level logic and patterns

Link to files or skills

• Tooling: Use linters/formatters for style—don't waste tokens on it

Always look for deterministic tools that use compute

---

# Managing Memory

* • Load on Demand: load only what is needed at the moment
* • Plan Mode: focus on solution complexity before implementation
* Use the ADR/RFC process with the LLM\, keep it small
* • Update constantly: Refine context at every major step
* Clear context and maintain context health
* Use YAML for simple structure
  * LLM understands structure\, much more efficient than inferring from text
* Use Commands and Skills

---

# OpenSpec & Feature Maps

• Creates a change before rolling it into the app

The 4\-Step Review: Clarify architecture to maintain clean context

• Consistency: Use version control for specs as strictly as code

Easier to understand changes/releases\, provides log

• Workflow: Feature Map → Adjust Arch → Adjust Plan

https://github\.com/Fission\-AI/OpenSpec

---

# SpecKit, Kiro, & GSD

• SpecKit: Commands for Specify\, Analyze\, Plan\, Implement

\- /speckit\.analyse really good for understanding scope of a version\, gives tasks\, estimates\. produces all tasks\, some for humans\, some for LLMs

\- found I kept doing one big feature\, and then working with cline to finish it

\- still had to have the discipline to clean up

• Kiro \(kiro\.dev\): Clean EARS requirements syntax

• GSD \(Get Shit Done\): Streamlined workflow automation\, but organic definition

---

# Agentic Development

• Role Definition: Specs provide clear responsibilities to avoid chaos and token usage

\- deterministic workflows are already solved processes

\- mapping to roles in the modern workplace chaos could be repeating mistakes

• MCP: Token Management: Overhead for basic workflows can hit 32k tokens

• 	Architecture: Use sub\-agents to manage local context and avoid bloat

•	Caching: Tune for cached system prompts to save cost and time

---

# Process Oriented vs Outcome oriented

\- illusion of control\. Give it up\, but it is hard not to micro\-manage/parachute\-parent

\- are agents going to report how busy they are?

\- are agents going to ask each other for story points?

\- software production is not in great shape

\- lacking true engineering cert

\- not sure its a good idea to automate a bad process

\- LLM get practices from public info\, much public info is about hyping a certain process and less about measuring reality of it

---

# AI Product Development

AI great for user research\, and all PM tasks

\- clarify problems and valuable problems\. Valuable to your business

Understand users and what they value to find valuable problems

\- understand jobs to be done and valuable deliverables

\- find ICP\, understand TAM

\- competitive analysis

Easy to generate artifacts for Product Value\, Planning and Release \(requiremints\.app\)

---

# Theory of Constraints

• The Ingestion Bottleneck: How fast can humans review the generated output?

• 	Stuck Mode: Delete and regenerate smaller versions

• Value: Use LLMs to understand value\, not just generate volume

Parachute Parenting: Hard not to micro\-manage agents; focus on outcomes

• Automation: Don't automate a bad process

• Discipline: Software production lacks true engineering certs; specs help provide that definition

---

# The Strategic Path Forward

• Context is the Asset: Keep it Secure\, portable\, and versioned for enterprise adoption\. Not solved yet\, but can with governance\, judgement and discipline

• Create Determinism: Probabilistic behavior creates cost; deterministic behavior is free\. Get good at not relying on LLM assistance all the time\.

Find out from users\. Adoption happens\, when it happens: seeing mandated usage \(prompts/week\)\, no need of telling people to use a better tool\, they do it

\- some hype is eventualities\, railroads and dotcoms were also bubbles\. We aren’t there yet

