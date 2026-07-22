---
title: "Ako-Kupu — Te Reo Māori Learning App"
date: 2026-06-01
summary: "Learners need low-friction practice to retain Te Reo Māori vocabulary — this flashcard and progress-tracking web app adds an AI learning layer that degrades gracefully so the core stays available even without an API key"
tags:
  - Full-Stack
  - Python
  - AI
tech_stack:
  - Flask
  - PostgreSQL
  - psycopg 3
  - Google Gemini API
  - Docker
  - Render
  - pytest
links:
  - type: github
    url: https://github.com/eirikrbe/Ako-Kupu
    label: Code
  - type: live
    url: https://ako-kupu.onrender.com
    label: Live app
page_links: {}
featured: true
status: "Live"
role: "Two-person team (with Yirong Chen)"
team_size: 2
highlights:
  - "AI features degrade gracefully — the app runs fully without an API key"
  - "Raw psycopg 3 database layer, no ORM"
  - "Pylint ≥ 8.0 enforced before every commit"
---

*Kupu* means words; *ako* is the reciprocal learning between teacher and student. Ako-Kupu is a Te Reo Māori flashcard and learner-progress web application built as a two-person team project for MSE800 at Yoobee College.

## What it does

Learners work through Te Reo Māori vocabulary as flashcards and track their progress over time. An AI learning layer built on the Google Gemini API enriches the experience — and the app is deliberately designed to boot and run without the API key, with only the AI features degrading.

## How it's built

- **Flask** with the app-factory pattern and blueprints
- **Neon PostgreSQL** accessed through raw **psycopg 3** — no ORM, so the SQL is explicit and reviewable
- **Docker** for containerisation, deployed on **Render**
- **pytest** for tests, with **Pylint** (minimum score 8.0) enforced before commits

## Process

The project ran on a full Jira and Confluence workflow with three sprint epics, using the GitHub for Jira integration so branches, commits and pull requests were linked to issues via issue keys.
