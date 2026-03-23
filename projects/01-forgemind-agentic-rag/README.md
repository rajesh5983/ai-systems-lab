# ForgeMind v1 — Agentic RAG for Technician Maintenance Support

## Overview

ForgeMind is a multi-agent AI prototype designed to support maintenance technicians with grounded, context-aware guidance from technical manuals and maintenance documentation.

The project explores how an agentic Retrieval-Augmented Generation (RAG) system can move beyond simple question answering to provide structured troubleshooting support, maintenance checklists, and safety-aware validation.

This portfolio project was developed as the foundation for a broader AI roadmap, where future versions of ForgeMind evolve from knowledge assistance into workflow-aware and enterprise-ready operational support.

---

## Why this project matters

Field technicians often work in environments where speed, accuracy, and safety all matter at the same time. The challenge is not just finding information, but finding the right information quickly across manuals, fault references, and maintenance instructions.

Traditional document search is slow and fragmented. ForgeMind addresses this by combining retrieval, orchestration, and validation through a multi-agent design.

The goal is to demonstrate how AI can support technicians with:

- faster access to relevant maintenance knowledge
- structured troubleshooting guidance
- safety-aware output validation
- a scalable foundation for future workflow automation

---

## Problem statement

Technicians supporting heavy equipment and machinery often rely on large technical manuals, dispersed reference material, and manual troubleshooting processes. In high-pressure maintenance scenarios, this creates friction in locating the right guidance at the right time.

ForgeMind was designed to explore a practical question:

**How can a multi-agent AI system help technicians retrieve grounded maintenance knowledge and convert it into actionable, safety-conscious support?**

---

## Solution summary

ForgeMind v1 uses a supervisor-led multi-agent architecture built in Langflow.

The system currently focuses on three core capabilities:

- retrieving relevant content from an indexed manual corpus
- generating maintenance and troubleshooting guidance
- validating outputs for safety and response quality

This makes ForgeMind v1 a strong base layer for future upgrades such as parts ordering, work order simulation, technician context awareness, and workflow automation.

---

## Core architecture

ForgeMind v1 is structured around four main agents:

### 1. Supervisor Agent
Acts as the central orchestrator. It interprets the user request and routes tasks to the relevant agents.

### 2. Retrieval Agent
Fetches relevant content from the indexed manual and document corpus to ground the response.

### 3. Maintenance Agent
Transforms retrieved information into structured troubleshooting steps, maintenance actions, or checklists.

### 4. Validation Agent
Applies a validation layer to improve response quality and reinforce safety-aware output framing.

---

## Current v1 capabilities

- multi-agent orchestration using a supervisor pattern
- manual and fault-related knowledge retrieval
- troubleshooting and maintenance checklist generation
- prompt-based safeguard and validation logic
- Langflow-based implementation with JSON flow artefacts
- observability and evaluation support through LangWatch

---

## Example use case

A technician is preparing to inspect a CAT engine after a low oil pressure fault.

ForgeMind can support this by helping produce:

- relevant fault-related guidance
- troubleshooting checklist
- maintenance actions
- safety-oriented validation before action

---

## Repository structure

```text
01-forgemind-agentic-rag/
├── README.md
├── archive/
├── 01_overview/
├── 02_architecture/
├── 03_agents/
├── 04_prompts/
├── 05_data/
├── 06_evaluation/
├── 07_governance/
├── 08_demos/
└── assets/

## Langflow artefacts as code

The core implementation of ForgeMind v1 is built in Langflow. For this reason, the exported JSON flow files are treated as the primary code artefacts for the project.

These JSON files capture the logic and structure of the system and can be imported into Langflow for review, extension, or reuse.

---

## Data and knowledge base

ForgeMind v1 currently uses a curated set of technical documents and PDF-based maintenance references as its knowledge base.

The project intentionally began with a smaller document set to:

- keep the prototype focused
- reduce retrieval noise
- improve grounding reliability during early experimentation
- fit within practical context and tooling limits

---

## Safeguards and design considerations

ForgeMind includes early-stage safeguards to reduce the risk of misleading or unsafe outputs.

These include:

- grounding responses on retrieved context
- validation before final response generation
- explicit handling for unsupported or out-of-scope queries
- safety-aware response framing

This project does not replace official maintenance procedures, OEM documentation, or qualified technician judgement.

---

## Current limitations

ForgeMind v1 is a prototype and should be understood within that context.

Current limitations include:

- small document corpus
- no live integration with ERP, inventory, or order tracking systems
- no persistent memory across sessions
- limited personalization by technician role or skill level
- workflow automation is not yet implemented in v1

These limitations are intentional and create the design space for future versions.

---

## Roadmap

### ForgeMind v1  
Multi-agent RAG assistant focused on grounded maintenance support  

### ForgeMind v2  
Workflow-aware AI with simulated actions such as work order creation, parts request generation, webhook-based triggers, and notification flows  

### ForgeMind v3  
Context-aware and enterprise-ready system with technician context, memory, optimization logic, and broader operational orchestration  

---

## Showcase intent

This repository is structured as a portfolio project to demonstrate:

- applied AI system design
- multi-agent orchestration thinking
- retrieval and grounding patterns
- responsible AI considerations
- product and architecture maturity beyond a basic chatbot

---

## Author

**Rajesh Prasannakumar**  
Data and AI practitioner.

This project reflects a focus on designing AI systems that bridge technical capability with real-world operational value.