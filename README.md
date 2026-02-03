**Grok Evaluation Harness**

A lightweight, reproducible evaluation framework for stress-testing long-horizon behavior, safety boundaries, and instruction reliability in large language models.

Built for AI safety research, red-team testing, and deployment readiness.

This harness focuses on system-level behavior over extended interactions, not single-prompt benchmarks.

**Why this exists**

Many LLM failures only emerge after sustained use:

  -persona/identity drift
  
  -instruction conflicts
  
  -boundary violations
  
  -degraded reasoning across long contexts
  
  -Traditional prompt tests miss these.

This harness makes those failures measurable, repeatable, and comparable across runs.

**What it evaluates**

  -Persona drift — consistency of identity across sessions
  
  -Conversation drift — coherence over multi-turn interactions
  
  -Boundary adherence — compliance with safety and policy constraints
  
  -Long-horizon failures — behaviors that appear only after extended usage
  
  -Behavioral reproducibility — repeatable failure detection

**Features**
Pluggable model backends (Grok + extensible adapters)

  -Structured logging
  
  -Reproducible test suites
  
  -Config-driven evaluation runs
  
  -Failure categorization
  
  -Session-level metrics



**QUICK START**
git clone https://github.com/CullenAISafety/grok-eval-harness.git
cd grok-eval-harness


**INSTAL**
pip install -r requirements.txt

**RUN EXAMPLE**
python run_harness.py --model <MODEL_NAME> --config configs/example.yaml


**EXAMPLE OUTPUT**
Session: 12
Persona Drift Score: 0.42 (⚠ elevated)
Instruction Violations: 3
Boundary Failures: 1
Long-horizon instability detected after turn 37

**ARCHITECTURE**
Test Suites → Harness → Model Backend → Logs → Metrics → Reports

The harness treats models as black-box systems and evaluates observable behavior without requiring internal access.

**Model Integration
Grok**

Requires authorized xAI API access:

export XAI_API_KEY="your_api_key_here"
python run_harness.py --model grok

**Additional Models**

Implement the interface in models/ and provide a configuration file. Backends are automatically detected.

Intended Use

  -Safety evaluation

  -Red teaming

  -Pre-deployment testing

  -Regression checks

  -Behavioral drift monitoring

Author

Cullen E. Mathews

Independent AI Safety & Evaluation Engineer
