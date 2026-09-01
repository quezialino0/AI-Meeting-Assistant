# AI Meeting Assistant

> Automated meeting minutes generation using n8n, a local LLM, and automated PDF delivery by email.

## Overview

AI Meeting Assistant is an automation workflow built with **n8n** that transforms a meeting transcript into a structured and professional meeting minutes document.

The workflow receives a transcript file, extracts its text, uses a local **Qwen LLM through Ollama** to analyze the meeting, structures the extracted information, generates an HTML document, converts it to PDF, and automatically sends the final document by email.

The goal is to automate the repetitive work involved in creating meeting minutes while keeping the information structured and easy to review.

---

## Problem

Creating meeting minutes manually after a meeting can be time-consuming.

Important information such as:

- decisions;
- assigned tasks;
- responsible people;
- deadlines;
- pending issues;
- participants;

can easily be missed or require additional manual organization.

The goal of this project is to automate this process from the meeting transcript to the final document.

---

## Solution

The workflow follows this process:

**Meeting Transcript → AI Analysis → Structured Data → HTML → PDF → Email**

The LLM analyzes the transcript and extracts:

- Participants
- Summary
- Decisions
- Tasks
- Responsible people
- Deadlines
- Pending issues

The structured information is then used to generate a professional meeting minutes document.

---

## Workflow

```text
Receive Meeting File
        ↓
Extract Transcript
        ↓
Analyze Meeting
   ├── Ollama — Qwen Model
   └── Structured Meeting Output
        ↓
Generate Meeting Minutes HTML
        ↓
Create HTML File
        ↓
Convert HTML to PDF
        ↓
Prepare PDF File
        ↓
Send Meeting Minutes by Email