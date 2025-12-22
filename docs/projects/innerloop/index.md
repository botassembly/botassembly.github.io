---
description: Agent loop SDK for LLM tool-calling. The execute-observe-decide cycle that powers autonomous agents.
---

# innerloop

> Agent loop SDK - the execute-observe-decide cycle

innerloop is a thin Python harness that runs the core agent loop: execute a tool, observe the result, decide what to do next. It handles streaming, tool dispatch, and state management so you can focus on your agent's logic.

## Quick Start

```bash
pip install innerloop
```

```python
from innerloop import AgentLoop

loop = AgentLoop(
    model="claude-sonnet-4-20250514",
    tools=[...],
    system_prompt="You are a helpful assistant."
)

result = loop.run("What's the weather in NYC?")
```

## Features

- **Minimal API** - One class, one method
- **Streaming** - Built-in support for streaming responses
- **Tool dispatch** - Automatic tool execution and result handling
- **State management** - Conversation history and context
- **Extensible** - Hooks for custom behavior

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/innerloop)
- [API Reference](./api.md)
- [Examples](./examples.md)

---

*Documentation is aggregated from the [innerloop repository](https://github.com/botassembly/innerloop). Updates appear nightly.*
