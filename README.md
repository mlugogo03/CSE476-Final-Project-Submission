# CSE 476 Final Project -- Agent Implementation

## Overview

This project implements an automated question-answering agent
designed for the final evaluation of CSE 476. The agent reads 
questions and determines the domain (math, logic, science, etc.), then sends
each question to a custom model endpoint before saving all answers in a JSON
output file.

The system includes: 
- A domain-aware prompting mechanism
- A fallback reasoning system to guarantee answers even when the model fails
- Complete logging of the call count and progress


## How the Agent Works

### 1. Domain-Aware Prompting

The agent uses different system prompts depending on the question
category.

### 2. Answer Generation (`single_call`)

Handles API request construction, domain logic, and response parsing.

### 3. Smart Fallback System

Provides answers when the model times out or errors.

### 4. End-to-End Workflow

The `main()` function loads data, sends questions, applies fallbacks,
and writes output.

## Reproducibility Steps

1. Clone the GitHub repository.
2. Ensure Python3 and the requests package are installed.
3. Place the test JSON file (cse_476_final_project_test_data.json) in the repo directory.
4. Run the script: generate_answer_template.py
5. The output will be written to cse_476_final_project_answers.json.
