# Test Cases

## Overview

This section outlines the evaluation approach used to test ForgeMind v1 across different types of technician queries.

The goal is to assess how well the system performs in terms of:

- relevance of retrieved information  
- quality of generated guidance  
- structure and clarity of responses  
- safety awareness and validation  
- handling of edge cases and unsupported queries  

---

## Evaluation Approach

ForgeMind v1 is evaluated using a set of representative test prompts that simulate real-world technician scenarios.

Each test case is assessed based on:

- **Relevance** — how well the response aligns with the query  
- **Grounding** — whether the response reflects retrieved source content  
- **Structure** — clarity and organization of the output  
- **Safety** — inclusion of safety considerations where applicable  
- **Completeness** — coverage of the requested information  

---

## Test Case Table

| Test ID | Scenario | Prompt | Expected Behavior | Observations | Risk Type |
|--------|--------|--------|------------------|--------------|----------|
| TC-01 | Fault diagnosis | Provide troubleshooting steps for low oil pressure in a CAT engine | Structured checklist with causes and actions | Response structured well with clear steps | Low |
| TC-02 | Maintenance guidance | Provide maintenance steps and safety considerations for low oil pressure | Includes steps + safety validation | Safety section included and well framed | Low |
| TC-03 | Combined query | Provide fault context, troubleshooting, and safety validation | Multi-section structured response | Good orchestration across agents | Medium |
| TC-04 | Out-of-scope query | Provide repair steps for unrelated equipment not in corpus | System should acknowledge limitation | Partial response with limited grounding | High |
| TC-05 | Ambiguous query | Engine issue with unclear description | System should request clarification or general guidance | Generic response produced | Medium |
| TC-06 | Safety-critical scenario | Provide steps involving potential hazards | Safety validation must be strong | Safety section present but can be improved | Medium |
| TC-07 | Rephrased prompt | Same query with different wording | Consistent response expected | Slight variation in structure observed | Low |

---

## Key Observations

### 1. Strong Performance in Structured Scenarios
The system performs well when:

- queries are clearly defined  
- relevant content exists in the knowledge base  

Outputs are:

- structured  
- actionable  
- aligned with expectations  

---

### 2. Dependence on Retrieval Quality

The quality of responses is closely tied to:

- document coverage  
- retrieval accuracy  
- chunking strategy  

Gaps in retrieval can lead to incomplete or partially grounded outputs.

---

### 3. Variability with Prompt Phrasing

Different phrasing of similar queries can lead to:

- variation in structure  
- differences in level of detail  

This highlights sensitivity to prompt design.

---

### 4. Safety Layer Adds Value

The Validation Agent consistently improves:

- response completeness  
- safety awareness  

However, there is scope to strengthen safety handling in more complex scenarios.

---

### 5. Challenges with Out-of-Scope Queries

When queries fall outside the knowledge base:

- the system may still attempt a response  
- grounding may be weak  

This reinforces the need for stronger out-of-scope detection.

---

## Alignment with Observability (LangWatch)

Evaluation results can be further supported using LangWatch by tracking:

- response relevance scores  
- grounding scores  
- trace-level agent behavior  
- latency and performance metrics  

This enables a more systematic and data-driven evaluation approach.

---

## Opportunities for Improvement

Based on testing, future enhancements may include:

- improved retrieval tuning and document expansion  
- stronger out-of-scope detection mechanisms  
- response consistency improvements  
- confidence scoring for outputs  
- enhanced safety validation logic  

---

## Summary

The test cases demonstrate that ForgeMind v1:

- performs well for structured, in-scope queries  
- benefits significantly from grounded retrieval  
- produces clear and actionable outputs  
- still requires improvements in edge-case handling and consistency  

This evaluation provides a baseline for measuring improvements in future versions of the system.