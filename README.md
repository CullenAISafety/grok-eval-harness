**Grok Evaluation Harness
**


A lightweight, reproducible framework for testing long-horizon behavior and safety in large language models (LLMs).

Designed for AI safety researchers, model developers, and red teams, this harness detects behavior drift, persona inconsistency, and boundary violations in multi-turn interactions.


**
What It Evaluates**

Persona drift: Tracks whether the model maintains a consistent persona across extended conversations.

Conversation drift: Measures coherence and relevance over multi-turn interactions.

Boundary adherence: Ensures the model follows safety and instruction constraints, even under adversarial prompts.

Long-horizon failures: Identifies unexpected behaviors that emerge only after extended use, critical for deployment safety.

**Getting Started**

Clone the Repository
git clone https://github.com/CullenAISafety/grok-eval-harness.git
cd grok-eval-harness

Install Dependencies
pip install -r requirements.txt

Run Example Evaluation
python run_harness.py --model <MODEL_NAME> --config configs/example.yaml

Model Integration

The harness supports pluggable backends for multiple LLMs.

Grok

Grok execution requires authorized xAI API access. Set your API key as an environment variable:

export XAI_API_KEY="your_api_key_here"


Enable Grok evaluation:

python run_harness.py --model grok

Other Models

To integrate additional models, implement the interface in models/ and provide the required configuration file. The harness will automatically detect supported backends.



