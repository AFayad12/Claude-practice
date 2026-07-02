# CLAUDE.md

## My Second Brain
My Obsidian vault is stored at:
C:\Users\abdelrahman fayad\Desktop\Obsidian\Claude-Brain

After completing ANY task, automatically do the following:

1. Open My Profile.md and update it if any of these changed:
   - A new project was built or updated
   - A new skill was added
   - A new MCP server was connected
   - My setup changed in any way

2. Open Lessons Learned.md and add a new entry if:
   - We fixed a bug and I should remember why
   - We discovered something that didn't work and why
   - I learned a new command or workflow
   - We solved an error I might hit again

Keep all updates short and clear — one line per lesson.
Never delete existing notes, only add to them.
After updating, tell me exactly what you added so I can see it.

Before starting any task, read My Profile.md and Lessons Learned.md from that folder to understand who I am and what I already know.
This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static personal website for Abdo with six pages: Home, About, Hobbies, Quiz, My Journey, and Dashboard. No build system, bundler, or external dependencies — open any `.html` file directly in a browser.

## Architecture

All styling is inline `<style>` blocks within each HTML file — there is no shared stylesheet. Each page duplicates the same nav and base CSS (body, nav, card). The design uses a deep purple background (`#2d0057`) with translucent white cards and a consistent nav bar where the current page gets `class="active"`.

When adding a new page:
1. Copy the nav and base styles from an existing page.
2. Add a link to the new page in the nav of all six existing files.
3. Set `class="active"` only on the link matching the current page.

## Completed Projects

| File | Description |
|------|-------------|
| `index.html` | Home page — a welcome landing card with Abdo's name and a short intro |
| `about.html` | About page — a card with personal background and highlighted details about Abdo |
| `hobbies.html` | Hobbies page — a grid of cards, each describing one of Abdo's hobbies |
| `quiz.html` | Quiz page — an interactive multiple-choice quiz |
| `journey.html` | My Journey page — a timeline telling the story of Abdo's learning journey |
| `dashboard.html` | Dashboard — a productivity app with a to-do list, Pomodoro focus timer, daily goals tracker with progress bar, and a sticky-note-style notes section with localStorage persistence |

## Skills Learned

Claude Code features and skills Abdo has used so far:

- **Generating files from scratch** — describing what you want in plain English and having Claude build the full HTML/CSS/JS
- **Editing existing files** — asking Claude to make targeted changes to specific parts of a file without rewriting everything
- **Multi-file edits** — having Claude update several files at once (e.g. adding a nav link to all six pages simultaneously)
- **Plan mode** — using plan mode to see and approve a detailed plan before any code is written, so there are no surprises
- **The `/verify` skill** — having Claude automatically open the page in a real browser (using Playwright) and test that every feature works, with a screenshot as proof
- **The `/ultraplan` skill** — sending a plan to the cloud for review and editing in a browser (requires a git repository with a GitHub remote)
- **`git init`** — initialising a git repository to enable version control and unlock Claude Code cloud features like ultraplan
- **Memory** — Claude remembers preferences and project details across separate conversations so you don't have to repeat yourself

## Developer Preferences

- The developer's name is Abdo. He is a beginner learning Claude Code.
- After finishing any task, always explain what was done in simple, plain language.
- Always use a dark purple color theme for any visual project.
- Never use complicated technical words without explaining them first.

## MCP Servers Installed
- **fetch** — lets Claude browse websites like Wikipedia and documentation pages

## Skill Files Installed
- **review-html** — reviews HTML files for bugs, inconsistencies, and style issues. Use with /review-html