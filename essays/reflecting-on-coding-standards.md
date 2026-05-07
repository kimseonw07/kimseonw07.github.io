---
layout: essay
type: essay
title: "Why Coding Standards Felt Painful but Necessary in Learning TypeScript"
date: 2026-02-11
published: true
labels:
  - Coding Standards
  - Software Engineering
  - ESLint
  - TypeScript
---

<img width="200px" class="rounded float-start pe-4" src="../img/ESLint.png" alt="ESLint logo" />

## Struggling with Coding Standards at First
At the beginning of the module, coding standards felt more frustrating than helpful. After writing TypeScript code that compiled and ran correctly, I often had to go back and fix a wave of ESLint warnings before I could move on. A function I had finished and tested would suddenly be covered in red underlines — not because the logic was wrong, but because I had written `const result = compute()` without annotating the return type, or left behind a `let i` that I had used during debugging and forgotten to remove.

One specific rule that caught me off guard early was `@typescript-eslint/explicit-function-return-type`. I had written a short helper that returned a filtered array and assumed TypeScript would infer the type without any annotation from me. ESLint flagged it immediately. Adding `: Student[]` to the signature felt unnecessary at the time since the return value was obvious from reading the code. But these small interruptions stacked up, and fixing them took time I had mentally already allocated to the next task.

## ESLint as a Source of Cognitive Load
One of the most challenging aspects was the mental overhead ESLint introduced. Writing code while simultaneously anticipating potential linting errors required a different kind of attention than I was used to. Even minor issues surfaced the moment I saved the file. At one point I was working through a WOD and introduced a temporary `console.log` for debugging. As soon as I typed it, ESLint flagged `no-console`. I knew I was going to remove it — it was a debugging line — but seeing the warning appear before I even finished the thought broke my focus.

However, this pressure also revealed gaps in my understanding. Several errors were not arbitrary. When ESLint flagged `@typescript-eslint/no-explicit-any` on a variable I had typed as `any` because I was unsure of its actual shape, it forced me to stop and work out what the type should actually be. In one case, that investigation revealed I was passing data between two functions in a way that was inconsistent — one expected an array, the other was treating it as a single object. The linter did not catch the logic error directly, but it surfaced the underlying type confusion that would have caused a runtime problem later.

## Recognizing the Value for Code Quality
As the module progressed, my perspective began to shift. Although fixing linting issues remained time-consuming, I started to see how coding standards improved overall code quality in concrete ways. When I revisited a TypeScript file I had written two weeks earlier, I could read through it quickly because every function had an explicit return type, every variable had a clear and consistent name, and there was no dead code cluttering the logic. None of that would have been true if I had been writing under no constraints.

I also noticed that the `no-unused-vars` rule quietly prevented a category of bug I had run into before: keeping a stale variable around that I thought was still connected to the rest of the code. ESLint surfaced it immediately instead of letting it silently drift out of sync.

## Coding Standards in Collaborative Environments
The real value of coding standards became most apparent when considering collaboration. In a team setting, consistent rules establish shared expectations. Instead of debating whether a function needs a return type annotation or whether `var` is acceptable, the linter decides — and everyone moves on. ESLint acts as a neutral enforcer that removes personal style from code reviews so reviewers can focus on logic and design instead.

This benefit becomes even more important in large-scale projects. Small inconsistencies accumulate quickly in large codebases. A team where one developer uses `any` liberally and another annotates every variable carefully will produce code that is difficult to read and even harder to refactor. Shared standards prevent that drift from the start.

## Long-Term Perspective on Discomfort
Looking back, the discomfort I experienced seems like a necessary part of the learning process. The frustration was real — there were moments where I just wanted the linter to leave me alone long enough to finish a thought. But those interruptions trained habits that I now find genuinely useful. I write explicit return types by default now, not because ESLint requires it, but because I have internalized the reason it matters.

This module helped me understand that professional software engineering prioritizes sustainability over short-term speed. Enforcing standards slows you down at the beginning and speeds you up over the long run. That tradeoff felt abstract when I first read about it, but after a semester of living it, it feels like one of the more practically valuable things I learned.

### Use of AI
AI tools (ChatGPT) were used to assist with organization, grammar, and clarity. The ideas and reflections presented in this essay are my own and are based on my personal experience during this semester.
