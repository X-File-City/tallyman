---
name: planning-rules
description: Guides how we create new plans and store them in the project.
---

# Overview

This document guides how we create new plans and store them in the project.

## Save plans and number them

When we create a plan, even in planning mode, we always want to create this plan
as a durable markdown file. This allows us to save and reuse the document rather
than generating an ephemeral plan not stored in source control.

You should create the plan named NNN-plan-description.plan.md in the project's plan folder.
Not .cursor/plans, but workspace_root/plans.

## Split large plans / features

For larger plans and features, we want to use a multi-step process. Our plans usually include
phases: phase 1: ..., phase 2: ..., etc.

In this case, we create a plan in a subfoder of plans named NNN-plan-description. Then we
create multiple markdown files named:

NNN-plan-description/
    - 00-plan-introduction.plan.md
    - phase-01-phase-name.plan.md
    - phase-02-phase-name.plan.md
    - phase-03-phase-name.plan.md

And so on. The 00-plan-introduction.plan.md ties all of these files together and sets the stage for the project/feature.

## The user prefers if you interview them

When creating the plan, please interview the user to clarify every detail if you are unsure.

## Audience

The plan is for you and the user to collaborate on buildig out a feature or fix. But you should ultimately structure the outputs assuming they will be handed to you (the AI) directly to implement the changes.
