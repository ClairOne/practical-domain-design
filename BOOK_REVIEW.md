# Practical Domain Design - Complete Manuscript
**Generated:** Fri Oct 10 07:58:19 AM EST 2025
**Repository:** https://github.com/ClairOne/practical-domain-design
**Analysis URL:** https://raw.githubusercontent.com/ClairOne/practical-domain-design/main/BOOK_REVIEW.md

---

## 📖 Part 1 - The Problem & The Fix/1.1.introduction.md

# Chapter 1.1: Introduction / Overview

## Why another book?

I’ve spent 30 years building software — wearing every hat from developer to DBA to product owner. I’ve seen Agile sprints devolve into ticket shuffles, Scrum ceremonies turn into theater, and DDD grind to a halt in translation debates. I loved the ideas, but in practice they were either too heavy, too vague, or too fragile.

So I built something different: **Feedback Loops.**

Feedback Loops are a lightweight, repeatable way to keep business and tech aligned while you ship software that actually solves the right problems. The core is simple: **Baseline → Loop → Canon.** Capture what is, run a thin slice of change, then lock in what worked as the new truth. Repeat until you’re bored of winning.

And the glue that makes it all practical? **Practical Domain Design (PDD).** These are the artifacts — maps and docs — that capture how the business and the system really work. Not theory. Not a 200-page spec. Just enough clarity to keep everyone on the same page.

---

## Who this book is NOT for

This isn’t a Software Development 101 or Project Management 101 book. If you’re looking to learn how to code, manage a sprint board, or figure out what a BA or software architect does from scratch — this isn’t it. We assume you’ve been around the block. You already know the basics, the roles, and the lingo.

This book is for skimmers and doers. If you need in‑depth explanations of common software concepts, most of what follows will fly right over your head. We won’t hold your hand on fundamentals — we’ll show you how to run Feedback Loops and build Practical Domain Design artifacts that cut through the noise.

## Who this book is for

If you’re on a small product team drowning in chaos — napkin requirements, ops firefights, QA chasing ghosts, devs guessing what the business really wanted — this book will give you structure without the overhead.

If you’re in a large enterprise — with Jira backlogs that groan under their own weight, committees for every decision, and slide decks that say a lot but change little — Feedback Loops scale up. They create traceability from the first pain point all the way to shipped code and back again.

---

## What this book will teach you

We’ll walk step by step through:

1. **Spotting the real problem.** Why traditional methods collapse in practice.
2. **Learning the Feedback Loop pattern.** Baseline → Loop → Canon.
3. **Running the Strategic Loop.** Capturing pain points, validating problems, framing vision, and producing a PRD plus business-facing Practical Domain Design.
4. **Running the Tactical Loop.** Translating PRDs into technical design, code, and technical-facing PDD artifacts.
5. **Making it Canon.** How to lock in what worked as the new shared truth.
6. **Keeping it alive.** How to handle drift, growth, and the messy reality of shipping software.

By the end, you won’t have a binder of theory. You’ll have a handful of living artifacts, a loop your team can actually run, and a way to evolve design without burning out.

---

## What next

You can dip into the case studies to see how this plays out in real, funny, and sometimes disastrous situations. Or you can skip ahead to Part 1, where we unpack why popular methodologies trip teams up and how Feedback Loops fix the gaps.

Either way, you’ll be ready to see how this system keeps both business and tech honest, aligned, and moving forward.

---

👉 In short: This isn’t another process fad. **Feedback Loops are the engine. Practical Domain Design is the map. Together they make shipping software sane again.**

---

## 📖 Part 1 - The Problem & The Fix/1.2.why-popular-methodologies-trip-us-up.md

# Chapter 1.2: Why Popular Methodologies Trip Us Up

Every shiny methodology promises to save us from chaos. Waterfall promised predictability. Agile promised speed. Scrum promised teamwork. DDD promised clarity. And yet, here we are in 2025 — still drowning in rework, mistranslation, and late-night fire drills.

The problem isn’t that these approaches are *wrong*. It’s that they assume conditions that almost never exist in real life: clear requirements, stable goals, and teams who magically speak the same language. When reality doesn’t match the theory, teams stumble into the same traps over and over.

Let’s break it down.

---

## 1.2.1 Waterfall Woes

Waterfall works when you’re building a bridge. You know the river won’t move halfway through construction. Software? Not so much.

The idea: gather all the requirements upfront, design it all, build it, test it, ship it. Neat, linear, controlled.

The reality: by the time you deliver, the business has changed, the users want something else, and your beautiful plan is already obsolete. Feedback arrives only at the very end, when it’s most expensive to act on. That “predictability” comes at the cost of massive waste.

---

## 1.2.2 Agile & Scrum Theater

Agile started as a manifesto with values we all agree on. But somewhere along the way, it became cargo cult. Teams measure “velocity” like it’s a blood pressure reading, hold standups that are just status recitals, and run sprint reviews where half the features demoed don’t even matter.

Scrum made it worse by scripting ceremonies into rigid theater:

* Standups: everyone reports what they did, nobody collaborates.
* Sprint reviews: awkward half-demos to polite applause.
* Retros: gripe sessions with no follow-through.

The backlog bloats, the ceremonies keep rolling, and actual alignment fades. You’re agile in name, but in practice it’s theater.

---

## 1.2.3 DDD: Great in Theory, Hard in Practice

Domain-Driven Design was a leap forward. Finally, a way to make the business and devs talk about the same problems. The artifacts are genuinely useful for developers.

But adoption is brutal. The learning curve is steep, the diagrams are intimidating, and the “ubiquitous language” idea turns into endless arguments about whether to call it a customer, client, or account. Translation debt piles up faster than tech debt.

DDD shines in greenfield projects with time to spare. In messy, fast-moving environments, it often collapses under its own weight.

---

## 1.2.4 The Common Pitfalls Across All

Different methods, same problems:

* **Translation fatigue** – Business says one thing, tech hears another, and everyone nods while building the wrong thing.
* **Decision ping-pong** – Choices bounce between teams until deadlines make them for us.
* **Lack of traceability** – No clean line from pain point → requirement → code.
* **Ceremony over outcomes** – More focus on rituals than results.

Sound familiar? That’s because the root problem is the same: we keep treating design as a one-time event instead of a continuous process.

---

## 1.2.5 What We Actually Need

What teams actually need isn’t another methodology layered on top. We need:

* A **lightweight, repeatable system** that doesn’t collapse under real-world chaos.
* A way to **connect business and tech** without forcing them to speak the same language.
* A rhythm that works for both **startups** (fast, messy) and **enterprises** (big, political).

In other words: we need **Feedback Loops.**

Feedback Loops don’t throw out Agile, Scrum, or DDD. They modernize them. They give teams a pattern that works even when the ground shifts under their feet.

That’s where we go next.

---

## 📖 Part 1 - The Problem & The Fix/1.3.the-feedback-loops-fix.md

# Chapter 1.3 The Feedback Loops Fix

So if Agile, Scrum, DDD, and all the rest aren’t *wrong*, why do so many teams still crash and burn when they follow them? Because they’re optimized for theory, not today’s reality. Most frameworks assume clean backlogs, neat handoffs, and stakeholders who magically speak the same language. That’s not how real teams live.

Reality check: today’s teams are juggling remote work, cloud services, spaghetti legacy systems, and business expectations that change by the week. You don’t need more ceremony. You need a system that keeps everyone aligned even when the ground shifts under your feet.

That’s where **Feedback Loops** come in.

---

## a. Core Idea: Loops, Not Linear

Instead of one-and-done handoffs, Feedback Loops treat design as an ongoing cycle. Each loop is a self-contained engine:

1. **Baseline** – Capture the current state.
2. **Loop** – Run thin-slice experiments from pain point → solution.
3. **Canon** – Lock in what worked as the new truth.

Then repeat. Over and over. The rhythm creates alignment without endless meetings.

👉 Think of it like muscle memory. The more loops you run, the stronger and faster your team gets.

---

## b. Two Worlds, Same Pattern

We run **two loops in parallel**:

* **Strategic Loop (Business)** – Captures departments, workflows, operations, and business entities. Produces PRDs and business-facing Practical Domain Design maps.
* **Tactical Loop (Tech)** – Captures modules, actions, services, and models. Consumes PRDs + business maps, then produces code, technical maps, and docs.

Both use the same pattern: Baseline → Loop → Canon. The outputs of one feed the other. Strategic defines the *what* and *where it fits*. Tactical defines the *how*. Together, they keep business and tech in sync without pretending they speak the same language.

---

## c. Why Feedback Loops Beat Theater

Other frameworks collapse at the handoff:

* Agile devolves into ticket-shuffling.
* Scrum becomes sprint ceremonies with no heartbeat.
* DDD stalls in translation fights over terminology.

Feedback Loops solve this by:

* Making translation explicit through **Practical Domain Design artifacts** (business maps + technical maps).
* Building traceability: every line of code can be traced back to an original pain point.
* Keeping alignment alive: each Canon update refreshes both sides.

---

## d. In Short

Feedback Loops don’t replace Agile, Scrum, or DDD. They modernize them. They’re the glue that keeps strategy and tactics connected, so teams can adapt quickly *without* losing alignment.

* Strategic Loop = design the business.
* Tactical Loop = design the system.
* Canon = the shared, living truth.

That’s the fix: **loops instead of theater, artifacts instead of guesses, and alignment that sticks.**

---

## 📖 Part 1 - The Problem & The Fix/1.4.practical-domain-design.md

# Chapter 4: Practical Domain Design

Feedback Loops are the engine. But an engine without wheels doesn’t get you far. That’s where **Practical Domain Design (PDD)** comes in. These are the artifacts — the maps and documents — that give shape to the loops. They’re lightweight enough for small teams, structured enough for big enterprises, and always traceable back to the original pain point.

Without artifacts, loops are just meetings. With artifacts, loops create a living body of truth everyone can see, use, and trust.

---

## a. Why Artifacts Matter

Most teams don’t fail because they lack ideas. They fail because ideas get lost in translation:

* Business says one thing, devs hear another.
* QA tests the wrong acceptance criteria.
* Ops inherits a feature no one explained.

Artifacts fix that. They:

* **Anchor conversations** in shared documents, not opinions.
* **Create traceability** from pain point → PRD → code.
* **Prevent rework** by forcing clarity early, when it’s cheap.

👉 In short: artifacts are the receipts. They prove why you built what you built, and how it ties back to real business problems.

---

## b. PDD in the Strategic Loop

On the business side, loops generate these artifacts:

* **Business Pain Point Entry (PPE)** – Catch the smoke early.
* **Problem Validation Brief (PVB)** – Prove the fire is real.
* **Vision & Problem Statement (VPS)** – Paint the better world.
* **Requirements Brief (RB)** – Define what must be true.
* **Product Requirements Document (PRD)** – Package the bet we’re making.
* **Business Map (Strategic PDD)** – Place the solution in context: departments → workflows → operations → entities.

This last step is critical. The PRD describes the solution in isolation. The Business Map shows where it fits in the larger system and exposes potential conflicts before they reach code.

---

## c. PDD in the Tactical Loop

On the tech side, loops consume the Strategic artifacts and produce Tactical ones:

* **Inputs:** PRD + Business Map.
* **Outputs:**

  * **Technical Map (Tactical PDD)** – Modules → Actions → Services → Models.
  * **Code** – The working system that meets the business need.

Example:

* Business Map: *Workflow → Manage Teams; Operation → Team.addCoach; Entity → Team.*
* Technical Map: *Module → Team; Action → ManageTeam; Service.Function → TeamService.addCoach(); Model → Team.*

The mirroring makes traceability automatic. Business designs in their terms, tech implements in theirs, and the maps line up without forcing a “ubiquitous language” nobody actually uses.

---

## d. The Symmetry

Strategic and Tactical PDD artifacts are mirrors:

* **Department ↔ Domain/Module**
* **Workflow ↔ Action**
* **Operation ↔ Service.Function**
* **Entity ↔ Model**

This symmetry is what makes PDD powerful. It lets each side work in their own language while keeping the maps aligned. Every pain point can be traced all the way to a line of code, and every line of code can be traced back to a business problem.

---

## e. In Short

Feedback Loops keep the system moving. **Practical Domain Design provides the map.** Together they:

* Keep business and tech aligned without forcing them to fake fluency.
* Prevent “lost in translation” disasters.
* Ensure every solution fits both the business context and the codebase.

👉 Loops are motion. PDD is structure. That’s how you ship features that work, make sense, and don’t torch your weekends.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.0.0.strategic-feedback-loop-overview.md

# Chapter 2.0.0 Strategic Feedback Loop Overview

The **Strategic Feedback Loop** is where business reality gets captured, tested, and translated into living artifacts. It’s not about wishful thinking or future-state diagrams. It’s about running a repeatable cycle that turns raw pain points into validated business designs everyone can agree on.

The pattern is the same as every loop in this book: **Baseline → Loop → Canon.**

---

## Purpose

The Strategic Loop gives the business side of the house a clear rhythm:

* **Baseline:** Capture how the business *actually* runs today (departments, workflows, operations, entities).
* **Loop:** Take new pain points, validate them, shape vision, define requirements, and produce a PRD plus a Strategic PDD (Business Map).
* **Canon:** Lock in what worked as the new shared truth, so the next loop starts from reality, not fiction.

This isn’t BA theater. It’s structured momentum. Each cycle creates artifacts that are small, lightweight, and traceable all the way to tactical work.

---

## Burning Questions It Answers

* How do we capture what’s really happening in the business without drowning in documentation?
* How do we know which problems are real and worth solving?
* How do we ensure the “fix” fits into the bigger business picture?
* How do we keep everyone aligned as the business evolves?

---

## Why It Matters

Most teams either under-document (chaos) or over-document (paralysis). The Strategic Loop threads the needle: just enough structure to prevent waste, but not so much that you spend all day making diagrams nobody reads.

It also creates **traceability**:

* Pain Point → Validation → Vision → Requirements → PRD → Strategic Domain Design → Canon.

That chain of custody means when someone asks “why are we building this?” you don’t shrug — you point straight to the artifact trail.

---

## In Short

The Strategic Feedback Loop is the business engine of PDD. It keeps pain points from getting lost, turns ideas into validated requirements, and maps them into the business context before anything ever hits code. It’s how business stops lobbing requests over the wall and starts co-owning the design of the system.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.1.0.strategic-baseline.md

# Chapter 2.1.0 Strategic Baseline Overview

Every loop starts with a **Baseline**. For the Strategic Loop, that means capturing how the business really works today — not the glossy slide deck version, not the wishful-thinking version, but the messy, duct-taped, real-world version.

Think of the Baseline as your starting map. You can’t plan a road trip if you don’t know where you’re starting. The Strategic Baseline is that “you are here” marker.

---

## Purpose

The Strategic Baseline provides a shared snapshot of business reality:

* **Departments** – The big buckets of responsibility.
* **Workflows** – The repeatable processes those departments run.
* **Operations** – The atomic steps inside workflows.
* **Entities** – The nouns the business cares about (customers, invoices, tickets, etc.).

It’s not about fixing anything yet. It’s about agreeing on the current state so you have a foundation to build from.

---

## Burning Questions It Answers

* What are the major departments we rely on?
* What workflows actually happen day to day?
* What operations make those workflows run?
* What business entities do we touch across teams?

---

## Why It Matters

Without a baseline, every conversation becomes a game of telephone. Marketing swears support “always” drops tickets, support says billing is the bottleneck, billing blames sales. Nobody has the same picture.

The Strategic Baseline kills the guessing game. It makes the invisible visible. Once it’s documented, you can:

* Spot overlaps and conflicts across departments.
* Onboard new people without 3 weeks of tribal-knowledge download.
* Build traceability into future loops.

👉 It’s the difference between arguing about what’s true and agreeing on what’s real.

---

## In Short

The Strategic Baseline is your starting map. It doesn’t solve problems — it shows you where you actually are. And without it, every loop risks starting from fantasy instead of reality.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.1.1.concept-establish-the-strategic-baseline.md

# Chapter 2.1.1 Strategic Baseline – Documenting the Business

Every team thinks they know how their business runs… until they try to write it down. Suddenly the “simple” billing process has six hidden detours, and Support’s “standard” workflow turns out to be fifty shades of chaos.

That’s why every **Strategic Feedback Loop** starts with a **Baseline**. This isn’t about fixing anything or debating best practices. It’s about taking a snapshot of how the business actually operates today — warts, duct tape, and all.

Think of it like a map: you can’t plan a road trip until you know where you’re starting. The Baseline is that “you are here” marker.

---

## The Four Building Blocks

When documenting the business, capture four simple pieces:

* **Departments** – Big buckets of responsibility.
* **Workflows** – The repeatable processes those departments run.
* **Operations** – The atomic steps inside each workflow.
* **Entities** – The nouns the business deals with every day.

That’s it. No buzzwords. Just the terms people already use.

---

## Artifacts

Feedback Loops give you structure with flexibility. Each template plays a role at a different stage:

* **🧠 Strategic Baseline – Brain Dump**: Capture Departments, Workflows, Operations, and Entities in one messy table. Don’t worry about gaps. Just dump it.
* **🏢 Department Detail**: Zoom into each department. Describe what it does, who runs it, and the workflows it owns.
* **⚙️ Workflow Detail**: For each workflow, nail down the trigger, goal, and step-by-step operations.

👉 Think of it as layers: Brain Dump for breadth, Department Detail for context, Workflow Detail for depth. Pick the layer you need. That’s the flexibility of PDD — structured enough to guide you, loose enough to adapt.

---

## Success Criteria

You know your baseline is “good enough” when:

* You can show it to a new hire and they nod instead of squinting.
* Nobody in the room says “that’s not how we do it.”
* Each department or module fits on a single screen. If it sprawls, split into sub-baselines instead of one giant hairball.

---

## Why It Matters

* **Shared reality:** Everyone stops pretending they know how things work and actually sees it on paper.
* **Foundation for backlog:** You can’t capture pain points if you don’t know the workflows they belong to.
* **Low effort, high return:** Two hours of mapping saves weeks of guesswork later.

---

👉 In short: The Baseline is just holding up a mirror. Don’t polish it. Don’t overcomplicate it. Just capture what *is*. The fixing comes later, in the Loop.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.1.2.sop-establish-the-strategic-baseline.md

# Chapter 2.1.2 Strategic Baseline – SOP

The **Strategic Baseline** is the first step of the Strategic Feedback Loop. Think of it as building a simple map of how your business really works — not the slide-deck fantasy, not the way leadership *wishes* it ran, but the way it actually runs day to day.

This isn’t theory. It’s an SOP you can follow like a recipe. By the end, you’ll have a set of lightweight artifacts that make the invisible visible.

---

## ✅ Quick Checklist

1. Gather the team in a room (or a shared doc).
2. Brain dump all departments.
3. Assign an owner to each department.
4. Brain dump workflows under each department.
5. Split into department huddles to break workflows into operations and entities.
6. Each team assembles a scratchpad map for its department.
7. Owners present maps, group provides feedback.
8. Collect and refine Department Detail docs.

That’s it. One session gets you from fuzzy guesses to a shared Strategic Baseline.

---

## Step 1 – Brain Dump Departments (and Assign Owners)

* List **all departments** in the business.
* Ask: “If payroll cuts a check for it, is it a department?”
* Assign a business owner — not necessarily a manager, but the person who knows the work well enough to own the map.

**Output artifact:** A list of departments with assigned owners.

👉 Don’t debate org charts. Focus on functional buckets of work.

---

## Step 2 – Brain Dump Workflows

* For each department, list its repeatable processes.
* Ask: “When X happens, what do we do that results in Y?”
* Keep it short and high-level.

**Output artifact:** A rough list of workflows under each department.

👉 Capture what people *say* they do. Refinement comes later.

---

## Step 3 – Break Workflows into Operations

* Split into department huddles.
* Break each workflow into **operations** (verb + entity, e.g., `Invoice.create`).
* If it takes branches or approvals, it’s a separate workflow.

**Output artifact:** A short list of operations under each workflow.

---

## Step 4 – Capture Entities

* Entities are the **nouns** your business touches (Customer, Invoice, Ticket).
* Scan operations for nouns and list them.
* Note where entities cross department lines — overlaps matter later.

**Output artifact:** A list of entities for each department.

---

## Step 5 – Assemble Scratchpad Maps

* Map each department: Departments → Workflows → Operations → Entities.
* Don’t worry about size or balance.

**Output artifact:** A Strategic Baseline scratchpad map per department.

👉 Uneven maps aren’t wrong — they’re clues. Overloaded? Under-defined? Both are signals for future loops.

---

## Step 6 – Present and Review

* Department owners present their maps.
* Group asks: “Does this look real? What’s missing? Who else is impacted?”
* Capture updates live.

**Output artifact:** Validated Department Detail docs.

---

### Success Criteria

Your baseline is ready when:

* A new hire nods instead of saying, “That’s not how we do it.”
* Each department has an owner confirming workflows.
* Differences across maps point to questions, not confusion.

👉 In short: Don’t polish the map to make it pretty. Capture what’s real. Messy beats imaginary every time.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.1.3.workshop-establish-the-strategic-baseline.md

# Chapter 2.1.3 Strategic Baseline – Workshop

This isn’t a stiff agenda — it’s a playbook. The goal: get everyone in a room, cut through the fantasy versions of “how we work,” and by lunch you’ll have a Strategic Baseline instead of hot air.

---

## 🕘 9:00 – Kickoff (15 min)

* Welcome the group.
* Explain the goal: *“By lunch, no more mystery workflows hiding under the carpet. We’ll have a map of how this circus really runs.”*
* Quick overview: Brain dump → Deep dive → Present & review.

---

## 📝 9:15 – Brain Dump Departments & Workflows (45 min)

* List all departments.
* List the main workflows under each department.
* Assign an owner for each department.
* Stop when most heads are nodding and nobody’s starting a fistfight.

**Output artifact:** A master list of departments, owners, and high-level workflows.

---

## 👥 10:00 – Department Huddles: Deep Dive (60 min)

* Split into department groups (stay in the same room).
* Each group:

  * Breaks workflows into operations.
  * Captures entities touched by those operations.
  * Assembles a scratchpad map (Dept → Workflows → Operations → Entities).

**Facilitator’s role:** Float between groups, answer questions, keep momentum up.

**Output artifact:** Department scratchpad maps.

---

## 🍴 11:00 – Lunch & Presentations (60 min)

* As people eat, department owners present their maps.
* Encourage blunt but constructive feedback:

  * “Does this look like reality?”
  * “What’s missing?”
  * “Who else is impacted by this?”
* Update maps live.

**Output artifact:** Validated Department Detail docs.

---

## ✅ 12:00 – Wrap-Up & Next Steps (15 min)

* Recap what was captured.
* Highlight obvious gaps or lopsided departments (signals for backlog).
* Explain where this leads: *“These baselines set us up for the next Feedback Loop.”*

**Final Output:** A complete Strategic Baseline across departments, ready for the Strategic Loop.

---

👉 In short: Half a day, lock the team in a room, and walk out with artifacts that actually reflect reality instead of PowerPoint fantasy.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.1.4.ai-establish-the-strategic-baseline.md

# Chapter 2.1.4 Strategic Baseline – AI Assisted

Sometimes you don’t want to wrangle sticky notes and whiteboards. Maybe your team is remote, maybe nobody wants to play facilitator, or maybe you just want the artifacts to come out clean from the start. That’s where the **AI-assisted version of the Strategic Baseline** comes in.

The process is the same as the manual SOP, but instead of stopping at scratchpads, you feed raw notes into prompts that generate polished baseline docs. The AI doesn’t replace judgment — it just handles the grunt work of formatting, structuring, and cross-referencing.

---

## ✅ Quick Checklist

1. Use the **Interview Prompt** to gather raw notes from department owners and SMEs. Capture the messy, conversational version of “how we actually work.”
2. Feed those notes into the **Department Detail Prompt** to structure each department’s map of workflows, operations, and entities.
3. For workflows needing more depth, run the **Workflow Detail Prompt** to expand into operations and entity touchpoints.
4. Review the AI outputs as a group — check accuracy, fill gaps, and correct mistakes.
5. Save the generated docs as your baseline artifacts (Department Detail, Workflow Detail, etc.).

---

## 🔧 Prompt Map

| Step                  | Output Artifact           | Prompt to Use            |
| --------------------- | ------------------------- | ------------------------ |
| Capture messy reality | Strategic Baseline notes  | Interview Prompt         |
| Structure departments | Department Detail drafts  | Department Detail Prompt |
| List workflows        | Workflow Detail drafts    | Workflow Detail Prompt   |
| Break into operations | Workflow + Operations map | Workflow Detail Prompt   |
| Capture entities      | Entity List (baseline)    | N/A (list only)          |
| Assemble baseline     | Strategic Baseline Map    | Combine outputs above    |

👉 See the Appendices for copy-paste ready prompt templates.

---

## Success Criteria

* AI outputs structured, consistent docs for every department.
* Group review and validation is complete (AI is fast, not infallible).
* Everyone agrees the docs reflect *reality*, not just AI guesses.
* Entities are captured as a simple list for now — detailed docs come later during the Loop.

---

👉 In short: Run the same workshop flow, but let AI handle the documentation grunt work. Humans still confirm what’s true, but you’ll walk away with clean, shareable artifacts in a fraction of the time.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.2.0.strategic-loop-overview.md

# 2.2.0 Strategic Loop Overview

The Baseline gave us a snapshot - a mirror showing how the business really runs today. The Loop is what turns that snapshot into motion. It’s the engine of Feedback Loops: every new pain, idea, or risk enters the loop, gets translated into shared artifacts, and comes out the other side as a validated decision or a parked item. Then it repeats. Simple, structured, and brutally effective.

---

## What is the Loop?

The Loop is a **repeatable feedback cycle** that turns messy business input into testable bets. It’s not a meeting, it’s not theater for theater’s sake - it’s the operating system for how decisions move from *“someone raised their hand”* to *“this shipped and we know if it worked.”*

At its core, the Loop:

1. **Captures** pain points in business terms.
2. **Validates** if the problem is real and worth solving.
3. **Frames** a vision of the better state and ties it to company goals.
4. **Defines** requirements in plain business language.
5. **Packages** it all into a Product Requirements Document (PRD) that feeds the tactical side.

Each pass through the Loop ends in a decision: **go, pivot, or park.**

---

## Baseline vs Loop

* **Baseline = Snapshot.** It’s the “before photo” of how things work today - departments, workflows, operations, entities - frozen so we know our starting point.
* **Loop = Motion.** It’s the treadmill that keeps the business honest. Every new problem runs the same course, producing artifacts and decisions.

👉 Without a baseline, you’re improving in a vacuum. Without a loop, your baseline becomes a museum exhibit. Together, they give you both clarity (where we are) and momentum (how we improve).

---

## Do You Need a Baseline First?

No. The Loop works from day 1, even if there’s no existing baseline. If you have no history, the first passes through the Loop *become* your baseline. If you do have an existing operation, a quick baseline helps you spot drift faster, but don’t wait on paperwork to start. Rule of thumb: **start the Loop, let artifacts create the minimum baseline you need.**

---

## FAQs About the Loop

**Is this just Agile with new words?**
No. Agile describes values and ceremonies. The Loop is a concrete sequence with defined artifacts and exit criteria. It doesn’t replace Agile - it gives Agile teams a spine.

**Does this add more paperwork?**
No. Each artifact answers a specific question that *must* be answered sooner or later. By tackling them in the Loop, you solve them early and cheaply instead of after release when fixes are expensive. Artifacts are short by design - a page or two, not a binder.

**Who runs the Loop?**
Each step has an owner. On the strategic side it’s often the product owner or business analyst. On the tactical side it might be a PM. Titles don’t matter - roles do. PDD defines clear hats: reporter, validator, owner, stakeholder. No more *“I thought you were handling that.”*

**How long does it take?**
From Pain Point to PRD, a simple issue might take hours. A complex one, days. With AI prompts, you can start from a vague one-liner and build a PRD in under an hour. Cadence is flexible - weekly heartbeat plus ad-hoc urgent cycles. The key is consistency: **every issue takes the same path, no side doors.**

**Why should I care?**
Because the Loop kills the two biggest killers of delivery: **translation fatigue** (everyone guessing what the other side meant) and **decision ping-pong** (choices bouncing until deadlines make them for us). The Loop doesn’t just give speed - it gives confidence that speed isn’t sending you in circles.

---

## Real-World Example

*Customer Support Backlog*
Baseline showed that support tickets lived in 3 different systems. A rep raised a pain point: customers wait 5+ days for refunds. The team logged it as a PPE, validated the delay with metrics (PVB), framed a vision of “refunds in under 24 hours” (VPS), defined clear requirements (RB), and packaged it into a PRD. The tactical team then picked it up knowing exactly why it mattered and how success would be measured. That’s the Loop in action.

---

👉 **In short:** The Baseline is your starting map. The Loop is the vehicle. Together they turn *“we think we know”* into *“we know, we acted, and here’s the proof.”* That’s the heart of Feedback Loops - clarity, motion, and decisions that stick.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.2.1.business-pain-point-entry.md

# 2.2.1 Business Pain Point Entry

Every fire starts with smoke. The Business Pain Point Entry (PPE) is how we catch that smoke early - before the fire spreads, before the backlog fills with noise, and before everyone is arguing over symptoms instead of causes.

This is the very first artifact in the Strategic Loop. It’s deliberately lightweight: a single page that captures what hurts, who it hurts, and how bad it stings. Nothing fancy, nothing polished - just enough clarity to make sure the problem doesn’t get lost.

---

## Purpose

The PPE exists to **capture pain points in business terms.** It turns vague complaints into structured input the team can track and act on. If you don’t capture the pain clearly here, the rest of the Loop risks chasing the wrong problem.

---

## Audience (Hats)

Anyone close to the work should be able to submit a PPE:

* Support agents hearing customer complaints
* Ops staff spotting bottlenecks
* Finance noticing billing errors
* Product managers seeing churn risks
* Engineers hitting repeated friction

👉 If you see smoke, you can file a PPE. Titles don’t matter - proximity to the problem does.

---

## Burning Questions It Answers

* **What hurts?** A crisp description of the problem.
* **Who’s feeling it?** The team, customers, or both?
* **How bad does it sting?** The immediate impact on time, money, or sanity.

These sound simple, but nailing them early prevents weeks of rework later. You either spend 5 minutes here or 5 weeks after release when the “fix” didn’t actually fix the real problem.

---

## Why It Matters

Skipping PPE means relying on tribal knowledge and hallway conversations to carry business problems forward. That’s a recipe for translation fatigue, forgotten details, and mismatched expectations. A simple entry creates traceability - every artifact downstream ties back to the original pain point, building a clean chain of custody from complaint to solution.

PPE also builds momentum. It gives the reporter a quick win, and it gives the team something concrete to validate. With the AI prompts we provide, you can go from a vague one-liner to a clear PPE in under 5 minutes.

---

## Template

```
# Business Pain Point Entry

**Title:** [Concise, descriptive name]

**Description:** [1-2 sentences with key facts from user input]

**Impact:** [Clear effects mentioned by user]

**Type:** [Category selected by user]

**Date Logged:** [Today's date YYYY-MM-DD]

**Source/Reporter:** [Person/team who identified it]

**Evidence/Data:** [Metrics, examples, or "TBD - to be gathered"]

**Next Steps/Notes:** [User input or "TBD"]
```

---

👉 **In short:** The PPE is the smoke alarm for your business. Fast to fill out, impossible to ignore, and the foundation for everything else in the Feedback Loop.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.2.2.problem-validation-brief.md

# 2.2.2 Problem Validation Brief

A Business Pain Point Entry (PPE) captures the smoke. The Problem Validation Brief (PVB) is where we check if there’s an actual fire. Not every complaint deserves a project, and not every pain point is worth fixing right now. The PVB separates the real problems from the noise.

---

## Purpose

The PVB exists to **validate** whether a pain point is real, significant, and worth solving. It pulls in evidence, quantifies impact, and gets stakeholders aligned. Without this step, teams waste months chasing anecdotes or politics.

---

## Audience (Hats)

The PVB is owned and driven by the **Product/Business side**, but it pulls in voices from:

* **Product** – framing the problem clearly
* **Analytics/Data** – pulling proof from metrics and logs
* **Finance** – confirming cost/ROI impacts
* **Ops/Support Leads** – confirming the problem shows up in daily work

👉 Engineering may be consulted for feasibility hints, but the PVB is about proving the problem exists in business terms.

---

## Burning Questions It Answers

* **Is this pain real?** Do we have concrete evidence, not just opinions?
* **Can we prove it?** What observations and metrics back this up?
* **What’s the cost of ignoring it?** If we leave this alone, how bad will it get?
* **Who agrees?** Which stakeholders sign off that this is a real problem worth solving?

---

## Why It Matters

Skipping validation is how “zombie projects” are born - initiatives with no evidence, no measurable impact, and no defenders once things get tough. The PVB keeps the backlog honest. It makes sure energy only goes into problems with proof, alignment, and stakes.

PVBs also act as insurance. Later, when someone asks *“Why are we working on this?”* you can point back to the evidence, quantified impact, and stakeholder alignment. No more shrugging or digging through old Slack threads.

---

## Template

```
# Problem Validation Brief

## 1. Problem Description
[Clear description without solutions - who/what affected, when/where it occurs]

---

## 2. Evidence & Observations
- [Evidence item 1]
- [Evidence item 2]
- [Evidence item 3]

---

## 3. Quantified Impact
- **[Metric name]:** [Value + explanation]
- **[Metric name]:** [Value + explanation]
- **[Metric name]:** [Value + explanation]

---

## 4. Validation Sources
- [Source 1]
- [Source 2]
- [Source 3]

---

## 5. Cost of Inaction
[Describe likely outcome if problem not fixed]

---

## 6. Stakeholder Alignment
- **[Role/Title]:** [Agreement or statement]
- **[Role/Title]:** [Agreement or statement]
- **[Role/Title]:** [Agreement or statement]

---

## 7. Initial Scope Boundaries
- **In Scope:** [Key activities/areas included]
- **Out of Scope:** [Exclusions to prevent scope creep]
```

---

👉 **In short:** The PVB is your bullshit filter. It separates signal from noise, backs it with evidence, and ensures everyone agrees the fire is real before you call in the fire brigade.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.2.3.vision-problem-statement.md

# 2.2.3 Vision & Problem Statement

The Problem Validation Brief (PVB) proved the fire is real. The Vision & Problem Statement (VPS) is where we decide what a better world looks like once the fire is out - and why it matters strategically. It connects the validated problem to a motivating, measurable future state.

---

## Purpose

The VPS exists to **paint the better world and tie it to strategy.** It reframes the problem into a vision the business can rally around, defines measurable objectives, and shows how this effort aligns with company goals.

---

## Audience (Hats)

The VPS is typically crafted and owned by the **Business side**, with input from:

* **Business Owner / Product Lead** – drives the vision
* **Finance** – ensures alignment with budgets and ROI
* **Ops / Compliance** – surfaces constraints
* **Customer / Stakeholder Reps** – ground the vision in reality
* **Engineering Lead** – consulted for feasibility checks

👉 This is where strategy, not tactics, takes center stage.

---

## Burning Questions It Answers

* **Where do we want to go?** What does success look like in concrete terms?
* **Why now?** What’s the urgency or driver making this worth doing?
* **How does this tie to company goals?** If it doesn’t ladder up, why bother?
* **What constraints matter?** Budget, compliance, or technical realities that can’t be ignored.

---

## Why It Matters

Vision without measures is just a pep talk. Measures without vision lead to local optimizations that miss the point. The VPS locks both together. It gives leadership a quick, strategic read (*“does this matter to the business?”*) and gives teams a north star to navigate by.

It also anchors everything that follows: requirements, PRDs, tactical designs. Without a clear VPS, you risk building things that solve the wrong problem or solve the right problem in a way no one cares about.

---

## Template

```
# Vision & Problem Statement
**Phase 2: Vision Framing — Business Understanding**

---

## 1. Document Information
| Field | Value |
|-------|-------|
| **Document ID** | VPS-[YYYYMMDD]-[derived from problem] |
| **Version** | 0.1 (Draft) |
| **Date Created** | [Today's date] |
| **Author(s)** | [User name if provided] |
| **Status** | Draft |

---

## 2. Executive Summary
[3-5 sentence summary combining problem + vision + strategic importance]

---

## 3. Problem Statement
**3.1 Problem Description**
[Pull from PVB - business-friendly language]

**3.2 Evidence of the Problem**  
[Pull evidence from PVB]

**3.3 Root Causes (if known)**
[Extract from PVB if available, or "TBD - requires further analysis"]

---

## 4. Business Impact
| Impact Area | Description | Severity | Evidence |
|-------------|-------------|----------|----------|
| Financial | [From user input] | [H/M/L] | [From PVB] |
| Customer | [From user input] | [H/M/L] | [From PVB] |
| Operational | [From user input] | [H/M/L] | [From PVB] |

---

## 5. Vision Statement
[User's ideal future state - inspiring and measurable]

---

## 6. Objectives & Desired Outcomes
| Objective | Description | Success Measure |
|-----------|-------------|-----------------|
| [O1] | [From user input] | [KPI/metric] |
| [O2] | [From user input] | [KPI/metric] |

---

## 7. Strategic Alignment
[How this aligns with company goals - from user input]

---

## 8. Constraints & Considerations
[Budget, timeline, technical, compliance constraints from user]

---

## 9. Stakeholder Overview
| Name | Role | Interest/Influence | Notes |
|------|------|-------------------|-------|
| [Stakeholders from user input with roles] |

---

## 10. Approval
| Name | Role | Signature | Date |
|------|------|-----------|------|
| [Key stakeholders] | | | |
```

---

👉 **In short:** The VPS is your north star. It ties a validated problem to a compelling future, with measures and alignment baked in. No vision, no direction. With vision, every next step makes sense.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.2.4.requirements-brief.md

# 2.2.4 Requirements Brief

The Vision & Problem Statement gave us the north star. The Requirements Brief (RB) is where we translate that vision into clear, testable requirements the whole team can agree on. It’s not about design or solutions yet - it’s about drawing the lines that define what “done” really means.

---

## Purpose

The RB exists to **turn vision into business-level requirements that are clear, scoped, and testable.** It ensures everyone agrees on the problem definition, goals, constraints, and success indicators before tactical design begins.

---

## Audience (Hats)

The RB is owned by **Product**, with strong input from:

* **Business Owner** – sets the boundaries of value
* **QA Lead** – ensures requirements are testable
* **Ops/Support** – highlights operational impacts
* **Dev Lead** – sanity-checks feasibility
* **Compliance/Legal** – if applicable, ensures constraints are captured

👉 Think of this as the handshake document across all roles before anyone writes code.

---

## Burning Questions It Answers

* **What must be in scope?** The core capabilities needed to realize the vision.
* **What must stay out of scope (for now)?** The guardrails to prevent scope creep.
* **What business rules and constraints matter?** Compliance, timelines, budgets, technical realities.
* **What risks are lurking?** Dependencies or threats that could derail progress.
* **What does success look like?** Clear acceptance signals agreed on by all.

---

## Why It Matters

Projects go off the rails when scope and rules are fuzzy. The RB prevents that by forcing clarity early. It also builds traceability: every requirement ties back to the validated problem and vision. Later, when questions come up (*“Why are we building this?”*), the RB provides the receipts.

It’s also the antidote to endless back-and-forth during sprints. With clear, business-level requirements, QA and devs can test outcomes instead of guessing intent. Everyone saves time.

---

## Template

```
# Requirements Brief
**Phase 2: Requirements Definition — Business Understanding**

---

## 1. Document Information
| Field | Value |
|-------|-------|
| **Document ID** | RB-[YYYYMMDD]-[derived from problem] |
| **Version** | 0.1 (Draft) |
| **Date Created** | [Today's date] |
| **Status** | Draft |

---

## 2. Purpose
This document refines the validated business problem into clear, testable requirements, ensuring all stakeholders agree on scope, constraints, and success indicators before moving to technical design.

---

## 3. Problem Context Summary
**Pain Point Recap:** [From PVB]  
**Business Impact:** [From Vision doc]  
**Why Now:** [Strategic drivers from user input]

---

## 4. Goals & Objectives
| Goal | Description | Priority | Success Measure |
|------|-------------|----------|-----------------|
| [From Vision doc objectives] |

---

## 5. Scope
### In Scope
[User-defined included capabilities]

### Out of Scope  
[User-defined exclusions]

---

## 6. Stakeholders & Roles
[Table with stakeholders, roles, responsibilities]

---

## 7. Functional Requirements (Business-Level)
| ID | Requirement Statement | Priority | Acceptance Criteria |
|----|----------------------|----------|---------------------|
| FR-1 | [User requirements in business language] | H | [Measurable criteria] |

---

## 8. Non-Functional Requirements (Business-Level)
| ID | Category | Requirement | Priority |
|----|----------|-------------|----------|
| NFR-1 | Performance | [Performance standards] | H |
| NFR-2 | Compliance | [Compliance requirements] | H |

---

## 9. Constraints & Assumptions
### Constraints
[Technical, business, regulatory constraints]

### Assumptions  
[Key assumptions about resources, data, systems]

---

## 10. Dependencies & Related Initiatives
| Dependency | Description | Impact if Not Met |
|------------|-------------|-------------------|
| [Critical dependencies] |

---

## 11. Risks & Mitigation
| Risk | Likelihood | Impact | Mitigation Strategy |
|------|------------|--------|-------------------|
| [Key risks with mitigation plans] |

---

## 12. Acceptance Signals (Exit Criteria for Phase 2)
- All stakeholders agree on problem definition, goals, and scope
- Functional and non-functional requirements documented at business level  
- Success measures are clear and testable
- Constraints, dependencies, and risks identified

---

## 13. Approval
| Name | Role | Signature | Date |
|------|------|-----------|------|
| [Approval stakeholders] | | | |
```

---

👉 **In short:** The Requirements Brief is your contract for clarity. It keeps scope creep out, ties requirements back to vision, and defines what “done” means before anyone touches code.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.2.5.product-requirements-doc.md

# 2.2.5 Product Requirements Document (PRD)

The Requirements Brief defined what must be true for success. The Product Requirements Document (PRD) is where those requirements are packaged into a single, business-facing spec that’s clear, testable, and ready for the tactical side to pick up without guesswork.

---

## Purpose

The PRD exists to **package the business solution in a way that’s ready for tactical translation.** It ties together the validated problem, the vision, and the requirements into a coherent business solution definition. If the PRD is fuzzy, the tactical work will be chaos.

---

## Audience (Hats)

The PRD is owned by **Product**, but it requires tight alignment from:

* **Business Owner** – confirms the solution matches the vision and ROI case
* **QA Lead** – ensures acceptance criteria and metrics are testable
* **Dev Lead** – sanity-checks feasibility before tactical planning
* **Ops/Support** – validates operational impacts and readiness
* **Compliance/Legal** – ensures regulatory constraints are captured

👉 This is the last stop before translation into technical design and backlog items.

---

## Burning Questions It Answers

* **What solution are we betting on?** The chosen business approach in plain terms.
* **Which capabilities and rules must exist?** The non-negotiables for the solution to work.
* **How will we measure success?** Clear KPIs and acceptance criteria that define “done.”
* **What risks or dependencies need attention?** Early warning before tactical planning starts.

---

## Why It Matters

If you can’t articulate the business solution clearly at this stage, you’re setting the tactical team up for endless interpretation and rework. The PRD is the handshake between strategy and tactics - the artifact that makes sure everyone is betting on the same horse before the race begins.

It also locks traceability: every line in the PRD ties back to the Requirements Brief, Vision, and Validation. No orphan requirements, no *“where did this come from?”* features.

---

## Template

```
# Product Requirements Document (PRD)
**Phase 3: Business Solution Definition — Tech-Agnostic**

---

## 1. Document Information
| Field | Value |
|-------|-------|
| **Document ID** | PRD-[YYYYMMDD]-[derived from problem] |
| **Version** | 0.1 (Draft) |
| **Date Created** | [Today's date] |
| **Author(s)** | [From Phase 2 or user input] |
| **Status** | Draft |

---

## 2. Purpose & Scope
**2.1 Purpose**
[Why this PRD exists - reference Phase 2 documents and business problem]

**2.2 Scope**
- **In Scope:** [From Requirements Brief + user input]
- **Out of Scope:** [From Requirements Brief + user input]

---

## 3. Background & Context
[Pull from Problem Validation Brief and Vision Statement]
- Summary of validated problem from Phase 1
- [Any historical context or current workarounds mentioned]
- Business drivers for addressing this now

---

## 4. Goals & Objectives
[Table from Vision & Problem Statement, refined with user input]
| Goal | Description | Priority | Success Measure |
|------|-------------|----------|-----------------|
| [From Phase 2 + user refinements] |

---

## 5. Proposed Business Solution
**Solution Summary:** [User's core business solution description]

**Key Capabilities:**
[3-5 critical capabilities from user input]
- [Capability 1]
- [Capability 2]
- [Capability 3]

**Business Rules:**
[Must-enforce rules from user input]
- [Rule 1]
- [Rule 2]
- [Rule 3]

**Assumptions:**
[Conditions that must be true from user input]
- [Assumption 1]
- [Assumption 2]
- [Assumption 3]

---

## 6. Functional Requirements
| ID | Requirement Statement | Priority | Acceptance Criteria |
|----|----------------------|----------|---------------------|
| FR-1 | [User's specific functional requirements in business terms] | H | [Measurable, testable criteria] |
| FR-2 | [Continue based on user input] | H/M/L | [Criteria] |
| FR-3 | ... | ... | ... |

---

## 7. Non-Functional Requirements (Business-Level)
| ID | Category | Requirement Statement | Priority |
|----|----------|----------------------|----------|
| NFR-1 | Performance | [User's performance expectations] | H |
| NFR-2 | Availability | [Uptime/availability requirements] | H |
| NFR-3 | Compliance | [Regulatory/policy requirements] | H |
| NFR-4 | Usability | [User experience standards] | M |

---

## 8. Constraints & Dependencies
### Constraints
[From Requirements Brief + user input]
- [Technical constraints]
- [Business constraints]
- [Regulatory constraints]

### Dependencies
| Dependency | Description | Impact if Not Met |
|------------|-------------|-------------------|
| [Critical dependencies from user input] |

---

## 9. Risks & Mitigation Strategies
| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| [Top risks from user input with mitigation plans] |

---

## 10. Success Metrics & KPIs
[Business-focused metrics from user input]
- [Metric 1: measurable business outcome]
- [Metric 2: measurable business outcome]
- [Metric 3: measurable business outcome]

---

## 11. Acceptance Criteria (Exit for Phase 3)
- Solution is **testable in business terms**
- Acceptance criteria are clear, measurable, and agreed upon
- Functional and non-functional requirements fully captured
- Stakeholders have signed off on the PRD
- Technical teams can begin implementation planning

---

## 12. Approval
| Name | Role | Signature | Date |
|------|------|-----------|------|
| [Business Owner from stakeholder list] | Business Owner | | |
| [PM/PO from stakeholder list] | PM/PO | | |
| [QA Lead] | QA Lead | | |
```

---

👉 **In short:** The PRD is the handshake between strategy and tactics. It’s the last chance to lock clarity before translation into code. If it’s solid here, the tactical team runs smooth. If it’s fuzzy, welcome to chaos.

---

## 📖 Part 2 - Strategic Feedback Loop (Business Side)/2.3.0-strategic-domain-design.md

# 2.3.0 Strategic Domain Design

The PRD defines *what* solution we’re betting on. Strategic Domain Design (SDD) defines *where that solution lives in the business* and *how it interacts with the rest of the system.*

This is the bridge between the Strategic Loop and the Tactical Loop. It’s where we zoom out and ask: does this solution fit cleanly into the business, or are we about to create workflow collisions and role confusion?

---

## Purpose

SDD ensures that every PRD-backed solution slots neatly into the business model: departments, workflows, operations, and entities. It adds context that prevents well-meaning fixes from causing bigger problems elsewhere.

---

## Burning Questions It Answers

* What **departments** does this PRD touch?
* Which **workflows** are involved, and who owns them?
* Where are the **crossovers** or potential conflicts?
* Which **operations** (steps) are required?
* Which **business entities** are impacted?
* Who is **allowed** to perform these workflows and operations? (roles & permissions)
* Under what **context** can those operations be performed?

---

## Why It Matters

PRDs are written in isolation - they describe a problem and solution, but not always how it interacts with the larger business. That’s fine for speed, but dangerous for alignment.

SDD is the safeguard. It lets business stakeholders see cross-workflow and cross-department conflicts *before* the Tactical team ever touches code.

Example:

* Josh (League Manager) can create teams and add staff.
* Bill (Head Coach of Anoka Trap Team) can add or remove staff for his own team, but not for others.

Both rules sound fine in a PRD. But when mapped in SDD, you see they live in the same **Team Management workflow**. If not clarified, the system might allow head coaches to modify other teams, creating chaos.

---

## The Mapping

Strategic terms map directly to Tactical terms:

* **Department → Domain/Module**
* **Workflow → Action**
* **Operation → Service.Function**
* **Business Entity → Model**

This one-to-one mapping is what allows the business to design the system in their own language, while IT focuses on implementing it in code. Think architect (business) and builder (IT).

---

## Deliverable

An SDD artifact is usually a structured map or table. Example:

**Department: League Management**

* **Workflow:** Manage Teams

  * **Operations:** `Team.create`, `Team.addCoach`, `Team.addStaff`
  * **Entities:** Team, Staff, Coach
  * **Roles/Permissions:**

    * League Manager: all operations
    * Head Coach: only staff operations for their own team

This rolls up into the same structure used on the Tactical side, which makes traceability automatic.

---

## What’s Next

This overview is enough for small teams to see the value and slot solutions into the bigger picture.

For larger or more complex orgs, we’ll dive deeper in the next sections:

* **2.3.1 Departments** – define the big buckets and owners
* **2.3.2 Workflows** – capture repeatable processes per department
* **2.3.3 Operations** – break workflows into verb + entity steps
* **2.3.4 Entities** – list the nouns that flow through operations

---

👉 **In short:** PRD defines the solution in isolation. SDD defines its place in the business. It’s how Feedback Loops ensure that solutions don’t just work - they fit.

---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/3.0.0.tactical-domain-design-overview.md


---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/3.1.0.tactical-domain-design-baseline.md


---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/3.1.1.concept-baseline.md

# 7.1.1 Concept: Establish The Tactical Baseline - Documenting the Code

Every dev team thinks they know their codebase… until they try to map it. Suddenly, that “simple” membership feature runs through three controllers, a job, a helper class, and an Eloquent model with more business logic than the product owner ever imagined.

That’s why we start the Tactical Phase with a Baseline. This isn’t about refactoring or cleaning yet. It’s about taking a clear snapshot of how the code actually works today — hacks, shortcuts, god classes, and all.

Think of it like making a field guide: you can’t explore the jungle safely until you know which paths exist and which plants will give you a rash.


---

### The Four Building Blocks

When documenting the code, we care about four concrete pieces:

1. **Modules** – The big buckets of code. In Laravel, this might be `App/Domain/Orders` or `App/Domain/Teams`. In a legacy mess, it might just mean “everything under `Controllers/` that sorta belongs together.”
2. **Actions** – The entry points that do real business work. In clean apps these are explicit `Action` classes. In messy ones, they might be controller methods (`TeamController@update`), queued jobs, or artisan commands packed with logic. If it kicks off a workflow, it’s an Action.
3. **Services** – Reusable logic units. In nice systems these are service classes with single responsibilities. In less nice ones, they’re helpers, utilities, or giant “manager” classes that quietly run half the app. Either way, call them out.
4. **Models** – The nouns of your system. Laravel’s Eloquent models, custom DTOs, or whatever is pretending to be the thing. Even if your models are overweight with business rules, document them as they are.

👉 The rule of thumb: Modules hold Actions. Actions call Services. Services operate on Models. If you can’t see that chain, your baseline isn’t finished.


---

### Putting It All Together

Here’s a small Tactical Baseline for a fictional Teams module:

``` 
Module: Teams
  Actions:
    - TeamController@update
    - InviteController@create

  Services:
    - TeamService.updateName()
    - InviteService.send()

  Models:
    - Team
    - Invite
    - Athlete

```

👉 Just like the Strategic side, this is the **scratchpad view**. It’s quick, nested lists that give you a fast way to capture what’s really in the codebase without debating polish.

When you’re ready to formalize it, you’ll switch to the **structured templates in the appendix** (Module Detail, Action Detail, etc.). Those templates provide the consistency needed for sharing across the team, but the core structure stays the same: Modules → Actions → Services → Models.

Think of it as messy field notes vs a cleaned-up field guide. Both matter. The notes help you explore, the guide helps everyone else navigate.


---

### Success Criteria

You know your Tactical Baseline is “good enough” when:

- A new dev could trace a feature from Action → Service → Model without getting lost.
- No one on the team says “oh wait, you forgot the thing in Helpers.php.”
- Each module baseline fits on a single screen. If it sprawls, split it into sub-baselines (e.g. “Teams Baseline,” “Billing Baseline”).
- You can point from each operation in the Strategic Baseline to its match here.


---

### Why It Matters

Most teams think they know their code until they try to map it. That’s when the blind spots show up: duplicate services, controllers hiding core business logic, models overloaded with side effects.

The Tactical Baseline forces the code into daylight. It gives you a shared mental model of what’s actually running in production — good, bad, and ugly. And that shared map is the only way the Loop can work.

👉 In short: Don’t refactor yet. Don’t make it pretty. Just document reality so you can start fixing it, one backlog item at a time.


---

---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/7.1.2.sop.md


---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/7.1.3.workshop.md


---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/7.2.0.tactical-loop.md


---

## 📖 Part 3 - Tactical Feedback Loop (Tech Side)/coding-standards.md

# Part 3 - Tactical Feedback Loop

## Tech Stack & Coding Standards

---

## 1. Stack Overview

* **Framework:** Laravel 12
* **Auth:** Passport (scopes for web-access, api-access, plus jobs/commands where appropriate)
* **Authorization:** Spatie Permission + Laravel Gates/Policies
* **UI:** Volt + Flux
* **DB:** MySQL 8.x
* **Testing:** PEST
* **Transport:** UI routes, API routes, Jobs, Commands
* **Config:** `.env` flags to enable/disable modules

👉 **In short:** Everything hangs off Laravel conventions. Keep it boring, predictable, and testable.

---

## 2. Module Conventions

* **Strategic mapping:** Each Department → one Module namespace (Domain and Module are interchangeable).
* **Namespace:** `App/<Module>` for Actions, Services, DTOs, and optionally Models; or `App/Models` for global models when appropriate.
* **Enablement:** Each module has an `.env` toggle `MODULE_<NAME>=true|false` and a module service provider to register routes and bindings.
* **Seams:** Modules should not reach into each other’s internals. Cross-module communication goes through Services or Events.

### Folder skeleton

```
app/<Module>/
  Actions/
  Services/
  DTO/
  Policies/
  Providers/
  Routes/
    web.php
    api.php
  Jobs/
  Commands/
  Exceptions/
  Support/  # helpers specific to module
  Listeners/
```

---

## 3. Routing

* **Split by module:** Each module owns `Routes/web.php` and `Routes/api.php` registered by its provider.
* **Volt first:** Favor Volt based routes for UI. Controllers remain for non-Volt endpoints or when composition is clearer.
* **Thin edges:** Route → FormRequest → Action. Volt functions and controllers stay thin and delegate immediately to Actions.
* **Passport scopes:** Apply `web-access` or `api-access` at the route middleware layer.

---

## 4. Entry Points

* **Allowed:** UI Routes, API Routes, Jobs, Commands, Listeners.
* **Rule:** All entry points call an **Action**. No direct Service calls from transport edges or listeners.
* **Background work:** Jobs wrap Actions. Commands are thin facades over Actions for ops workflows. Listeners also delegate directly to Actions and contain no logic.

---

## 5. Actions

* **Role:** Tactical mirror of a Strategic Workflow. Orchestrates Services and emits Events.
* **Contract:** Accepts an `ActionInputDTO`, returns an `OutputDTO` or ViewModel.
* **Validation:** Inputs validated by FormRequest or explicit DTO validators.
* **Authorization:** Verify Spatie Permissions before invoking Services or emitting Events.
* **Side effects:** Only through Services. No direct DB writes here.

---

## 6. Services

* **Role:** Tactical mirror of a Strategic Operation. Encapsulates business logic.
* **Authorization:** Enforce Gates/Policies inside Services before mutating anything.
* **I/O contracts:** `ServiceInputDTO` and `ServiceOutputDTO`. Never return Eloquent models to callers outside the service.
* **Cross-module:** Allowed via service interfaces. Bind interfaces in module provider.

---

## 7. Models

* **Scope:** Models may be global in `App/Models` or module scoped in `App/<Module>/Models` when boundaries are strong.
* **Keep thin:** No business rules beyond relationships, casts, scopes, and accessors where unavoidable.
* **Policies:** Define access rules here, enforced consistently by Services.

---

## 8. DTOs

* **Why:** Deterministic contracts between layers. Simplifies testing with PEST.
* **Types:** `ActionInputDTO`, `ResultDTO/OutputDTO`, `ServiceInputDTO`, `ServiceOutputDTO`, plus View DTOs for UI.
* **Rules:** Immutable where practical. No framework coupling inside DTOs.

---

## 9. Validation

* **FormRequest:** Mandatory at transport edges for incoming data.
* **Service-level checks:** Business rule validation lives in Services, not controllers.

---

## 10. Authorization

* **Order of checks:**

  1. Passport scope at route (entry gate)
  2. Spatie Permission for capability checks
  3. Gate for contextual rules
  4. Policy for record-level decisions
* **Placement:** Services own the enforcement before performing mutations.

---

## 11. Environment Flags

* **Module toggles:** `.env` variables enable or disable module route registration and scheduled jobs.
* **Feature flags:** Use config or a simple toggle service for sub-module features. Keep flags discoverable and test-covered.

---

## 12. Testing

* **PEST:** Required for units, services, and actions.
* **DTO tests:** Verify serialization and invariants.
* **Policy tests:** Cover critical access paths and denial cases.
* **Action tests:** Treat as integration at the module seam.
* **Event/Listener tests:** Ensure events are emitted correctly and listeners properly dispatch Actions.

---

## 13. Database

* **Migrations:** Live alongside the module or in central `database/migrations` with clear naming: `<timestamp>_<module>_<table>_...`.
* **Seeds:** Module-specific seeders where useful. Keep idempotent.
* **Constraints:** Default to constraint logic in Services for situational data integrity. DB-level constraints may be used sparingly, but Services are the source of truth and surface friendly errors.

---

## 14. Error Handling

* **Exceptions:** Module-specific exceptions under `Exceptions/`. Bubble to a standard handler with problem details.
* **Error boundaries:** Catch at Action edges, convert to domain-safe responses or problem detail objects.
* **User messaging:** Services surface friendly errors - no raw framework exceptions should leak to UI or API clients.

---

## 15. Events

* **Emit:** Use Laravel Events from Actions or Services to represent meaningful business facts.
* **Listeners:** **Must only invoke Actions** and contain no business logic. Keep them single-purpose and idempotent.
* **Conventions:**

  * Events named in past tense, e.g., `TeamCreated`, `InvoiceSent`.
  * Listeners live under `Listeners/` within the module and only dispatch Actions (no direct Service or DB calls).

---

## 16. Observability

* **Structured logging:** Prefer JSON logs for aggregation. Always include correlation IDs (`request_id`, `action_run_id`).
* **Metrics:** Count key events and failures per module/action. Naming convention: `<module>.<action>.<result>`.
* **Performance timing:** Log execution time of hot path Services/Actions for insight.
* **Event trails:** Log event emissions and listener outcomes to form an audit trail.

---

## 17. Naming & Style

* **Actions:** VerbNoun, e.g., `ManageTeam`, `IssueRefund`.
* **Services:** `<Noun>Service` with verb methods, e.g., `TeamService.addCoach()`.
* **DTOs:** Suffix with DTO, e.g., `CreateTeamInputDTO`.
* **Routes:** Grouped by module prefix. No long anonymous closures except Volt pages.

---

## 18. Dependencies & Boundaries

* **No hidden reach-ins:** A module cannot use another module’s internal classes directly.
* **Interfaces:** Cross-module use only via interfaces bound in providers.
* **Events as seams:** Prefer events for low coupling.

---

## 19. Tactical Artifacts Mapping

* **Module Detail:** Maps to Department Detail
* **Action Detail:** Maps to Workflow Detail
* **Service Detail:** Maps to Operation Step Detail
* **Model Detail:** Maps to Business Entity Detail

---

👉 **In short:** Keep edges thin, center logic in Services, orchestrate with Actions, guard with Policies, and move data in DTOs. Boring code today beats clever bugs tomorrow.

---

## 📖 Part 4 - Templates & Translation/08.1.strategic-to-tactical-translation-map.md

# 8.1 Strategic to Tactical Translation Map



| Strategic term            | Tactical - Laravel    | Notes                                                                                                                                                     |
| ------------------------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Department                | Domain                | Top-level business area and code namespace. Example: `App/Domain/PainPoints`.                                                                             |
| Workflow                  | Action                | Multi-step SOP composed of Operations. Implemented as one coordinating Action that may call other Actions.                                                |
| Operation                 | Service.function      | Single-step unit of business work. E.g. Team.update                                                                                                       |
| Business Entity           | Model                 | The noun of the system. Keep models thin.                                                                                                                 |
| Workflow Request          | ActionInputDTO        | Input to a coordinating Action. Includes step list, dependencies, and handoff expectations.                                                               |
| Workflow Response         | ResultDTO / OutputDTO | Composite business response with run id, final status, and next step hints.                                                                               |
| Operation Request         | ServiceInputDTO       | Input contract for a Service. For Search use criteria DTOs; for Change use command DTOs.                                                                  |
| Operation Response        | ServiceOutputDTO      | Output contract from a Service. Returns entity/view DTOs or paginated sets - never Eloquent models.                                                       |
| Business Input Form       | FormRequest           | Transport-layer validation. Converts to ActionInputDTO.                                                                                                   |
| Access Channel            | Passport Scope        | Broad transport gate - web, api, job, command. Checked at entry. After entry, Permissions + Gates + Policies govern capabilities and records.             |
| Permission                | Spatie Permission     | Named capability entity - role or grant based. No specific record context. Used for UI show/hide and quick guards.                                        |
| Role                      | Spatie Group          | Business role mapped to a Spatie Group that aggregates Permissions for assignment to users.                                                               |
| Access Rule               | Gate                  | Contextual rule at workflow boundaries: combine permissions with runtime context like business hours, feature flags, maintenance mode. Can call Policies. |
| Access Policy             | Policy                | Per-entity decision: ownership, record state, org constraints for a specific instance.                                                                    |
| Business Event            | Event                 | Past-tense fact like `PainPointCreated`. Emitted by Services or Actions.                                                                                  |
| Business Event Subscriber | Listener              | Handles side effects of Business Signals. Single classification - tactical attributes defined later.                                                      |
| Notification              | Notification          | Messages to humans or channels triggered by Events/Actions.                                                                                               |

### Access control - order of checks

1. **Access Channel - Passport Scope**: can this token enter via web, api, job, or command
2. **Permission - Spatie Permission**: named capability like `team.create`, `team.update`
3. **Access Rule - Gate**: context checks - business hours, feature flags, maintenance
4. **Access Policy - Policy**: record-level rules - ownership, role on team, attribute limits

- Principle: the deeper you go, the more restrictive. Trust at higher layers - verify at lower layers. Lower layers should not depend on the entry channel.

---

