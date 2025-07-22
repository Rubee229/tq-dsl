# Toneovial Intelligence × TQ-DSL  
*A Human-AI Semantic Language Framework for Education*

This project introduces **Toneovial Intelligence™** — a cognitive framework for learning through tone, structure, and reasoning — and its operational syntax layer: **TQ-DSL** (Teaching Quotient Domain-Specific Language).

TQ-DSL is a domain-specific language designed to help teachers annotate instructional logic in a machine-readable way, enabling co-learning experiences between educators, learners, and AI.

---

## Table of Contents(plus)

- [What is TQ-DSL](#custom-tq-dsl)
- [What is Toneovial Intelligence](#custom-toneovial-intelligence)
- [Who Is This For](#custom-who-is-this-for)
- [Contribution](#custom-contribution)

---
<a name="custom-tq-dsl"></a>
## What is TQ-DSL  
*A Domain-Specific Language for Teaching Strategy Markup – Human-Writable, AI-Readable*

**TQ-DSL (Teaching Quotient Domain-Specific Language)** is an open syntax system designed for co-learning between educators, learners, and AI.

It allows teachers to semantically tag instructional content using a lightweight, code-like structure — marking teaching steps, reasoning strategies, student levels, sentence patterns, and learning cues. These annotations are both human-readable and machine-parsable, enabling AI systems to support adaptive instruction, generate learning tasks, and engage in structured strategy-aware dialogue.

TQ-DSL forms a semantic bridge that connects:  
**Instructional content → Pedagogical strategy → AI interaction → Learning tasks → Teacher collaboration → Learning traceability**

---
<a name="custom-toneovial-intelligence"></a>
## What is Toneovial Intelligence™

**Toneovial Intelligence™** is the conceptual foundation behind TQ-DSL.  
It is a human-centered cognitive framework that treats tone and structure not as decorative features, but as scaffolds for reasoning, reflection, and dialogue.

It aims to externalize *how we think* — not just *what we know* — by combining insights from:
- Educational psychology  
- Language and discourse analysis  
- AI-mediated interaction  

Through submodules like **Toneovial Math™**, learners are encouraged to verbalize their thinking process — even when making mistakes — turning error into structured understanding.

TQ-DSL operationalizes this vision by offering a syntax layer that AI systems can read, interpret, and respond to.

<a name="custom-who-is-this-for"></a>
## Who Is This For

- **Educators** designing structured, strategy-based lessons enhanced by AI  
- **Developers** building co-learning tools, DSL parsers, or AI tutors  
- **Curriculum designers** exploring multi-layer instruction and student-level adaptation  
- **Researchers** investigating semantic teaching frameworks and machine-parsable pedagogy

<a name="custom-contribution"></a>
## Contribution

This project welcomes collaborators from both education and AI communities.  
You are invited to contribute by:
- Proposing new syntax rules and use cases  
- Sharing classroom implementations  
- Developing tools that support or parse TQ-DSL  
- Helping shape the future of human–AI co-learning


## Table of Contents

1. [What is TQ-DSL?](#1-what-is-tq-dsl)
2. [Language Objectives](#2-language-objectives)
3. [Syntax Structure Overview](#3-syntax-structure-overview)
4. [Sample Snippet (TQ-DSL in Use)](#4-sample-snippet-tq-dsl-in-use)
5. [AI Features Enabled by TQ-DSL](#5-ai-features-enabled-by-tq-dsl)
6. [For Developers: Parsing TQ-DSL for AI Systems](#6-for-developers-parsing-tq-dsl-for-ai-systems)
7. [Open Source & Community Principles](#7-open-source--community-principles)
8. [Future Extensions (v1.0+)](#8-future-extensions-v10)
9. [Invitation to Join](#9-invitation-to-join)

⸻

## 1.What is TQ-DSL?

TQ-DSL is an open syntax language designed for AI-assisted teaching systems and strategy-driven educators.
It enables teachers to annotate instructional materials using a code-like structure, marking teaching steps, reasoning strategies, learner grouping, language deconstruction, and learning reminders in a way that is readable, collaborative, and interactive for AI.

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 2.Language Objectives

| Item          | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| Purpose       | Provide teachers with a fast syntax structure to semantically annotate instructional strategies. |
| Readability   | Human-readable, AI-parsable and classifiable.                              |
| Executability | Enables AI to transform syntax into lesson plans, vocabulary lists, task cards, and interactive activities. |
| Extensibility | Supports user-defined semantic tags for adaptation across subjects and levels. |

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 3.Syntax Structure Overview

TQ-DSL uses a standardized syntax format:
[prefix][semantic_type]*[subtag]: content sentence

For example:
/step 1: Identify paragraph structure  
@decode*coherence: Observe contrast transitions like “however”  
chunk*angle: think twice → 再三考慮

You can define your own subtag types to suit different subject domains.  
For instance, teachers might use:

- `@decode*inference`  
- `@decode*structure`  
- `@decode*evidence`

This makes TQ-DSL extensible across disciplines such as English reading, science inquiry, or math problem solving.

### chunk*subtype

Used to mark teachable language units, such as phrasal verbs, idioms, grammar formulas, or domain-specific terms.  
These markers help AI recognize reusable instructional targets for transformation, practice generation, or learner feedback.

Examples:
chunk*phrasalverb: give up → 放棄  
chunk*grammar: It is + adj + that + S + V → 強調句型  
chunk*science: evaporation → 蒸發

## 4.Sample Snippet (TQ-DSL in Use)
@meta: English Reading Structure Task – National Exam Context

/step 1: Begin by counting the number of paragraphs. Predict the structure (e.g., Introduction-Development-Turn-Conclusion or Point 1-2-3-Contradiction).

/step 2: Read the final sentence first. Identify the paragraph’s stance or cautionary tone.  
@decode*mumskill  
chunk*angle: if you're worried about... → "If you are concerned..."

golden rule in exam: Time is limited. Do not aim to read every sentence in full.

#level.high: Directly compare the options with paragraph logic gaps.  
#level.mid: Pay attention to transitions like "also" and "however".  
#level.low: Understand and spell phrases like "you’d better think twice".

@remind^sign: The second-to-last sentence often contains contrast or additional information.

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 5.AI Features Enabled by TQ-DSL

TQ-DSL syntax enables AI systems to automatically:
A.Generate lesson plans based on /step structure
B.Create sentence pattern replacement tasks from chunk*angle
C.Produce leveled task cards using #level.high/mid/low
D.Extract strategic notes using @decode and golden rule
E.Suggest pronunciation/spelling practices using >rephrase + chunk
F.Facilitate dialog-based tutoring via structured strategy instruction

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 6.For Developers: Parsing TQ-DSL for AI Systems

TQ-DSL is a line-based, semantically-tagged instructional language. It uses a prefix + type + subtype format for every tag.

🧾 Syntax Parsing Pattern
[type][*subtype]: [content or directive]

Each line can be interpreted as a semantic instruction. Example:
/step 2: Read conclusion first
@decode*coherence: Observe transitions like "however"
chunk*angle: you’d better think twice → 再三考慮
#level.low: Focus on spelling and reading

📥 AI-friendly Mapping Output (e.g. YAML)
- type: step
  order: 2
  description: Read conclusion first

- type: decode
  subtype: coherence
  strategy: Observe transitions like "however"

- type: chunk
  subtype: angle
  input: "you’d better think twice"
  output: "oops"

- type: level
  level: low
  task: Focus on spelling and reading

————
Applications for Developers
a.Turn TQ-DSL syntax into prompt templates
b.Train LLMs with tagged learning strategies as fine-tuning input
c.Generate adaptive feedback and microtasks based on #level.* markers
d.Build interactive tutors that follow /step logic
e.Combine @decode strategies with chunk lines to produce comprehension-enhancing tasks

The language is intentionally designed to be:
a.Flat but composable
b.Human-writable
c.Easily tokenizable and structure-extractable

Parser reference implementations will be available in Python and JavaScript.

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 7.Open Source & Community Principles
This project is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)

You are free to use, modify, and share this teaching syntax with attribution and share-alike terms.

Community Contributions Encouraged: Syntax expansions, translations, tooling support, integrations, and classroom examples are welcome.

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 8.Future Extensions (v1.0+)
a.Syntax Expansion: Add logic support for math, science, reading literacy, and other subjects.
b.TQ-AI Integration: Build a parsing engine or fine-tuned GPT tutor for TQ structure.
c.Material Conversion Tool: Translate traditional teaching materials into TQ-DSL annotated structure.
d.Interactive Learning Platform: Let students use TQ-DSL for task prompts, reflection, self-assessment, and peer review.
e.Lesson Version Control: Support versioning and iteration tracking of DSL-based teaching sequences and post-class analysis.

🔝 [↑ Back to Table of Contents](#table-of-contents)

## 9.Invitation to Join
If you are:
A teacher or educator
An AI tool designer or developer
A curriculum designer
A linguist or education researcher

We warmly invite you to collaborate, test, propose syntax extensions, share usage cases, and co-create the world’s first AI teaching language centered on teachers × learners.

🔝 [↑ Back to Table of Contents](#table-of-contents)
