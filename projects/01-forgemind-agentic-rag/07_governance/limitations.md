# Limitations

## Overview

ForgeMind v1 is a prototype designed to explore the application of multi-agent AI in technician maintenance support.

While it demonstrates key capabilities such as grounded retrieval, structured guidance, and validation, it operates within a defined scope and set of constraints.

Understanding these limitations is essential for interpreting the system’s outputs responsibly and for guiding future improvements.

---

## Scope Limitations

### 1. Limited Knowledge Base

ForgeMind v1 is built on a curated but relatively small set of technical documents.

This means:

- coverage is not comprehensive  
- certain fault scenarios or edge cases may not be represented  
- responses are only as strong as the underlying document corpus  

**Implication:**  
The system may not always retrieve sufficient context for less common or highly specific queries.

---

### 2. No Real-Time Data Integration

The system does not integrate with live enterprise systems such as:

- ERP platforms  
- inventory systems  
- maintenance management systems  

All responses are based on static documents.

**Implication:**  
ForgeMind cannot provide real-time status, availability, or operational data.

---

### 3. No Workflow Execution Capability

ForgeMind v1 focuses on guidance and does not execute actions such as:

- creating work orders  
- ordering parts  
- triggering external systems  

**Implication:**  
The system supports decision-making but does not automate operational workflows.

---

### 4. Stateless Interaction Model

Each interaction is treated independently.

The system does not:

- retain session memory  
- track previous queries  
- maintain context across interactions  

**Implication:**  
Follow-up queries may require restating context.

---

### 5. Limited Personalization

ForgeMind does not currently adapt responses based on:

- technician experience level  
- certifications or role  
- site-specific conditions  

**Implication:**  
All users receive a similar level of detail and guidance.

---

## Technical Limitations

### 1. Retrieval Variability

The quality of responses depends on the effectiveness of retrieval.

Factors include:

- document structure  
- chunking strategy  
- query phrasing  

**Implication:**  
Different prompts may produce different results for similar queries.

---

### 2. Prompt Sensitivity

The system relies on prompt engineering to guide behavior.

Small changes in phrasing can influence:

- response structure  
- level of detail  
- routing decisions  

**Implication:**  
Consistency may vary across inputs.

---

### 3. Partial Grounding Risk

While the system uses retrieval, there may still be cases where:

- responses are only partially grounded  
- the model fills gaps with inferred information  

**Implication:**  
Outputs should be reviewed before use in real-world scenarios.

---

## Safety and Operational Limitations

### 1. Not a Replacement for Official Guidance

ForgeMind is not intended to replace:

- OEM documentation  
- certified maintenance procedures  
- professional technician judgement  

**Implication:**  
All outputs should be validated against official sources before action.

---

### 2. Prototype-Level Safeguards

While safeguards are implemented, they are:

- prompt-based  
- not enforced through formal policy engines  
- not validated in production environments  

**Implication:**  
There is still residual risk in outputs.

---

## Environment Constraints

### 1. Limited Dataset Size

The system operates within practical limits of:

- context window size  
- number of documents ingested  
- compute and tooling constraints  

**Implication:**  
Scaling the system requires changes to data handling and architecture.

---

### 2. Dependency on Tooling

ForgeMind v1 is built using:

- Langflow for orchestration  
- vector-based retrieval  
- external evaluation tooling  

**Implication:**  
Behavior and performance are influenced by the capabilities and limitations of these tools.

---

## Summary

ForgeMind v1 is intentionally designed as a focused prototype to demonstrate:

- multi-agent AI architecture  
- grounded retrieval patterns  
- structured and safety-aware outputs  

Its limitations reflect early-stage design choices and practical constraints rather than shortcomings.

These limitations also define the pathway for future enhancements, including:

- workflow integration  
- context awareness  
- system scalability  
- enterprise-grade safeguards  

Recognizing these boundaries is key to using the system responsibly and evolving it effectively.