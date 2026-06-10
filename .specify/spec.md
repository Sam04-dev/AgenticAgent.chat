# Specification: AgenticAgent.chat - The Agent Trust Layer

## Project Overview
This specification defines the core behaviors and data contracts for **the Agent Trust Layer**, a verifiable trust and authorization protocol for autonomous AI agents.

## Source of Truth
> [!IMPORTANT]
> This project follows a **Spec-First** methodology. All data contracts and behavior definitions are maintained in YAML files within the `.specify/spec/` directory.

### Current Specs:
- **`.specify/spec/agenticagent-chat.yaml`**: defines the `TaskIntent` entity and the `submit_intent` behavior with its respective guardrails (price, ERC-8004 status, slippage).
- **`.specify/spec/handshake.yaml`**: defines the handshake protocol between the Agent Brain and the Agent Trust Layer.

## Behaviors

### 1. `submit_intent` (from `.specify/spec/agenticagent-chat.yaml`)
- **Inputs**: `TaskIntent`
- **Outputs**: `ValidationArtifact`
- **Constraints**:
    - Agent must have an active ERC-8004 Registry ID.
    - Risk score must be validated via Genkit Flow before signing.
    - Slippage and Price triggers must be within defined bounds.

---

## Active Tasks
Current focus is on initializing the Specify environment and codifying the Project Constitution.

See [.specify/memory/constitution.md](.specify/memory/constitution.md) for architectural guardrails.
