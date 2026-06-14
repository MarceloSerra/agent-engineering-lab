# Getting Started with Agents Engineering

## Prerequisites

- Python 3.10+ installed and configured
- Basic understanding of LLM APIs (OpenAI, Anthropic, or local models)
- Familiarity with async/await patterns in Python
- Access to at least one LLM provider (API key or local inference setup)

## Quick Setup

```bash
# Clone the repository
git clone https://github.com/MarceloSerra/agent-engineering-lab.git
cd agent-engineering-lab

# Create virtual environment
python -m venv .venv
source .venv/bin/activate

# Install dependencies (add your own requirements.txt)
pip install openai langchain anthropic
```

## Your First Agent

Start with the [Tool Calling](../tool-calling/README.md) section to understand how LLMs interact with external functions. Then move to [Agents](../agents/README.md) for building autonomous systems.

## Recommended Learning Order

1. **Week 1-2:** Tool Calling fundamentals — function calling, structured output
2. **Week 3-4:** MCP basics — filesystem server, custom tool creation
3. **Week 5-6:** Agent architectures — reactive, planning, reasoning patterns
4. **Week 7-8:** Memory systems — short-term context, long-term persistence
5. **Week 9+:** Multi-agent orchestration and production concerns

## Next Steps

After setup, explore:
- [Learning Path](learning-path.md) — Detailed progression guide
- [Examples](../examples/) — Code samples for each concept
- [Projects](../projects/) — Complete application templates
