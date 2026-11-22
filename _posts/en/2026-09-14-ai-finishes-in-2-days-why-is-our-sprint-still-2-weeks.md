---
title: "AI Finishes in 2 Days, So Why Is Our Sprint Still 2 Weeks?"
description: "Parkinson's Law in the age of Agentic Engineering: when AI makes coding far faster, the bottleneck moves from writing software to making decisions."
ref: ai-two-days-two-week-sprint
authors: [ahmad]
image: /assets/images/ai-selesai-2-hari/cover.jpg
---

*Originally published in Indonesian on [daus95.com](https://daus95.com/2026/09/14/ai-bisa-selesai-dalam-2-hari-kenapa-kita-masih-pakai-sprint-2-minggu/), September 14, 2026. This is an English translation.*

There is a simple law that has been known for a long time:

> “Work expands to fill the time available for its completion.”

Work tends to grow to match the time we give it.

This principle is known as Parkinson’s Law, introduced by C. Northcote Parkinson in 1955.

A simple example.

Imagine we ask someone to write a report and give them two weeks. Chances are the report will only really be finished near the end of the second week.

But if we had said from the start that the report must be done by tomorrow afternoon, it often turns out the same work could be done in a single day.

That doesn't mean the person was deliberately slacking. What happens is usually more subtle.

When there is plenty of time, we tend to hold more discussions, weigh more alternatives, do more revisions, wait longer to make decisions, and add work that wasn't considered necessary before.

In the end, the work expands to match the time available.

## Then came AI

Parkinson’s Law gets even more interesting once we enter the era of AI, especially Agentic Engineering.

In traditional software engineering, a feature might be estimated to take two weeks to build.

So we create two-week sprints.

The team does planning, then the developers start coding. After that come code review, testing, bug fixing, deployment, and many other activities.

Two weeks later, the feature is done.

Now imagine the same work done with the help of an AI coding agent.

AI can read the spec, study the codebase, make changes across many files, run tests, find errors, fix them, and run the tests again.

Coding work that used to take several days might now be done in a few hours.

The question:

Will the feature now be done in a few hours?

Not necessarily.

The process could very well still look like this:

<figure class="fig fig-img"><img src="{{ '/assets/images/ai-selesai-2-hari/alur.jpg' | relative_url }}" alt="Workflow: AI finishes coding in 4 hours, then waits for review, waits for QA, waits for a meeting, enters the next sprint, and is finally done two weeks later. Total time about 2 weeks, even though the coding took only 4 hours." width="2172" height="724" loading="lazy"><figcaption>The diagram is in Indonesian. In English: AI finishes coding in 4 hours → waiting for review → waiting for QA → waiting for a meeting → enters the next sprint → done two weeks later. Total time: about 2 weeks (even though the coding itself took only 4 hours).</figcaption></figure>

AI makes the work much faster, but the way of working around it still runs on the old assumptions.

As a result, engineering productivity may go up 10 times, but the speed at which the organization produces something does not go up 10 times.

This is Parkinson’s Law in a new form.

## The problem is no longer coding speed

For decades, one of the biggest bottlenecks in software development was the human ability to write software.

That is why we measured capacity so much.

- How many developers do we have?
- How many days do they work?
- How many story points can we finish in one sprint?

In simple terms, the model looks like this:

<figure class="fig fig-img"><img src="{{ '/assets/images/ai-selesai-2-hari/old.jpg' | relative_url }}" alt="The old model: People (a team with various roles) determine Capacity (number of people, working hours, skills and tools, infrastructure and environment), which determines Time (for example 2 weeks, or 1 sprint), which produces Output (software that is finished and ready to use)." width="2172" height="724" loading="lazy"><figcaption>The diagram is in Indonesian. In English: <strong>People</strong> (a team with various roles: Developer, Product Owner, QA, Designer, Business Analyst) → <strong>Capacity</strong> (the amount of time and ability available: number of people, working hours, skills and tools, infrastructure and environment) → <strong>Time</strong> (time to finish the work, e.g. 2 weeks, or 1 sprint) → <strong>Output</strong> (the software produced: a feature that is finished and ready to use).</figcaption></figure>

Agentic Engineering is starting to change that relationship.

If AI can help with coding, testing, debugging, documentation, and many other engineering tasks much faster, then the amount of human time is no longer directly tied to the amount of software that can be produced.

The more important question changes from:

> “How much work can we finish in two weeks?”

to:

> “What must be done, and what tells us it is done?”

The difference looks small, but it is actually very fundamental.

## From Time-Box to Outcome

In the traditional approach, we often start from time.

For example:

We have a two-week sprint. What can we finish?

Agentic Engineering lets us flip that way of thinking.

We start from the outcome.

For example:

Users must be able to pay using QRIS.

Then we define clearly what done means: what must be fulfilled and what is optional.

For example:

**Mandatory** — must be available for the QRIS payment feature to be acceptable:

- the system can generate a QR code with the correct transaction amount;
- a successful payment changes the transaction status to Paid;
- a failed or expired payment must not change the transaction to Paid;
- the same transaction must not be recorded twice.

Meanwhile, there are things that add value but don't have to be there for the core function to be usable.

**Optional:**

- the payment page has a countdown timer;
- the system sends a payment confirmation email;
- the admin dashboard has a chart of QRIS transactions;

AI then helps the team produce the implementation very quickly.

This is exactly where the human role becomes more important.

After seeing the result, humans have to make a decision:

Is the mandatory implementation that was produced good enough to accept?

Technically everything may work, but the user experience turns out to be confusing. The team then decides that a certain improvement actually has to become mandatory.

Conversely, a requirement that was first considered important may turn out to be unnecessary once we see the app running.

New needs can also appear along the way.

For example, after trying the QRIS payment, the team realizes that users need to know how long the QR code is valid. The countdown timer, which was considered optional before, is then raised to mandatory.

Or the business situation changes, and priorities change with it.

None of these decisions are made by AI.

It is humans who decide what is good enough, what is still lacking, and what is most valuable to work on next.

Once all the mandatory needs are acceptable, the team makes another decision.

Are the benefits of building the optional features big enough to justify continuing?

Or is it better to stop and use the available engineering capacity on other backlog items that deliver more value?

With this way of thinking, work doesn't automatically keep growing just because there is still time available.

Time does not decide when the work is finished. Human judgment about whether the outcome is sufficient does.

## Humans become Decision Makers

This is where Agentic Engineering differs from simply using AI to speed up coding.

AI makes the implementation cycle extremely fast.

Something is built, a human looks at the result and gives feedback, and then AI produces the next version.

The cycle can become:

<figure class="fig fig-img"><img src="{{ '/assets/images/ai-selesai-2-hari/new.jpg' | relative_url }}" alt="The new cycle: Build (AI does the implementation based on the spec), Review (a human reviews the result), Decide (decide what is good enough, what needs to change, and what comes next), Adjust (give direction for changes, clarify requirements, or adjust priorities), Build Again (AI works on the next version). Iterate until the outcome is reached." width="2172" height="724" loading="lazy"><figcaption>The diagram is in Indonesian. In English: <strong>Build</strong> (AI does the implementation based on the spec) → <strong>Review</strong> (a human reviews the result: works, tests pass, needs fixes) → <strong>Decide</strong> (decide what is good enough, what needs to change, and what is next: “Good enough?”, “Needs changes?”, “What's next?”) → <strong>Adjust</strong> (give direction for changes, clarify requirements, or adjust priorities: fix the UI, add validation, change priorities, more detailed spec) → <strong>Build Again</strong> (AI works on the next version with the latest direction). Iterate until the outcome is reached.</figcaption></figure>

In the past, one such cycle might take several days or even weeks.

With AI, the same cycle can happen several times in a single day.

As a result, the work of humans shifts.

The less time it takes to turn decisions into code, the larger the share of human time that goes into making decisions.

Humans have to keep answering questions like:

- Is this result good enough?
- Did we learn anything new after seeing the result?
- Is there a new requirement that must now become mandatory?
- Is something that was mandatory before actually not that important?
- Have the business priorities changed?
- Is the next optional feature still worth building?
- Or is it better to stop now and move on to a more valuable backlog item?

So in Agentic Engineering, humans are not merely the people who give instructions to AI.

Humans are the decision makers in an engineering loop that runs far faster.

## Definition of Done becomes a living decision

Because of this, the Definition of Done in Agentic Engineering is not always a checklist made at the start and followed mechanically to the end.

We still need an initial definition of mandatory and optional.

But as real results start to appear, our understanding grows too.

We may discover something we hadn't thought of before.

We may have misjudged what users need.

We may find that a feature that looked important doesn't actually deliver much value.

Or the opposite: something first considered an extra turns out to be decisive for the product's success.

That is why the Definition of Done becomes something humans keep evaluating throughout the process.

This doesn't mean the target may change without control.

On the contrary, those changes must be conscious decisions, based on what we learned from the work already delivered.

AI shortens the distance between idea and implementation.

Humans use that implementation to make the next decision.

## Don't make AI faster. Make decisions faster.

There is a mistake many companies are likely to make.

They buy AI coding tools and expect productivity to jump. Developers do then produce code much faster. But the organization's processes don't change.

- Finished work waits for review.
- Decisions wait for the next meeting.
- Requirement changes wait for approval.
- QA waits for its schedule.
- Stakeholders only see the work at the end of the sprint.

In this situation, AI is already working in hours, but the organization is still making decisions in days or weeks.

The bottleneck moves.

In the past, the bottleneck may have been the ability to produce software. In Agentic Engineering, the bottleneck increasingly shifts to the human ability to evaluate results and make decisions.

That is why the transformation to Agentic Engineering can't be done just by giving developers an AI coding assistant.

We also have to redesign how humans review, learn, decide, and set priorities.

## From Utilization to Outcome

This also changes how we look at productivity.

In traditional organizations, management is often uncomfortable seeing an engineer who isn't busy. So management tries to increase utilization.

Everyone must have a task. All capacity must be filled.

But in a system that uses a lot of AI, that measure is increasingly irrelevant.

Imagine a team manages to produce all the mandatory functions it needs in just two days, when the work was previously estimated to take two weeks.

The team then assesses the result and concludes:

This is good enough to use. There are still eight days left.

Should we keep improving the feature just because the sprint hasn't ended? Not necessarily.

There may be five optional features that could still be built. But there may be other backlog items that bring far greater business benefit. So the more rational decision is:

Stop. This is enough. Move on to the next outcome.

This is where the link between Agentic Engineering and Parkinson’s Law becomes very clear.

Parkinson’s Law says:

> Work expands to fill the time available.

Agentic Engineering should push us to do the opposite:

Don't let the available time decide the size of the work. Let the sufficiency of the outcome and our priorities decide when we stop and move on to the next piece of work.

## A simple principle for Agentic Engineering

AI makes our ability to produce software grow very quickly.

But that doesn't mean we should produce as much software as possible.

On the contrary, as producing software gets cheaper, the ability to choose what is worth building becomes more important.

That is why the main question of Agentic Engineering is no longer:

> “What else can we work on?”

But:

> “Is what we've produced enough to reach the goal?”

If not yet, continue.

If we learn something new along the way, re-evaluate what is mandatory, what is optional, and the priorities.

If it is enough, decide whether additional work still adds value.

And if it doesn't, stop.

Move on to the next, more valuable outcome.

In the end, AI may make engineering run much faster.

But it is humans who must decide where we are heading, when something is enough, and when it's time to stop.
