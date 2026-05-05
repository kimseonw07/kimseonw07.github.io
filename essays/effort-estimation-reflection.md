---
layout: essay
type: essay
title: "Effort Estimation and Tracking: A Reflection"
date: 2026-05-04
published: true
labels:
  - Effort Estimation
  - Software Engineering
  - Project Management
  - StudyViser
---

## How did you make your effort estimates?

My effort estimates were primarily based on task similarity and past experience with comparable work. For most issues, I reasoned by analogy: if a previous task of similar complexity had taken a certain amount of time, I used that as an anchor for the new estimate, adjusting up or down based on perceived difficulty or unfamiliarity.

For example, when estimating the Student Dashboard Mockup (Issue #4), I set 180 minutes because I expected the design iteration and layout planning to be time-consuming, even though no actual code was involved. Similarly, for the Static Instructor Dashboard Layout (Issue #21) and the Static Student Course Study Page (Issue #22), I budgeted 120–240 minutes based on how long prior static layout work had taken in earlier milestones.

For more complex tasks like Collate glossary terms for a course into a viewable study guide (Issue #45) and Term View page (Issue #46), I estimated 300 and 240 minutes respectively, recognizing that these involved both non-trivial UI design and database logic. I also factored in a buffer for debugging and iteration, which I have found to consistently be underestimated in past projects.

## Did estimating in advance provide any benefit?

Yes, even when my estimates were off, the act of estimating upfront provided meaningful benefits for planning and prioritization.

One concrete example: estimating Issue #45 (Collate glossary terms) at 300 minutes made me realize early on that it was one of the heavier tasks in the milestone. This prompted me to start it earlier rather than leaving it to the end of the sprint. Had I not estimated it explicitly, I might have mentally categorized it as a "medium" task and deprioritized it.

Another benefit was team coordination. When estimates were visible on the GitHub project board, it helped the team quickly see which issues were lightweight versus heavyweight, and informally balance workload without needing a formal planning meeting. For instance, when Noah picked up shorter tasks like Playwright testing (Issue #28, estimated 60 minutes), it was partly because the board signaled that my tasks were already taking up a large chunk of time.

## Was tracking actual effort useful?

Tracking actual effort was genuinely useful, though the benefit was most apparent in hindsight rather than in real-time. Seeing the gap between estimated and actual effort helped me recalibrate my mental model of how long certain categories of work actually take.

A clear example is Issue #22 (Static Student Course Study Page), which I estimated at 240 minutes but only logged 120 minutes of coding effort and 120 minutes of non-coding effort. On the surface this might look like I overestimated, but the non-coding time reflected significant design research and iteration in Figma before writing any code. Seeing this breakdown made me realize I should split design-heavy issues into separate sub-tasks in future milestones, rather than collapsing them into a single estimate.

Tracking also helped with Issue #14 (Student Dashboard in deployment), where the actual effort of 120 minutes coding and 60 minutes non-coding came close to my 120-minute estimate. That gave me confidence that my intuition for deployment-adjacent tasks is reasonably calibrated.

## How did you track your actual effort?

I used a personal device timer to track both coding and non-coding effort. For coding sessions, I started the timer when I opened VSCode and stopped it whenever I took a break of more than a few minutes. I was careful not to include idle time such as context-switching, checking messages, or looking something up unrelated to the task.

For non-coding effort, I used the same timer method, noting start and stop times when performing activities such as design planning, researching component libraries, and writing documentation. I also kept brief notes in a text file to record what I was doing during each non-coding session, which made it easier to accurately assign time to specific issues after the fact.

In terms of accuracy, I believe my coding effort tracking was reasonably reliable (within 10–15%), though I likely undercounted some short coding bursts of 5–10 minutes that did not seem worth starting the timer for. My non-coding tracking may be slightly less accurate, as some activities like thinking through a design problem while away from the desk are difficult to capture.

## What would you change next time?

There are two main things I would change in future projects. First, I would adopt a more structured tool for tracking, such as WakaTime for coding effort, rather than relying solely on a manual timer. WakaTime eliminates the friction of remembering to start and stop a timer and provides automatic file-level granularity, which would make it easier to attribute time to specific issues when working across multiple tasks in a single session.

Second, I would decompose large issues more aggressively before estimating. Several of my issues (e.g., Issue #45, #46) were broad enough that they combined design, implementation, and testing into a single ticket. This made it harder to produce a meaningful estimate and also made it difficult to isolate where time was being spent. Breaking these into two or three sub-issues with individual estimates would improve both accuracy and manageability.

## AI Use in Effort Estimation and Implementation

I used two AI tools during the project: ChatGPT (GPT-4o, OpenAI) and Claude (claude-sonnet, Anthropic). These were primarily used for implementation assistance rather than for effort estimation itself, though they indirectly affected my estimates by changing how quickly I could complete certain tasks.

**ChatGPT (GPT-4o)**

I used ChatGPT mainly for generating boilerplate UI code and troubleshooting TypeScript type errors. A representative prompt I used was: "Given this Next.js component structure, generate a responsive card layout for displaying glossary terms with a search input at the top." The generation time was typically under 10 seconds. I spent roughly 5–10 minutes per use on prompt refinement and 10–15 minutes verifying and adapting the output to fit the project's design system. About 60–70% of the generated code was accepted with minor modifications; the remaining 30–40% required more significant refactoring, particularly around state management and Tailwind class conflicts.

**Claude (claude-sonnet)**

I used Claude primarily for explaining unfamiliar API patterns and reviewing logic in database query code. A typical prompt looked like: "Here is my Prisma query for fetching a student's submitted glossary terms grouped by course. Is there a more efficient way to write this, and can you explain why?" Claude's responses tended to be more explanatory than ChatGPT's, which was helpful for learning but sometimes required me to spend more time reading and extracting the directly usable parts. I estimate roughly 5 minutes per prompt on setup, 1–2 minutes on generation, and 10–20 minutes on verification and integration. Roughly 50% of the suggestions were used directly; the rest informed my approach without being copied verbatim.

Overall, AI assistance accelerated implementation significantly for tasks like Issue #27 (Term view) and Issue #45 (Collate glossary terms), both of which had estimated coding efforts of 120 minutes. The actual time was close to the estimate in part because AI-generated scaffolding reduced the time spent on repetitive boilerplate. However, the time saved on generation was partially offset by the time spent on verification and debugging AI output, which I have tried to honestly account for in my coding effort totals.
