# Mentat Platform Architecture v1.0

## Purpose

Mentat is a Markdown-first knowledge operating system.

The platform exists to transform ideas into structured knowledge and generate reusable expressions from that knowledge.

The system is designed around:

- human thinking
- Markdown-based knowledge creation
- version control
- AI collaboration
- repeatable artefact generation

---

# Architecture Principles

## 1. Markdown First

Markdown is the primary environment for thinking and knowledge development.

It provides:

- portability
- transparency
- version history
- human readability
- AI compatibility

The Markdown file is the source.

---

## 2. Knowledge Before Artefacts

Artefacts are generated expressions of knowledge.

The relationship is:


Knowledge

↓

Transformation

↓

Artefact


Never start with the artefact.

Start with the thinking.

---

## 3. Human Direction, AI Acceleration

Humans provide:

- intent
- judgement
- context
- decisions

AI supports:

- structuring
- transformation
- generation
- consistency
- automation

---

# System Architecture

                Mentat Operating Model

                        ↓

              Markdown Knowledge

                        ↓

                Transformation

                        ↓

                  Artefacts

                        ↓

                 Publications

                        ↓

                 Feedback Loop

---

# Repository Architecture


mentat/

├── operating-model/
│
├── knowledge/
│
├── publications/
│
├── artefacts/
│
├── templates/
│
├── brand/
│
├── architecture/
│
└── CLAUDE.md


---

# Knowledge Layer

## Purpose

Store all Markdown-based thinking and knowledge.

Structure:


knowledge/

├── inbox/
│
├── explorations/
│
├── assets/
│ ├── principles/
│ ├── frameworks/
│ ├── models/
│ ├── concepts/
│
├── projects/
│
└── decisions/


---

# Inbox

Purpose:

Capture raw ideas.

Characteristics:

- incomplete
- unstructured
- temporary

Examples:

- notes
- observations
- questions
- hypotheses

---

# Explorations

Purpose:

Develop ideas before deciding their destination.

Characteristics:

- structured thinking
- early frameworks
- working hypotheses

---

# Knowledge Assets

Purpose:

Store reusable knowledge.

Examples:

- principles
- frameworks
- models
- concepts

These are canonical Markdown files.

---

# Publications Layer

## Purpose

Store human-facing content.

Structure:


publications/

├── linkedin/
├── articles/
├── talks/
└── newsletters/


A publication can originate from:

- a knowledge asset
- an exploration
- a standalone idea

---

# Artefact Layer

## Purpose

Store generated representations.

Structure:


artefacts/

├── apps/
├── documentation/
├── linkedin/
├── presentations/
└── published/


Artefacts can be regenerated.

---

# Future Capabilities

Future versions of Mentat may introduce supporting capabilities such as:

- knowledge templates
- automated scaffolding
- validation systems
- publishing pipelines
- semantic search
- knowledge graphs
- AI agents

These capabilities should be introduced only when they improve the knowledge workflow.

The current foundation remains:

Markdown + Git + AI collaboration.

---

# Transformation Layer

Future capability:

Convert Markdown knowledge into:

- websites
- presentations
- diagrams
- social content
- documentation

Transformation should preserve meaning.

---

# Automation Principles

Automate:

- repetitive formatting
- generation
- validation
- publishing

Do not automate:

- judgement
- intent
- strategic decisions

---

# Evolution Path

Future Mentat capabilities may include:

- semantic search
- knowledge graphs
- AI agents
- automated publishing
- interactive knowledge applications

The foundation remains:

Markdown + Git + AI collaboration.

---

# Architecture Principle

The platform should make knowledge easier to create, maintain, transform and reuse over time.

The system should compound.