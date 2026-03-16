# MLOps Assignment 4

## What this repo does
This repo contains a GitHub Actions pipeline for ML model CI.

## Bugs Found and Fixed

### Bug 1 — Missing Checkout Step
Without actions/checkout, the runner has no access to repo 
files and the pipeline crashes immediately.

### Bug 2 — Incomplete Linter Step  
A step with only a name and no run/uses command is invalid 
YAML syntax and prevents the pipeline from starting.

### Bug 3 — Wrong Branch Trigger
Changed from `branches: main` to `branches-ignore: main` 
so the pipeline runs on feature branches, not main.

### Bug 4 — Missing Artifact Upload
Added upload-artifact step to save README.md as project-doc.
