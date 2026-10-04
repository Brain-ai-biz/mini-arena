---
name: mini-arena
description: Makes rival drafts compete, judged harshly, best one survives. Use when unhappy with an answer, for anything important, or on "arena", "make them compete", "זירה".
---

# Mini Arena

One answer is a guess. A tournament is a choice. Instead of answering once, write several
genuinely different drafts, attack each one like a harsh judge, fix the strongest, make them
compete again, and hand over only the winner.

Everything happens inside a single reply. No sub-agents, no tools, no files, so it works in the
regular chat as well as in Claude Code.

## When to run

- The user is not happy with an answer and asks again ("try again", "not good enough", "עוד פעם").
- The user asks for it: "arena", "make them compete", "זירה", "תעשה זירה".
- The output matters: a headline, a hook, an email to a big client, a sales page section, a
  decision between options, a plan, a tricky piece of code.

Skip it for trivial requests (a fact, a conversion, a one-word answer). If unsure, ask in one
line whether to run the arena.

## Modes

| mode | trigger words | drafts | rounds |
| --- | --- | --- | --- |
| quick | "quick", "מהיר" | 4 | 1 |
| default | nothing said | 6 | 2 |
| deep | "deep", "עמוק", "all in" | 10 | 3 |

## The procedure

### 1. Lock the task

Write the task in one line, then 2 to 4 success criteria taken from the user's words and the
conversation (audience, length, tone, constraints). If the user rejected an earlier answer, that
answer is the one to beat, and why it was rejected becomes a criterion.

If the task itself is missing, ask one question and stop. Do not ask anything else.

### 2. Deal the cards

Each draft gets its own approach card, and no two drafts share one. Pick the cards that fit the
task from this deck, or invent sharper ones:

- **Simplest**: the plainest version that fully works
- **Provocative**: picks a fight with an assumption the reader holds
- **Reader first**: written from inside the reader's day and pain
- **Hard number**: built around one concrete, surprising, true number
- **Opposite**: says the reverse of what everyone expects
- **Story**: one specific moment, person or place
- **Constraint first**: starts from the hardest requirement and builds out
- **First principles**: rebuilds the answer from what the goal actually needs
- **Expert's eye**: what a top practitioner in this field would do
- **Ruthless cut**: the version with nothing removable left

For code, decisions or plans, use approach cards that fit (for example: fastest to ship, most
robust, cheapest, easiest to undo, edge cases first).

Write every draft in full. A draft that is just the card's name with a generic answer under it
loses automatically.

### 3. Judge, harshly

Switch roles. You are now a judge who did not write any of the drafts and wants to find flaws.
For each draft:

- name its single biggest weakness, concretely (what is wrong, what it missed, where it breaks)
- score it out of 100:

| criterion | points |
| --- | --- |
| fits the task and every success criterion | 30 |
| specific, not generic | 25 |
| impact: would it actually work on the real audience or problem | 25 |
| clear and tight | 20 |

A draft with a fatal flaw (a false claim, a missed hard requirement, broken logic) cannot win,
whatever its score.

### 4. Rematch

Take the top 3 (top 2 in quick mode). Rewrite each one to fix the weakness the judge named,
without blending them into one another. Judge them again on the same rubric. In deep mode, repeat
with the top 2 for a third round.

### 5. Deliver

Lead with the winner, ready to use, then one line on why it won. Keep the rest short:

```
**The winner:** <the answer itself>

Why it won: <one line>

Runner-up: <one line, only if it is a real alternative in a different direction>
```

Show the full bracket (all drafts, weaknesses and scores) only when the user asks to see the
fight, or when they asked for a decision and the trade-offs matter.

## Rules

- Write in the user's language. Hebrew in, Hebrew out.
- Never invent facts, numbers or quotes to make a draft stronger. If a draft needs a real number
  the user did not give, mark it as a placeholder, for example [your real number], and say so.
- Scores are your judgment against the rubric, not a measurement. Never present them as proof.
- If the earlier answer the user rejected beats every new draft, say so plainly and explain why.
- The winner must be usable as is. No meta commentary inside the answer itself.
