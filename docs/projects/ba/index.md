---
description: Bot Assembly workflow language. Define multi-step LLM workflows in markdown.
---

# BA (Bot Assembly)

> Workflow language for AI agents

BA (Bot Assembly) is a markdown-based language for defining multi-step LLM workflows. Write `.ba.md` files with opcodes and modifiers, compile to executable workflows.

## Quick Start

```markdown
<!-- hello.ba.md -->
# Hello Workflow

## Steps

Think: What's a good greeting for {{name}}?
Do: Generate a personalized greeting
  - Use the user's name naturally
  - Keep it under 50 words
```

```bash
ba run hello.ba.md --name="Alice"
```

## Opcodes

| Opcode | Description |
|--------|-------------|
| `Think` | LLM reasoning step |
| `Do` | Execute an action |
| `Fetch` | Retrieve external data |
| `Wait` | Pause for condition/time |
| `Fork/Join` | Parallel execution |

## Modifiers

Control flow modifiers attach to opcodes:

- `@retry(3)` - Retry on failure
- `@timeout(30s)` - Set timeout
- `@cache` - Cache results
- `@parallel` - Run in parallel

## Features

- **Markdown-native** - Write workflows in familiar format
- **Composable** - Import and reuse workflow fragments
- **Type-safe** - Schema validation for inputs/outputs
- **Observable** - Built-in logging and tracing

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/ba)
- [Language Reference](./reference.md)
- [Opcode Guide](./opcodes.md)
- [Examples](./examples.md)

---

*Documentation is aggregated from the [ba repository](https://github.com/botassembly/ba). Updates appear nightly.*
