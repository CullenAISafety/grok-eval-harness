# Grok Evaluation Harness

A lightweight, reproducible framework for evaluating long-horizon behavior in large language models (LLMs).

## What It Evaluates

- Persona drift across multi-turn interactions
- Conversation drift and loss of coherence
- Boundary adherence under instruction pressure
- Long-horizon behavioral failures

## Getting Started

Clone the repository:
```bash
git clone https://github.com/CullenAISafety/grok-eval-harness.git
cd grok-eval-harness
## Model Integration

The harness is model-agnostic and supports pluggable backends.
Grok execution requires authorized xAI API access and is disabled by default.
