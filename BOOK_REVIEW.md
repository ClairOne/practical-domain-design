# Practical Domain Design - Complete Manuscript
**Generated:** Sat Sep 20 02:30:13 PM EST 2025
**Repository:** https://github.com/ClairOne/practical-domain-design
**Analysis URL:** https://raw.githubusercontent.com/ClairOne/practical-domain-design/main/BOOK_REVIEW.md

---

## 📖 Part 1 - Introduction/0.1.introduction.md

# Chapter 1: Introduction / Overview

**Why another book?**
I designed PDD in response to the problems I’ve run into over a 30-year career in software development. I love the idea of Domain-Driven Design. As a developer, the artifacts of DDD make my job easier. But the constant struggle was getting others to adopt the language and process. It was confusing. It was time consuming. And the Agile misconception that “prototyping = rapid development” just piled tech debt higher and faster.

So I started experimenting. Story maps worked for a while - they gave the business something to visualize and talk about - but they didn’t have enough structure. People get lost in endless options without a framework to guide them. Over time I collected a grab-bag of tools, tricks, and half-frameworks that solved real problems. I wore every hat - dev, DBA, architect, BA, product owner, mad scientist - and every role left me with another bit of the puzzle.

Those bits stuck. I still hear from people who use tools I built more than a decade ago. And when my current job gave me the freedom to stitch it all together into a single framework and test it with a small team, the feedback was jaw-dropping. Within days the team was shipping cleaner, faster, and with less stress.

I’ve been using the prompts that underpin PDD for weeks now, and the results are nothing short of  amazing. I built a full feature in 48 hours - from idea to production-ready pull request - with full documentation and polish I’d normally never have time for.

That’s why I’m writing this book. PDD isn’t theory. It’s the working framework born out of decades of bruises, stitched together in a way real teams can actually adopt and benefit from.

---

**Who this book is for**
If you’re on a small product team, you’ll recognize the chaos: napkin requirements, ops firefights, QA chasing ghosts, devs guessing at business intent. PDD gives you just enough structure to stop the bleeding without slowing you down.

If you’re in a large enterprise, the pain looks fancier - more Jira tickets, more committees, more slide decks - but it’s the same disease. Translation fatigue. Decision ping-pong. Models that look great on paper but collapse in production. PDD scales up because the core loop is the same: feedback, thin slices, and making the good stuff canon.

---

**What this book will teach you**
Here’s the journey we’ll take together:

1. **Spot the real problem.** Why traditional methods like DDD and “Agile Theater” break down in practice.
2. **Meet PDD.** The principles and promises that make it work.
3. **Build your baseline.** A simple way to capture where you are today before you try to fix it.
4. **Run the loop.** The feedback cycle that drives learning and prevents late-night disasters.
5. **Make it canon.** How to promote lessons from the loop into your new source of truth.
6. **Keep it alive.** How to deal with drift, growth, and the messy reality of shipping software.

By the end, you won’t have a binder of theory. You’ll have a handful of living artifacts, a loop your team can actually run, and a way to evolve design without collapsing under it.

---

**What next**
You’ve got two good options from here: dip into the case studies below to see how this stuff plays out in real, funny, and disastrous contexts - or skip ahead to Chapter 2 to start unpacking the problem space. Either way, you’re set up to get the most out of what comes next.

---

**\[CASE STUDY: TBD - Real]**
**\[CASE STUDY: TBD - Funny]**
**\[CASE STUDY: TBD - Disaster]**

---

👉 In short: PDD is the antidote to design theater. Whether you’re a five-person startup or a Fortune 500 death-by-committee machine, the principles are the same: feedback beats foresight, thin slices win, and what works becomes canon.

---

## 📖 Part 1 - Introduction/0.2.why-popular-methodolies-trip-up-teams.md

# Chapter 2: Why Popular Methodologies Trip Up Teams

Software design has been through a parade of “big answers.” Waterfall, Agile, Scrum, Domain-Driven Design (DDD), SAFe, LeSS, and countless hybrids with shinier logos. Each came with the promise: *follow these steps and your team will deliver better software, faster, with less pain.*

The problem? Most of these methods look great in books and slide decks, but in practice, teams end up tripping over the same cracks. Some approaches are too rigid. Some are too heavy. Others are elegant in theory but demand a learning curve so steep you need climbing gear.

PDD isn’t here to throw out everything that came before. It borrows the best pieces. But it also admits what hasn’t worked in the real world - especially for small teams without a stadium full of coaches and consultants.

---

## a. The Waterfall Mirage

Waterfall promised clarity: gather all the requirements up front, design once, build once, and roll it out like a factory product.

In practice? Businesses change their mind faster than you can finish a Gantt chart. By the time the last phase is done, the requirements are already out of date. The team ships exactly what was asked for six months ago - and exactly what no one wants today.

---

## b. Agile & Scrum Fatigue

Agile started as a rebellion against Waterfall’s rigidity. Scrum gave it structure: sprints, backlogs, standups. At first, it was liberating.

But without discipline, teams drift into **Agile Theater**:

* Standups become status recitals.
* Sprint reviews are awkward half-demos.
* Backlogs balloon into junk drawers.

Instead of speed and collaboration, you get ritual without results. Scrum isn’t broken - but applied mechanically, it wears teams down.

---

## c. DDD’s Steep Hill

Domain-Driven Design was revolutionary when it landed in 2003. It gave developers a way to model messy business problems in code. For practitioners, the artifacts are gold.

The catch? The learning curve. Getting non-developers to adopt the language and process often stalls out. Ubiquitous language sounds great until Sales, Support, and Finance are stuck in a three-hour debate about whether it’s a *customer* or a *client.*

DDD isn’t wrong. It was just early. And without simplification, it’s a barrier for teams trying to move fast.

---

## d. Framework Inflation

Every few years, a new acronym promises to scale Agile: SAFe, LeSS, Spotify model. These frameworks often solve problems for huge enterprises - but bring overhead most small teams can’t sustain. Suddenly you’re spending more time updating artifacts for the framework than solving real business problems.

---

## What these all have in common

* They start with **good intentions.**
* They deliver **value for some teams.**
* But when adopted blindly, they create as much pain as they solve.

Rigid plans collapse when the business shifts. Rituals drift into theater. Elegant ideas stall out under their own weight.

---

## Where PDD fits

Practical Domain Design isn’t a “replacement religion.” It’s a pragmatic evolution:

* **From DDD:** it keeps the clarity of modeling the domain - without the linguistic dogma.
* **From Agile/Scrum:** it keeps the feedback loops and thin slices - without the theater.
* **With Waterfall:** it can even fit, by using baselines and loops to reduce risk in staged delivery.

The core idea: **feedback beats foresight, thin slices win, and what works becomes canon.**

That makes PDD lightweight enough for a five-person startup, but structured enough to give a 5000-person enterprise real alignment.

---

👉 **In short:** Every methodology promised to fix the chaos. Most delivered value - and headaches. PDD builds on what worked, ditches what didn’t, and gives you a loop you can actually run without a playbook the size of a dictionary.

---

## 📖 Part 1 - Introduction/0.3.the-practical-domain-design-fix.md

# Chapter 3: The Practical Domain Design Fix

So if Waterfall, Agile, Scrum, and DDD each had their strengths, why do teams still keep tripping on them? Because most of these methods are used like it’s still the era they were born in. Waterfall assumed stable requirements. Agile assumed small, co-located teams. DDD assumed monoliths and long release cycles. The world has changed - APIs everywhere, cloud sprawl, remote everything, and a constant stream of alerts that hit at 2 a.m. Trying to use those methods unmodified today is like trying to run modern apps on a Windows 95 box. They might boot, but the fit is clunky.

That’s where **Practical Domain Design (PDD)** comes in.

---

## a. Core Idea: Two Worlds, One Map

Instead of forcing everyone into the same vocabulary or rigid process, PDD accepts reality: business and tech will always speak different dialects.

* Business talks in **departments, workflows, operations, and entities.**
* Devs talk in **modules, actions, services, and models.**

Neither side has to fake fluency. The bridge is a **translation map** that connects the two. It’s lightweight, visual, and keeps both sides honest.

👉 Think of it like subtitles on a movie. You don’t need the actors to change their lines, you just need a reliable translation so everyone follows the same plot.

---

## b. How PDD Solves the Old Problems

* **Waterfall’s rigidity** → PDD replaces one giant bet with thin slices and feedback loops. You still get structure, but you’re not locked into a six‑month death march.
* **Agile/Scrum fatigue** → PDD keeps the good parts (short cycles, collaboration) but trims the theater. No rituals for their own sake - only the loop that proves learning.
* **DDD’s steep hill** → PDD lowers the barrier. Instead of demanding one “ubiquitous language,” it gives each side its own baseline and ties them together with a map.
* **Framework inflation (SAFe, LeSS, etc.)** → PDD scales up without drowning in overhead. Strategic artifacts work for a 5‑person team and still make sense in a 5000‑person enterprise.

PDD doesn’t fight these methods - it plays nice with them. Want to run Scrum? Great, let PDD’s baselines feed your backlog. Stuck in a Waterfall shop? Use PDD’s loop to reduce risk between stages. Love DDD? Keep the modeling discipline, just ditch the vocabulary wars.

---

## c. Strategic vs Tactical

Classic methods often blur business intent and technical detail. PDD draws a hard line:

* **Strategic Baseline (business reality):** How the business actually runs today - departments, workflows, ops, and entities.
* **Tactical Baseline (code reality):** How the system actually behaves today - modules, actions, services, and models.

Side by side, the gaps and misalignments are impossible to ignore. That clarity is what fuels better decisions.

---

## d. The Loop as Connective Tissue

The real magic isn’t just the baselines - it’s the **Loop.**

Every time a new pain point or idea shows up, it runs through the same cycle:

1. Capture it in **business terms** (strategic).
2. Translate it into **technical terms** (tactical).
3. Implement, validate, and demo it back in both languages.

No endless debates. No ceremony creep. Just a repeatable loop that keeps everyone aligned while the system evolves.

---

👉 **In short:** Practical Domain Design doesn’t throw out old methods - it modernizes them. Structure without rigidity. Feedback without theater. Translation without language coups. Two worlds, one map, continuous loops. That’s the fix.

---

## 📖 Part 1 - Introduction/0.4.getting-started-with-pdd.md

# Chapter 4: Getting Started with PDD

Okay, enough theory. Let’s talk about what you actually need to get PDD off the ground. Spoiler: you don’t need a six-figure consulting engagement or a 300-page training manual. You need a couple of roles, a clear sense of your situation, and the discipline to keep the loop running. That’s it.

---

## a. Minimum Setup

The beauty of PDD is that it’s **lightweight on purpose.** You don’t need to reorganize the company or buy fancy tools. You can start with:

- A shared doc or whiteboard tool (Notion, Miro, Google Docs - doesn’t matter).
- Your existing backlog system (Jira, Trello, sticky notes on the wall).
- A team willing to spend 1–2 hours mapping how things *actually* work.

If you’ve got those, you can start. No excuses.

---

## b. Roles (aka Hats People Already Wear)

PDD doesn’t require you to invent fancy new job titles. You already have these roles on your team - we’re just shining a light on the hats they need to wear inside the loop.

- **Business Mapper**: This is your BA, Product Owner, or whoever actually knows how the business runs (warts and all). Their job in PDD is to capture workflows and entities in plain language, not corporate poetry.
- **Tech Mapper**: Usually a lead dev or senior engineer. They know where the codebase’s bodies are buried and can map modules, services, and models without hand-waving.
- **Loop Facilitator**: Think “Scrum Master without the burn-down chart fetish.” Their job is to keep the cycle moving, make sure business and tech maps stay aligned, and call BS when people start drifting into Agile Theater. On small teams, this can rotate or just fall to whoever’s best at herding cats.

👉 The point isn’t new titles. The point is coverage. If no one is wearing a hat, that perspective gets ignored - and your loop collapses.

---

## c. PDD Situations

Before you dive into mapping, figure out which **situation** your team is in. PDD flexes to fit, but the starting point changes:

### 1. Existing Business + Existing Software

*Example: A SaaS company that’s been live for 5 years. Customers are happy enough, but the codebase has grown into a patchwork quilt. You need to document what you have and improve it without blowing everything up.*

- **Strategic:** Baseline + Loop → Canon
- **Tactical:** Baseline + Loop → Canon
  👉 Document what exists (warts and all), then improve it incrementally.
  *Remodeling the house while you still live in it.*

---

### 2. Green Field (New Business + New Software)

*Example: Two founders with an idea for a marketplace app. No existing business processes, no codebase. You’re starting from zero.*

- **Strategic:** Loop → Canon
- **Tactical:** Loop → Canon
  👉 No baseline exists. The loop is both discovery and design.
  *Building on an empty lot.*

---

### 3. Existing Business + New Software (no pre-existing software)

*Example: A manufacturer that’s been tracking orders with spreadsheets and email threads. The business is humming, but now they want to build their first internal system.*

- **Strategic:** Baseline + Loop → Canon
- **Tactical:** Loop → Canon
  👉 Document the business, then treat the software side as green field.
  *Like digitizing a company that’s been running on paper binders.*

---

### 4. Existing Business + Re-write of Existing Software

*Example: A retailer stuck with a 15-year-old ERP system that crashes weekly and can’t keep up with new sales channels. It’s too brittle to patch anymore, so the only real option is a rebuild.*

- **Strategic:** Baseline + Loop → Canon
- **Tactical:** **Condensed Baseline (reference only)** + Loop → Canon
  👉 Capture the legacy system only as a **reference** to avoid repeating its mistakes. Build fresh tactical canon through the loop.
  *Tearing down a moldy house. Keep the inspection report, but don’t reuse the foundation.*

---

### Decision Checklist

Not sure which path you’re in? Use this quick guide:

* If you’ve got **business + software in production**, you’re in **Situation 1**.
* If you’ve got **no business and no software**, you’re in **Situation 2**.
* If you’ve got **business but no software yet**, you’re in **Situation 3**.
* If you’ve got **business + terrible software you need to replace**, you’re in **Situation 4**.

👉 When in doubt, pick the one that feels least optimistic. PDD works best when you face the messy reality head-on.

---

## Why This Matters

Most teams fail because they start too heavy. They try to roll out DDD workshops, big design sessions, or enterprise tooling before they’ve even proven the basics. PDD flips that: start minimal, keep artifacts tight, and let the loop prove its value.

In short: PDD doesn’t need a reorg. It just needs a map, a loop, and a team that agrees to keep it honest.

---

## 📖 Part 2 - Strategic Domain Design/2.0.0.strategic-domain-design-overview.md

# 📘 Chapter 2.0.0: Strategic Domain Design Overview

**Why strategy matters**
Software doesn’t fail because of code alone. It fails because of bad bets, muddled decisions, and feedback that never makes it to the people who can act on it. Strategic Domain Design is where PDD starts - it’s the layer that tells the business: *what’s the core business problem, how is it hurting us today, and what does an acceptable solution actually look like?*

If you skip strategy, you end up playing whack-a-mole with symptoms. Teams argue over architecture while the business quietly drifts off-course.

---

**The problem at the business layer**
Most organizations struggle with three things:

1. **Translation fatigue** - endless back-and-forth between business and tech creates lag and confusion.
2. **Decision ping-pong** - ownership is unclear, so choices bounce around until deadlines make the decision for you.
3. **Theater over truth** - slide decks and process rituals look good, but the real pain (risk, waste, late nights) is hidden.

Without a clear strategic frame, tactical excellence is wasted effort. You can invest in the slickest tools and the most polished reports and still back the wrong bet. PDD isn’t just about better delivery - it’s a process for improving how the business itself thinks, decides, and learns.

---

**What Strategic PDD gives you**
Practical Domain Design at the strategic level delivers three outcomes:

* **Clarity of bets** - a lightweight product brief that says what we’re trying to achieve and why it matters.
* **Explicit decision rights** - every decision has an owner, inputs, and a timebox. No more endless debates.
* **A living loop** - feedback from users, delivery, and risk gets inspected, and the plan actually changes.

Think of it as business guardrails. Not process for process’ sake, but a system that keeps decisions visible, accountable, and adaptable.

---

**Artifacts that matter**
Strategy isn’t about piles of documents. It’s about a few living artifacts that steer the ship:

* **Business Pain Point** - the raw issue we need to solve.
* **Problem Validation Brief** - evidence that the pain is real and worth fixing.
* **Vision & Problem Statement** - the north star and the context around it.
* **Requirements Brief** - the key needs we must address without drowning in detail.
* **Product Requirements Document (PRD)** - a structured record of what we’re committing to build.

If an artifact doesn’t directly improve clarity, speed, or safety, it’s baggage.

---

**Why it matters to the business**
Skip Strategic PDD and you leave product direction to inertia, the loudest voice, or the prettiest slide deck. Use it, and you get a loop where feedback actually alters course, decisions stick, and your team can focus on execution without burning weekends.

This chapter is the bridge: once you understand the business frame, the tactical chapters will show you exactly how to enforce it in code, tests, and releases.

---

👉 In short: Strategic Domain Design is the part of PDD that keeps the business honest. It’s not more meetings - it’s a way to make sure your team’s energy goes into bets that matter, decisions that stick, and feedback that changes the plan.

---

## 📖 Part 2 - Strategic Domain Design/2.1.0.strategic-domain-design-baseline.md

# 📘 Chapter 2.1.0: Strategic Domain Design - Baseline

**Why you need a baseline**
Before you start changing anything, you need to see the mess as it really is. Most teams blow past this step because it feels slow or boring. But if you don’t freeze a snapshot of your current reality, you’ll never know what actually improved - you’ll just be swapping one flavor of chaos for another.

Think of it like renovating a house: you take “before” photos not because they’re pretty, but because later they prove all the sweat was worth it.

---

**What a baseline gives you**
The baseline captures the business problems and decisions in flight right now. Done right, it gives you:

* **A common reference point** - everyone agrees on “this is where we are.”
* **A safe starting line** - you can experiment without losing track of the original problem.
* **Evidence for improvement** - proof that the loop is actually paying off.

---

**How to build your baseline**
You don’t need a six-month discovery crusade. You just need to answer a few blunt questions and capture them in living artifacts:

* **Business Pain Point** - What’s the real hurt? Phrase it in plain English.
* **Problem Validation Brief** - How do we know this hurt is real and worth fixing?
* **Vision & Problem Statement** - Where are we trying to go, and why?
* **Requirements Brief** - What’s essential to fix, without boiling the ocean?
* **Product Requirements Document (PRD)** - The first structured record of the bet we’re making.

If your team can crank out a single page for each, congratulations: you’ve got a baseline.

---

**Pitfalls to avoid**

* Don’t turn this into a months-long discovery marathon. The point is speed, not perfection.
* Don’t let artifacts rot on a shelf. If nobody updates them, they’re just paperwork.
* Don’t skip validation. If you can’t prove the pain is real, you’re solving the wrong problem.

---

**What next**

**Learn How It Works**
Start with the Practical Strategic Domain Design core concepts. That’s the playbook that explains why this isn’t just more paperwork and how it ties your business together.

**Learn How To Do It**
Crack open the SOP. Think of it as the recipe card: step-by-step, no fluff, just what you need to get cooking.

**Choose Your Own Adventure**
Now pick your weapon. Want the full hands-on experience? Go manual and grind it out with your team. Prefer speed and less grunt work? Let AI do the heavy lifting. Same baseline, different flavor of shortcut.

---

👉 In short: The baseline isn’t busywork - it’s the “before photo” that makes progress visible. Skip it, and you’re just running in circles and calling it strategy.

---

## 📖 Part 2 - Strategic Domain Design/2.1.1.concept-establish-the-strategic-baseline.md

# Chapter 2.1.1 Concept: Establish The Strategic Baseline - Documenting the Business

Every team thinks they know how their business runs… until they try to write it down. Suddenly the “simple” billing process has six secret detours, and Support’s “standard” workflow turns out to be fifty shades of chaos.

That’s why we start PDD with the **Baseline**. This is not about fixing anything. It’s not about debating best practices. It’s about taking a clean snapshot of how the business actually operates today - warts, duct tape, and all.

Think of it like a map: you can’t plan a road trip until you know where you’re starting. The Baseline is that starting point.

---

## The Four Building Blocks

When documenting the business, we care about four simple pieces:

1. **Departments** – The big buckets of responsibility.
2. **Workflows** – The repeatable processes each department runs.
3. **Operations** – The tasks inside each workflow.
4. **Entities** – The nouns the business deals with every day.

That’s it. No fancy jargon or synergistic buzzwords. Just business terms people already use.

---

### 1. Departments

Departments are the easiest place to start. If the company cuts paychecks for it, it’s a department.

* Sales
* Billing
* Support
* HR
* Operations

👉 Write them down as a list. Don’t argue about org charts or reporting lines. We just want the functional buckets of work.

---

### 2. Workflows

Workflows are the **repeatable processes** a department runs. Each workflow has a clear start, a series of operations, and an end.

Think of a workflow as a **story**: *When X happens, we do Y, which results in Z.*

Examples (Billing Department):

* **Generate Invoice** → (operations: `Invoice.create`, `Invoice.send`)
* **Handle Dispute** → (operations: `Dispute.open`, `Dispute.resolve`)
* **Send Payment Reminder** → (operations: `Reminder.create`, `Reminder.send`)

👉 If you can’t describe it as “When this event happens, we perform these steps to get to an outcome,” it’s not a workflow.

Workflows are the backbone of the Strategic Baseline. Later, when we connect them to the Tactical Baseline, you’ll see how each workflow coordinates a set of operations inside the code.

---

### 3. Operations

Operations are the **atomic steps** inside a workflow. Each one is a single action taken against a business entity. They should be short, concrete, and verb-heavy.

Examples:

* `Team.updateName`
* `Invite.create`
* `Season.changeRegistrationCloseDate`

👉 If an “operation” takes multiple checks, approvals, or branches, it’s not an operation - it’s a workflow.

Operations are where the business world starts to line up with the technical world. In the Tactical Baseline, these will map to **Business Entity Services** - e.g. “Update Team Name” becomes `TeamService.updateName()`.

---

### 4. Entities

Entities are the nouns your team touches. Customers, Invoices, Products, Tickets, Orders.

**Example (Billing Entities):**

* Customer Account
* Invoice
* Payment Method

Entities often cross department lines. That’s a good thing. Later, when we compare the business baseline with the code baseline, those overlaps will expose gaps and misalignments.

---

## Artifacts

PDD gives you a structured framework with the flexibility to use it how you want. Each template plays a role at a different stage of documenting the business:

* **🧠 Strategic Baseline - Brain Dump**
  Use this first. It’s the scratchpad where you capture Departments, Workflows, Operations, and Entities in one messy table. Don’t worry about gaps or duplicates. Just get it out of your head and into Markdown.

* **🏢 Department Detail**
  Once you’ve got the dump, zoom into each Department. This template helps you describe what the department does, who runs it, and the major workflows it owns. Use it when you want clarity across teams.

* **⚙️ Workflow Detail**
  For each workflow, break down the trigger, goal, and the step-by-step Operations. This is where you start to see how business steps line up with technical steps. Use it when you need to nail down the exact flow.

👉 Think of it like layers: Brain Dump for breadth, Department Detail for context, Workflow Detail for depth. Pick the layer you need right now. That’s the flexibility of PDD - structured enough to guide you, loose enough to adapt to your team.

---

## Success Criteria

You know your baseline is “good enough” when:

* You can show it to a new hire and they nod instead of squinting.
* No one in the room says “that’s not how we do it.”
* Aim to keep each department or module baseline on a single screen. If the map sprawls, break it into sub-baselines (e.g. “Billing Baseline,” “Membership Baseline”) instead of one giant hairball.

---

## Why It Matters

* **Shared reality:** Everyone stops pretending they know how things work and actually sees it on paper.
* **Foundation for backlog:** The next step (The Loop) builds on this. You can’t capture pain points if you don’t know the workflows they belong to.
* **Low effort, high return:** Two hours of mapping saves weeks of guesswork later.

---

👉 In short: The Baseline is just holding up a mirror. Don’t polish it. Don’t overcomplicate it. Just capture what *is*. We’ll worry about fixing things in the Loop.

---

## 📖 Part 2 - Strategic Domain Design/2.1.2.sop-establish-the-strategic-baseline.md

# Chapter 2.1.2 SOP: Establish The Strategic Baseline - Documenting the Business

The Strategic Baseline is where PDD starts. Think of it as building a simple map of how your business really works - not the slide-deck fantasy, not the way leadership *wishes* it ran, but how it actually runs day to day.

This isn’t theory. It’s an SOP you can follow like a recipe. By the end, you’ll have a set of artifacts that make the invisible visible.

---

## ✅ Quick Checklist

1. Gather the whole team in a room.
2. Brain dump all departments across the business.
3. Assign an owner to each department.
4. Brain dump workflows under each department.
5. Split into department-level huddles to break workflows into operations and entities.
6. Each team assembles a scratchpad map for its department.
7. Break for review: department owners present their maps, the group provides feedback.
8. Collect and refine Department Detail docs for all departments.

That’s it. Now let’s go step-by-step.

---

## Step 1 - Brain Dump Departments (and Assign Owners)

* Gather everyone together and list **all departments** in the business.
* Ask: “If payroll cuts a check for it, is it a department?”
* Write down department names (e.g., Billing, Sales, Support).
* **Assign a business owner** to each department - the person who will take responsibility for the workflows in that department.

**Why this matters:**

* Creates a single point of contact to confirm reality:

  * “Yes, my department does that.”
  * “No, that belongs to Jane’s team.”
* Helps the team start visualizing the company as structured roles instead of everyone doing everything.
* Sets you up for Tactical later when scopes, roles, and permissions come into play.

**Output artifact:** A list of departments with assigned owners.

👉 Pro tip: Don’t get stuck debating org charts. Owners aren’t necessarily managers. They’re the person who knows the work well enough to own the map.

---

## Step 2 - Brain Dump Workflows

* For each department, list the repeatable processes it runs.
* Ask: “When X happens, what do we do that ends with Y outcome?”
* Keep them short, e.g.:

  * Generate Invoice
  * Handle Dispute
  * Send Payment Reminder

**Output artifact:** A rough list of workflows under each department.

👉 This is still high-level. Don’t overthink. Capture what people *say* they do. You’ll refine later.

---

## Step 3 - Department Deep Dive (Operations)

* Split into department-level huddles (still in the same room).
* Take the workflow list for your department and break each workflow into **operations**.
* Each operation = **verb + entity** (e.g., `Invoice.create`, `Dispute.resolve`).
* Keep it short. If a step has multiple branches or approvals, that’s probably a separate workflow.

**Output artifact:** A short list of operations under each workflow.

---

## Step 4 - Capture Entities

* Entities are the **nouns** your business touches (Customer, Invoice, Payment Method).
* Go back through the operations you listed - the nouns are usually right there.
* Write them down under the department.

**Output artifact:** A list of entities for that department.

👉 Entities often show up in multiple departments. That’s good - it’ll expose gaps later when you compare baselines.

---

## Step 5 - Assemble Scratchpad Maps

* Each department team assembles its own map: Departments → Workflows → Operations → Entities.

**Output artifact:** A Strategic Baseline scratchpad map for each department.

👉 Don’t stress about size. If one department has 138 workflows and another has 3, leave it that way. The number isn’t “wrong” - it’s a clue.

* A huge list might mean the department is overloaded, or it might just mean you’ve defined workflows too narrowly.
* A tiny list might mean the department is well-bounded, or it might mean you’ve missed detail.

Either way, the map shows you something important about how the business actually functions. That visibility is gold.

---

## Step 6 - Present and Review

* Have department owners present their maps while everyone else listens.
* Encourage questions and clarifications:

  * “Does this look like reality?”
  * “What’s missing?”
  * “Who else is impacted by this?”
* Capture feedback and update the maps in real time.

**Output artifact:** Department Detail docs for each department, validated by the group.

---

### Success Criteria

You know your baseline is ready when:

* A new hire can look at it and nod instead of saying, “That’s not how we do it.”
* Every department has an owner who can confirm the workflows.
* The maps may be uneven across departments - and that’s fine. The differences themselves often tell you where to ask better questions later.

👉 In short: Don’t trim the map to make it “look nice.” Capture what’s real. Mess, imbalance, and lopsidedness are all useful signals for future backlog items.

---

## 📖 Part 2 - Strategic Domain Design/2.1.3.workshop-establish-the-strategic-baseline.md

# Chapter 2.1.3 Workshop: Establish The Strategic Baseline - Documenting the Business

This isn’t a stiff agenda, it’s a playbook. The goal: get everyone in a room, cut through the fantasy versions of “how we work,” and by lunch you’ll have real artifacts instead of hot air.

---

## 🕘 9:00 – Kickoff (15 min)

* Welcome the group.
* Explain the goal: *“By lunch, no more mystery workflows hiding under the carpet. We’ll have a map of how this circus really runs.”*
* Quick overview of the process: Brain dump → Deep dive → Present & review.

---

## 📝 9:15 – Brain Dump Departments & Workflows (45 min)

* Gather everyone in a room with whiteboards or a shared doc projected.
* Step 1: List all departments.
* Step 2: List the main workflows under each department.
* Assign an owner for each department.
* Stop when most heads are nodding and nobody’s starting a fistfight.

**Output:** A master list of departments, owners, and high-level workflows.

---

## 👥 10:00 – Department Huddles: Deep Dive (60 min)

* Split into department-level groups (still in the same room).
* Each group:

  * Breaks workflows into operations.
  * Captures entities touched by those operations.
  * Assembles a scratchpad map (Dept → Workflows → Operations → Entities).

**Facilitator’s role:** Float between groups, answer questions, and keep the wheels turning when energy dips.

**Output:** Department scratchpad maps.

---

## 🍴 11:00 – Lunch & Department Presentations (60 min)

* As people eat, department owners present their maps one by one.
* Encourage blunt but constructive feedback:

  * “Does this look like reality?”
  * “What’s missing?”
  * “Who else is impacted by this?”
* Update maps live based on feedback.

**Output:** Validated Department Detail docs.

---

## ✅ 12:00 – Wrap-Up & Next Steps (15 min)

* Recap what was captured.
* Highlight any obvious gaps or lopsided departments (signals for backlog).
* Explain where this leads: *“These baselines set us up for the next PDD phase.”*

**Final Output:** A complete Strategic Baseline across departments, ready for use in the PDD Loop.

---

👉 In short: Half a day, lock the team in a room, and walk out with artifacts that actually reflect reality instead of PowerPoint fantasy.

---

## 📖 Part 2 - Strategic Domain Design/2.1.4.ai-establish-the-strategic-baseline.md

# Chapter 2.1.4 AI: Establish The Strategic Baseline (AI-Assisted)

Sometimes you don’t want to wrangle sticky notes and whiteboards. Maybe your team is remote, maybe nobody wants to play facilitator, or maybe you just want the artifacts to come out clean from the start. That’s where the AI-assisted version of the Strategic Baseline comes in.

This is the same process as the manual SOP, but instead of stopping at scratchpads, you feed your raw notes into prompts that generate polished baseline docs. The AI doesn’t replace the team’s judgment - it just handles the grunt work of formatting, structuring, and cross-referencing.

---

## ✅ Quick Checklist

1. Start with the **Interview Prompt** to gather raw notes from department owners and SMEs. This helps capture the messy, conversational version of “how we actually work.”
2. Feed those interview notes into the **Department Detail Prompt** to structure each department’s map of workflows, operations, and entities.
3. For each workflow that needs more depth, run the **Workflow Detail Prompt** to expand it into operations and entity touchpoints.
4. Review the AI outputs as a group - check for accuracy, fill in missing details, and correct mistakes.
5. Save the generated docs as your baseline artifacts (Department Detail, Workflow Detail, etc.).

---

## 🔧 Prompt Map

| Step                  | Output Artifact (Baseline Scratchpad)         | Prompt to Use               |
| --------------------- | --------------------------------------------- | --------------------------- |
| Capture messy reality | Strategic Baseline                            | Interview Prompt            |
| Structure departments | Department List (baseline scratchpad)         | Department Detail Prompt    |
| List workflows        | Workflow List (baseline scratchpad)           | Workflow Detail Prompt      |
| Break into operations | Workflow + Operations (baseline scratchpad)   | Workflow Detail Prompt      |
| Capture entities      | Entity List (baseline scratchpad)             | N/A (list only at baseline) |
| Assemble baseline     | Strategic Baseline Map (combined scratchpads) | Combine outputs from above  |

👉 See the Appendices for the actual prompt templates. They’re copy-paste ready.

---

## Success Criteria

* The AI outputs structured, consistent docs for every department.
* The group has reviewed and validated them (don’t skip this - AI is fast, not infallible).
* Everyone agrees the docs reflect *reality*, not just what the AI guessed.
* Entities are captured as a simple list for now. Detailed Entity Docs come later during the Loop, when you need precision for domain design.

---

👉 In short: Run the same workshop flow, but let AI handle the documentation grunt work. You still need human brains to confirm what’s true, but you’ll walk away with clean, shareable artifacts in a fraction of the time.

---

## 📖 Part 3 - Tactical Domain Design/3.0.0.tactical-domain-design-overview.md


---

## 📖 Part 3 - Tactical Domain Design/3.1.0.tactical-domain-design-baseline.md


---

## 📖 Part 3 - Tactical Domain Design/3.1.1.concept-baseline.md

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

## 📖 Part 3 - Tactical Domain Design/7.1.2.sop.md


---

## 📖 Part 3 - Tactical Domain Design/7.1.3.workshop.md


---

## 📖 Part 3 - Tactical Domain Design/7.2.0.tactical-loop.md


---

## 📖 Part 4 - Templates/08.1.strategic-to-tactical-translation-map.md

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

