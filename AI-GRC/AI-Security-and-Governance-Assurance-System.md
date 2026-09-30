# AI Security and Governance Assurance System
Connects technical security work to business decisions the skill that separates senior candidates
from junior ones, and the one most technically-minded applicants neglect entirely.

## Business Scenario

A fictional organisation, "Northwind Retail," running several AI systems: an employee chatbot, a
customer-support assistant, a coding agent and a decision-support model.


## Architecture

```mermaid
flowchart TB
    Inventory[AI Inventory\nowner, purpose, model,\ndata classification,\nuser population,\nintegrations, risk tier]

    Inventory --> Register[AI Risk Register\nrisk, likelihood, impact, treatment]
    Register --> ControlMap[Control Mapping\nNIST AI RMF / GenAI Profile\nOWASP LLM Top 10\nMITRE ATLAS]
    ControlMap --> Evidence[Evidence Register\nhow each control is tested,\nwhat proof demonstrates it works]
    Evidence --> Dashboard[Executive Dashboard\nmajor risks, control weaknesses,\noverdue actions, decisions\nneeding leadership approval]

    Finding[Red-team Finding\ne.g. from Project 1] -->|logged as| Register
    Register -->|mapped to| ControlMap
    ControlMap -->|tested via| Evidence
    Evidence -->|gap found| Ticket[Remediation Ticket]
    Ticket -->|fixed, verified by| Retest[Retest]
    Retest -->|closes loop back into| Register

    style Finding fill:#3a1414,stroke:#c0392b,color:#fff
    style Retest fill:#14243a,stroke:#2980b9,color:#fff
```

