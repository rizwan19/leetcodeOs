# LeetcodeOS

A personal Leetcode coaching system designed to run inside [Claude Code](https://claude.com/claude-code).

Instead of grinding problems in isolation, this setup turns Claude into a coach that:
- Suggests the next problem based on your weakest patterns and spaced-repetition schedule
- Uses Socratic nudges instead of handing you the solution
- Tracks every solve, review, skip, park, and retire in a single Markdown file
- Schedules reviews with a tuned SM-2 spaced-repetition algorithm
- Calls out aha moments and pattern connections after each solve

It is one repo, two files: `CLAUDE.md` (the coach's instructions) and `progress.md` (your log). That's the whole system.

## How it works

When you open this folder in Claude Code, Claude reads `CLAUDE.md` automatically and follows the session protocol there:
1. Reads `progress.md` to see what you've done
2. Computes the gap since your last session and calibrates accordingly
3. Checks the Spaced Repetition Queue for items due today
4. Looks at Pattern Targets to find your weakest area
5. Suggests 1–2 problems with reasoning, not solutions

After you solve (or skip, or fail) a problem, Claude updates `progress.md` for you — Problem Log, Stats, Weekly Progress, Pattern Targets, Category Coverage, the SR Queue, and Session Notes — then commits.

## Getting started

1. Clone or download this repo into a folder on your machine.
2. Open the folder in Claude Code.
3. Tell Claude something like *"let's start a session"* or just *"hi"*. It will read `CLAUDE.md` and `progress.md` and propose a starting problem.
4. Solve the problem in your editor of choice (LeetCode site, IDE, paper — wherever). Then tell Claude how it went and your confidence 1–5. The log updates from there.

You don't need to memorize anything in `CLAUDE.md` — Claude does. You just respond in plain English.

## What's tracked

- **Problem Log** — every solve and review, with attempt counts and notes
- **Spaced Repetition Queue** — when each problem is due for review (SM-2)
- **Parked Problems** — ones above your current level, with bridge problems to build toward them
- **Retired Problems** — ones you've explicitly dropped from rotation
- **Pattern Targets** — count progress per pattern (Arrays, DP, Graphs, etc.)
- **Category Coverage** — qualitative notes per category
- **Requested Problems** — interview asks or specific problems to prioritize
- **Session Notes** — free-form observations, aha moments, lesson recaps

## Customizing

Both files are yours to edit. The most common tweaks:

- **Pattern targets:** in `CLAUDE.md` and `progress.md`, change the per-pattern target counts to match your roadmap (NeetCode 150, Blind 75, your own list).
- **Weekly target:** the goal is 3 problems/week — change it in `progress.md`.
- **SR algorithm:** the SM-2 parameters live in `CLAUDE.md` (first-rep intervals, lateness decay rule). Tune to taste.
- **Confidence scale:** the 1–5 mapping to SM-2 grades is in `CLAUDE.md`.

## Why this exists

Spaced repetition works for memorization, but most Leetcode trackers don't apply it. Tools like Anki are good at scheduling but bad at picking *which* problem you should be doing next based on pattern coverage. A coach prompt that reads your full history every session and reasons about gaps is a closer fit. This is that prompt, plus the log it operates on.

## License

MIT — see `LICENSE`.
