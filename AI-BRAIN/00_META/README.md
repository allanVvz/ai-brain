---
tags: [meta, vault, system, readme]
type: meta
applies_to: [all]
---

# README

## Purpose

This vault is the source of truth for all flows, skills, and rules used by AI agents in this system.

## Usage

- Always instruct the AI to reference this vault before responding
- Rules override task instructions
- Skills define agent behavior
- Flows define routing logic

## Structure

- `01_RULES/` — global constraints and output format rules
- `02_SKILLS/` — agent role definitions
- `03_FLOWS/` — step-by-step execution flows
- `04_MEMORY/` — pattern storage
- `05_ENTITIES/` — brand and product data
- `06_PATTERNS/` — detected signal-action pairs
- `07_PROMPTS/` — base prompt templates
- `08_LOGS/` — daily improvement logs
