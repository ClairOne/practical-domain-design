# Practical Domain Design - Complete Manuscript
**Generated:** Sat Sep 20 10:05:17 AM EST 2025
**Repository:** https://github.com/ClairOne/practical-domain-design

> This file is auto-generated for review purposes. 
> Direct link for AI analysis: https://raw.githubusercontent.com/ClairOne/practical-domain-design/main/BOOK_REVIEW.md

---

## Table of Contents

## Manuscript Stats
- **Total Chapters:** 1
- **Total Words:** 291
- **Total TODOs:** 0
- **Raw GitHub URLs:** All chapters available at `https://raw.githubusercontent.com/ClairOne/practical-domain-design/main/manuscript/chapters/`

---

## 📖 01.0.introduction.md

# 1. Introduction: How Small Teams Blow Up Their Own Code

Every small dev team has lived this nightmare:
The business tosses IT a two-sentence “requirement” that might as well be scribbled on a napkin. Developers nod, crank out a proof-of-concept feature, and proudly demo it.

Cue the soundtrack of horror:

- “What the fuck is this?”
- “That’s not how we do it.”
- “What about this?”

Suddenly the feature is wrong, the clock is ticking, and the team is rewriting code while silently muttering, “We’ll clean that up later.” Spoiler: later never comes.

Layer this on for a few years and you’ve built a monument to tech debt. The code is brittle, tangled, and allergic to change. Marketing is still selling shiny new features. Developers are quietly updating their résumés. Leadership eventually panics and swaps out IT heads like that will magically fix the mess. The next “big idea” is always the same: *Let’s rewrite everything from scratch - V2 will save us.* And somehow, it only makes things worse.

This isn’t a one-off story. It’s the repeating cycle of small software teams everywhere. And Domain Driven Design (DDD), despite its brilliance, often makes the gap worse. Why? Because it insists on one “ubiquitous language” - and business folks aren’t buying it.

That’s where Practical Domain Design (PDD) steps in. We don’t force business and developers into the same dictionary. We let each side keep speaking their own language, then build a clear, no-bullshit translation map between them.

PDD isn’t about elegance. It’s about survival. It’s about turning chaotic ideas into boringly predictable, stable releases. And yes, *boring* is the goal. Because software delivery should be routine, not a stress factory powered by duct tape and crossed fingers.


---

---

## 📖 01.1.1.case-study.ctgo.md


---

## 📖 02.0.who-this-book-is-for.md

# 2.0 Who This Book Is For

This book is for practitioners - the people who have to live with the code and the business every single day.

- Product owners who are sick of being translators for both sides.
- Developers who are tired of vague feature requests turning into fragile spaghetti.
- QA folks who find themselves guessing at the “real” workflow.
- Ops teams who inherit brittle systems nobody fully understands.

If you’ve tried to apply Domain Driven Design (DDD) in a small team and hit a wall of business resistance, you’re in the right place. If you’ve seen features rushed from idea to demo with little context, only to trigger endless rework, this book will feel uncomfortably familiar.

And let’s set the record straight: this isn’t a takedown of Agile or DDD. Quite the opposite. We’re big fans of both. Agile was a huge leap forward - when it’s done right, it gives teams speed, adaptability, and sanity. Same with DDD: when Eric Evans put it out into the world, it was groundbreaking. It gave us a vocabulary for mapping messy business problems into code. Two decades later, it’s still brilliant in the right context.

But here’s the rub: neither Agile nor DDD is *easy*. Agile gets watered down into ceremony without substance. DDD gets stuck in endless debates over terminology and feels impossible for small teams to implement fully.

Practical Domain Design (PDD) doesn’t try to replace them. It builds on them. Think of it as DDD evolved for the messy, fast-paced reality of small teams in 2025. We keep the spirit - alignment between business and code, feedback loops, working software over fluff - but update the practice to fit today’s world.

PDD provides the missing structure: a way for business to speak in its own terms, for developers to speak in theirs, and for both sides to stay aligned without pretending they share one universal language. It takes the good ideas of DDD, cuts the overhead, and plugs them into the rhythms of Agile so the loop actually works.

In short: If you’re done firefighting and ready to make delivery boring (in the best possible way), this book is for you.


---

### 👉 Why Not Just Use DDD?

Don’t get us wrong: we love Domain Driven Design. It was a game-changer when it came out, and it’s still brilliant in the right context. But here’s why small teams often struggle to pull it off:

- **The “one language” myth.** Business and devs rarely converge on a single vocabulary. Meetings turn into word-policing sessions instead of progress.
- **It’s heavy.** Full-blown DDD can feel like a consulting project all by itself. Small teams don’t have the time or headcount to run it by the book.
- **Translation fatigue.** Without clear mapping, “Send Payment Reminder” in the backlog becomes `retryPayment()` in code. Everyone’s half right and completely misaligned.

**PDD isn’t anti-DDD.** It’s DDD with a reality check. We keep the good ideas (clear models, alignment, feedback loops) but strip out the overhead and force-fit jargon.

---

## 📖 03.0.why-ddd-trips-up.md

# 3.0 Why Domain Driven Design Trips Up Teams

When *Domain Driven Design* first hit the shelves in 2003, it was a breakthrough. It gave us a language to talk about messy business problems in code - long before microservices, CQRS, or half the design patterns we take for granted today.

The thing is: software design has changed. The way we build, deploy, and maintain systems in 2025 looks nothing like it did back then. DDD wasn’t wrong - it was early. And when teams apply it by the book today, they often find themselves tripping over three big pitfalls.


---

## a. The Universal Language Myth

DDD introduced the idea of a “ubiquitous language” - one set of terms everyone uses. In theory, that kills confusion. In practice? It often leads to endless debates over whether to call it a “customer,” “client,” or “account,” while nothing ships.

Reality check: business and devs have different dialects. Finance will always say “invoice.” Devs will always say “DTO.” Pretending those worlds can be collapsed into a single dictionary is like trying to make English and French into “Frenglish.” You don’t get clarity - you get a mess.

The fix isn’t forcing one language - it’s building a map between the two.


---

## b. Translation Overhead

Translation is real work. And most teams don’t plan for it.

Without a clear map, “Send Payment Reminder” in the backlog morphs into `retryPayment()` in code. Support thinks the feature handles overdue accounts. QA tests retries. Everyone’s right in their own head - and everyone’s wrong together.

Skipping translation turns the backlog into a game of telephone. The further the message travels, the fuzzier it gets.


---

## c. Drift into “Agile Theater”

DDD promised tighter alignment between business and devs. But without a practical way to maintain that alignment, teams slide into ceremony-for-ceremony’s-sake.

- Standups turn into status recitals.
- Sprint reviews become awkward half-demos.
- The backlog bloats with junk no one remembers asking for.

Instead of real collaboration, you get Agile Theater: everyone playing their roles on stage, clapping politely, but the feature still misses the point.


---

👉 **In short:** DDD was a massive leap forward for its time, but applied unmodified today, it struggles. The “one universal language” doesn’t exist, translation gets skipped, and teams drift into agile cosplay. That’s not a failure of the idea - it’s just the reality of 20 years of evolution in software design.


---

---

## 📖 04.0.the-practical-domain-design-fix.md

# 4.0 The Practical Domain Design Fix

So if DDD isn’t broken, why are so many teams breaking *on* it? Because they’re trying to use it like it’s still 2003. Back then, monoliths ruled, deployments were rare, and most of the design patterns we now treat as table stakes hadn’t even been named yet.

Today, we build in a different world: APIs everywhere, distributed systems, devs juggling cloud, CI/CD pipelines, and “why is staging down again?” alerts at 2 a.m. Trying to run classic DDD in this context is like trying to text from a flip phone. The idea still works - but the interface is clunky.

That’s where **Practical Domain Design (PDD)** comes in.


---

## a. Core Idea: Two Languages, One Map

Instead of forcing everyone into one “ubiquitous language,” PDD takes the opposite approach: let each side keep speaking their native tongue.

- Business speaks in **departments, workflows, operations, and entities**.
- Devs speak in **modules, actions, services, and models**.

Neither side has to fake fluency. The bridge is a **translation map** that connects the two. It’s lightweight, visual, and keeps both sides honest.

👉 Think of it like subtitles on a foreign film. You don’t need the actors to switch languages. You just need a clear, reliable translation that makes sure everyone’s watching the same story.


---

## b. Strategic vs Tactical

Classic DDD lumps everything into “the domain.” PDD splits it into two clear phases, each with its own baseline and loop:

- **Strategic Phase (business reality):** Capture how the business actually runs - departments, workflows, ops, and entities. No “ideal future state,” just the messy now.
- **Tactical Phase (code reality):** Capture how the codebase actually works - modules, actions, services, and models. No “shoulds,” just what’s there today.

This two-baseline approach keeps business and dev honest. Later, when you lay them side by side, the gaps and misalignments jump out.


---

## c. The Loop as Connective Tissue

The real magic isn’t the baselines - it’s the **Loop.**

Every time a new pain point or idea comes in, it runs through the same cycle:

1. Capture it in **business terms** (strategic side).
2. Translate it into **technical terms** (tactical side).
3. Implement, validate, and demo it back in both languages.

No endless debates. No Agile Theater. Just a repeatable feedback loop that keeps both sides in sync without pretending they’re the same thing.

👉 In short: Practical Domain Design isn’t about reinventing DDD. It’s about modernizing it. We keep the spirit - alignment between business and code - but update the practice for today’s world. Two languages, one map, continuous translation. That’s the fix.


---

---

## 📖 05.0.getting-started-with-pdd.md

# 5.0 Getting Started with PDD

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

## 📖 06.0.0.strategic-pdd-the-language-of-business.md

# Strategic PDD - The Language Of Business

Every team thinks they know how the business runs… until they try to write it down. Suddenly, that “simple” billing process has six detours, two unspoken exceptions, and one undocumented spreadsheet only Karen from accounting knows about.

That’s why the Strategic Phase exists. Before we can fix anything, we need a clear snapshot of how the business actually works today - warts, duct tape, and all. Not how it should work, not how leadership likes to present it in slide decks, but how it really runs when customers are calling, orders are piling up, and the system is creaking.

The Strategic Phase has two parts:

Baseline: Document the business - departments, workflows, operations, entities. This is your map of “what is.”

The Loop: Capture pain points against that baseline and build a backlog in business terms. This turns raw complaints into structured inputs for the dev side.

👉 In short: The Strategic Phase is about building a shared reality. No silver bullets, no redesigns yet. Just an honest mirror held up to the business so everyone’s finally looking at the same starting point.
---

## 📖 06.1.0.strategic-baseline.md

# 6.1.0 The Strategic Baseline: Document the Business
Every team thinks they know how their business runs… until they try to write it down. Suddenly the “simple” billing process has six secret detours, and Support’s “standard” workflow turns out to be fifty shades of chaos.

That’s why we start PDD with the Baseline. This is not about fixing anything. It’s not about debating best practices. It’s about taking a clean snapshot of how the business actually operates today — warts, duct tape, and all.

Think of it like a map: you can’t plan a road trip until you know where you’re starting. The Baseline is that starting point.

The Four Building Blocks
When documenting the business, we care about four simple pieces:

Departments – The big buckets of responsibility.

Workflows – The repeatable processes each department runs.

Operations – The tasks inside each workflow.

Entities – The nouns the business deals with every day.

That’s it. No fancy jargon or synergistic buzzwords. Just business terms people already use.

## Departments
Departments are the easiest place to start. If the company cuts paychecks for it, it’s a department.

Sales

Billing

Support

HR

Operations

👉 Write them down as a list. Don’t argue about org charts or reporting lines. We just want the functional buckets of work.

## Workflows
Workflows are the repeatable processes a department runs. Each workflow has a clear start, a series of operations, and an end.

Think of a workflow as a story: When X happens, we do Y, which results in Z.

Examples (Billing Department):

Generate Invoice → (operations: Invoice.create, Invoice.send)

Handle Dispute → (operations: Dispute.open, Dispute.resolve)

Send Payment Reminder → (operations: Reminder.create, Reminder.send)

👉 If you can’t describe it as “When this event happens, we perform these steps to get to an outcome,” it’s not a workflow.

Workflows are the backbone of the Strategic Baseline. Later, when we connect them to the Tactical Baseline, you’ll see how each workflow coordinates a set of operations inside the code.

## Operations
Operations are the atomic steps inside a workflow. Each one is a single action taken against a business entity. They should be short, concrete, and verb-heavy.

Examples:

Team.updateName

Invite.create

Season.changeRegistrationCloseDate

👉 If an “operation” takes multiple checks, approvals, or branches, it’s not an operation - it’s a workflow.

Operations are where the business world starts to line up with the technical world. In the Tactical Baseline, these will map to Business Entity Services - e.g. “Update Team Name” becomes TeamService.updateName().

## Entities
Entities are the nouns your team touches. Customers, Invoices, Products, Tickets, Orders.

Example (Billing Entities):

Customer Account

Invoice

Payment Method

Entities often cross department lines. That’s a good thing. Later, when we compare the business baseline with the code baseline, those overlaps will expose gaps and misalignments.

Putting It All Together
Here’s a small Strategic Map for a fictional Billing department:


```yaml
Department: Billing
  Workflows:
    - Generate Invoice
        Operations:
          - Validate customer hours
          - Calculate totals
          - Issue invoice
        Entities:
          - Customer Account
          - Invoice
          - Payment Method
    - Send Payment Reminder
        Operations:
          - Identify overdue accounts
          - Generate reminder notice
          - Email customer
        Entities:
          - Customer Account
          - Invoice
```
👉 Notice how it’s just nested lists. Nothing fancy. This is the scratchpad view - the kind of quick sketch you’d throw together in a session to get the basics on paper.

Later, when you need to clean it up and share with others, you’ll use the structured templates in the appendix (Department Detail, Workflow Detail, etc.). Those templates give you consistency and clarity across the team, but the spirit is the same: Departments → Workflows → Operations → Entities.

Think of it as rough notes vs polished docs. Both are valid, just used at different moments in the loop.

Success Criteria
You know your baseline is “good enough” when:

You can show it to a new hire and they nod instead of squinting.

No one in the room says “that’s not how we do it.”

Aim to keep each department or module baseline on a single screen. If the map sprawls, break it into sub-baselines (e.g. “Billing Baseline,” “Membership Baseline”) instead of one giant hairball.

Why It Matters
Shared reality: Everyone stops pretending they know how things work and actually sees it on paper.

Foundation for backlog: The next step (The Loop) builds on this. You can’t capture pain points if you don’t know the workflows they belong to.

Low effort, high return: Two hours of mapping saves weeks of guesswork later.

👉 In short: The Baseline is just holding up a mirror. Don’t polish it. Don’t overcomplicate it. Just capture what is. We’ll worry about fixing things in the Loop.


---

## 📖 06.1.1.concept.md

# 6.1.1 Concept: Establish The Strategic Baseline - Documenting the Business

Every team thinks they know how their business runs… until they try to write it down. Suddenly the “simple” billing process has six secret detours, and Support’s “standard” workflow turns out to be fifty shades of chaos.

That’s why we start PDD with the **Baseline**. This is not about fixing anything. It’s not about debating best practices. It’s about taking a clean snapshot of how the business actually operates today — warts, duct tape, and all.

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

- Sales
- Billing
- Support
- HR
- Operations

👉 Write them down as a list. Don’t argue about org charts or reporting lines. We just want the functional buckets of work.


---

### 2. Workflows

Workflows are the **repeatable processes** a department runs. Each workflow has a clear start, a series of operations, and an end.

Think of a workflow as a **story**: *When X happens, we do Y, which results in Z.*

Examples (Billing Department):

- **Generate Invoice** → (operations: `Invoice.create`, `Invoice.send`)
- **Handle Dispute** → (operations: `Dispute.open`, `Dispute.resolve`)
- **Send Payment Reminder** → (operations: `Reminder.create`, `Reminder.send`)

👉 If you can’t describe it as “When this event happens, we perform these steps to get to an outcome,” it’s not a workflow.

Workflows are the backbone of the Strategic Baseline. Later, when we connect them to the Tactical Baseline, you’ll see how each workflow coordinates a set of operations inside the code.


---

### 3. Operations

Operations are the **atomic steps** inside a workflow. Each one is a single action taken against a business entity. They should be short, concrete, and verb-heavy.

Examples:

- `Team.updateName`
- `Invite.create`
- `Season.changeRegistrationCloseDate`

👉 If an “operation” takes multiple checks, approvals, or branches, it’s not an operation - it’s a workflow.

Operations are where the business world starts to line up with the technical world. In the Tactical Baseline, these will map to **Business Entity Services** - e.g. “Update Team Name” becomes `TeamService.updateName()`.


---

### 4. Entities

Entities are the nouns your team touches. Customers, Invoices, Products, Tickets, Orders.

**Example (Billing Entities):**

- Customer Account
- Invoice
- Payment Method

Entities often cross department lines. That’s a good thing. Later, when we compare the business baseline with the code baseline, those overlaps will expose gaps and misalignments.


---

### Putting It All Together

Here’s a small Strategic Map for a fictional Billing department:

``` 
Department: Billing
  Workflows:
    - Generate Invoice
        Operations:
          - Validate customer hours
          - Calculate totals
          - Issue invoice
        Entities:
          - Customer Account
          - Invoice
          - Payment Method

    - Send Payment Reminder
        Operations:
          - Identify overdue accounts
          - Generate reminder notice
          - Email customer
        Entities:
          - Customer Account
          - Invoice

```

👉 Notice how it’s just nested lists. Nothing fancy. This is the **scratchpad view** - the kind of quick sketch you’d throw together in a session to get the basics on paper.

Later, when you need to clean it up and share with others, you’ll use the **structured templates in the appendix** (Department Detail, Workflow Detail, etc.). Those templates give you consistency and clarity across the team, but the spirit is the same: Departments → Workflows → Operations → Entities.

Think of it as rough notes vs polished docs. Both are valid, just used at different moments in the loop.


---

## Success Criteria

You know your baseline is “good enough” when:

- You can show it to a new hire and they nod instead of squinting.
- No one in the room says “that’s not how we do it.”
- Aim to keep each department or module baseline on a single screen. If the map sprawls, break it into sub-baselines (e.g. “Billing Baseline,” “Membership Baseline”) instead of one giant hairball.


---

## Why It Matters

- **Shared reality:** Everyone stops pretending they know how things work and actually sees it on paper.
- **Foundation for backlog:** The next step (The Loop) builds on this. You can’t capture pain points if you don’t know the workflows they belong to.
- **Low effort, high return:** Two hours of mapping saves weeks of guesswork later.


---

👉 In short: The Baseline is just holding up a mirror. Don’t polish it. Don’t overcomplicate it. Just capture what *is*. We’ll worry about fixing things in the Loop.


---

---

## 📖 06.1.2.sop.md

# 6.1.2 SOP: Establish The Strategic Baseline - Documenting the Business

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

- Gather everyone together and list **all departments** in the business.
- Ask: “If payroll cuts a check for it, is it a department?”
- Write down department names (e.g., Billing, Sales, Support).
- **Assign a business owner** to each department - the person who will take responsibility for the workflows in that department.

**Why this matters:**

- Creates a single point of contact to confirm reality:
- “Yes, my department does that.”
- “No, that belongs to Jane’s team.”
- Helps the team start visualizing the company as structured roles instead of everyone doing everything.
- Sets you up for Tactical later when scopes, roles, and permissions come into play.

**Output artifact:** A list of departments with assigned owners.

👉 Pro tip: Don’t get stuck debating org charts. Owners aren’t necessarily managers. They’re the person who knows the work well enough to own the map.


---

## Step 2 - Brain Dump Workflows

- For each department, list the repeatable processes it runs.
- Ask: “When X happens, what do we do that ends with Y outcome?”
- Keep them short, e.g.:
- Generate Invoice
- Handle Dispute
- Send Payment Reminder

**Output artifact:** A rough list of workflows under each department.

👉 This is still high-level. Don’t overthink. Capture what people *say* they do. You’ll refine later.


---

## Step 3 - Department Deep Dive (Operations)

- Split into department-level huddles (still in the same room).
- Take the workflow list for your department and break each workflow into **operations**.
- Each operation = **verb + entity** (e.g., `Invoice.create`, `Dispute.resolve`).
- Keep it short. If a step has multiple branches or approvals, that’s probably a separate workflow.

**Output artifact:** A short list of operations under each workflow.


---

## Step 4 - Capture Entities

- Entities are the **nouns** your business touches (Customer, Invoice, Payment Method).
- Go back through the operations you listed - the nouns are usually right there.
- Write them down under the department.

**Output artifact:** A list of entities for that department.

👉 Entities often show up in multiple departments. That’s good - it’ll expose gaps later when you compare baselines.


---

## Step 5 - Assemble Scratchpad Maps

- Each department team assembles its own map: Departments → Workflows → Operations → Entities.

**Output artifact:** A Strategic Baseline scratchpad map for each department.

👉 Don’t stress about size. If one department has 138 workflows and another has 3, leave it that way. The number isn’t “wrong” - it’s a clue.

- A huge list might mean the department is overloaded, or it might just mean you’ve defined workflows too narrowly.
- A tiny list might mean the department is well-bounded, or it might mean you’ve missed detail.

Either way, the map shows you something important about how the business actually functions. That visibility is gold.


---

## Step 6 - Present and Review

- Have department owners present their maps while everyone else listens.
- Encourage questions and clarifications:
- “Does this look like reality?”
- “What’s missing?”
- “Who else is impacted by this?”
- Capture feedback and update the maps in real time.

**Output artifact:** Department Detail docs for each department, validated by the group.


---

### Success Criteria

You know your baseline is ready when:

- A new hire can look at it and nod instead of saying, “That’s not how we do it.”
- Every department has an owner who can confirm the workflows.
- The maps may be uneven across departments - and that’s fine. The differences themselves often tell you where to ask better questions later.

👉 In short: Don’t trim the map to make it “look nice.” Capture what’s real. Mess, imbalance, and lopsidedness are all useful signals for future backlog items.

---

## 📖 06.1.3.workshop.md

# 6.1.3 Workshop: Establish The Strategic Baseline - Documenting the Business

This agenda gives you a practical way to run the Strategic Baseline SOP (6.b) as a live workshop with your team. Time-boxed, structured, and designed to get from nothing → validated artifacts in one session.


---

## 🕘 9:00 – Kickoff (15 min)

- Welcome the group.
- Explain the goal: *“By lunch, we’ll have a clear map of how the business actually works, broken down by department.”*
- Quick overview of the process: Brain dump → Deep dive → Present & review.


---

## 📝 9:15 – Brain Dump Departments & Workflows (45 min)

- Gather everyone in a room with whiteboards or a shared doc projected.
- Step 1: List all departments.
- Step 2: List the main workflows under each department.
- Assign an owner for each department.
- Stop when there’s general agreement on the lists.

**Output:** A master list of departments, owners, and high-level workflows.


---

## 👥 10:00 – Department Huddles: Deep Dive (60 min)

- Split into department-level groups (still in the same room).
- Each group:
- Breaks workflows into operations.
- Captures entities touched by those operations.
- Assembles a scratchpad map (Dept → Workflows → Operations → Entities).

**Facilitator’s role:** Float between groups, answer questions, keep momentum.

**Output:** Department scratchpad maps.


---

## 🍴 11:00 – Lunch & Department Presentations (60 min)

- As people eat, department owners present their maps one by one.
- Encourage quick feedback and clarifications from the room:
- “Does this look like reality?”
- “What’s missing?”
- “Who else is impacted by this?”
- Update maps live based on feedback.

**Output:** Validated Department Detail docs.


---

## ✅ 12:00 – Wrap-Up & Next Steps (15 min)

- Recap what was captured.
- Highlight any obvious gaps or lopsided departments (signals for backlog).
- Explain where this leads: *“These baselines set us up for the next PDD phase.”*

**Final Output:** A complete Strategic Baseline across departments, ready for use in the PDD Loop.


---

👉 In short: Half a day, everyone in one room, real artifacts at the end.

---

## 📖 06.1.4.sop-ai.md

# 6.1.4 SOP: Establish The Strategic Baseline (AI-Assisted)

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

## 📖 06.2.0.strategic-loop.md


---

## 📖 08.1.strategic-to-tactical-translation-map.md

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

## 📖 7.0.0.tactical-pdd.md


---

## 📖 7.1.0.tactical-baseline.md


---

## 📖 7.1.1.concept.md

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

## 📖 7.1.2.sop.md


---

## 📖 7.1.3.workshop.md


---

## 📖 7.2.0.tactical-loop.md


---

