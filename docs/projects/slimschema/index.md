---
description: YAML-based schema system for defining data shapes used across BotAssembly workflows.
---

# slimschema

> YAML schema system for data shapes

slimschema is a lightweight schema system for defining data structures. It validates inputs/outputs, generates TypeScript types, and supports constraints. Used across BotAssembly for consistent data handling.

## Quick Start

```yaml
# user.schema.yml
type: object
properties:
  id:
    type: string
    format: uuid
  name:
    type: string
    minLength: 1
  email:
    type: string
    format: email
required: [id, name, email]
```

```python
from slimschema import validate

schema = load_schema("user.schema.yml")
validate(schema, {"id": "123", "name": "Alice", "email": "alice@example.com"})
```

## Features

- **YAML-based** - Human-readable schema definitions
- **Validation** - Runtime validation of data
- **Type generation** - Generate TypeScript types from schemas
- **Constraints** - Min/max, patterns, formats
- **Composable** - Reference other schemas

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/slimschema)
- [Schema Syntax](./syntax.md)
- [Type Generation](./codegen.md)

---

*Documentation is aggregated from the [slimschema repository](https://github.com/botassembly/slimschema). Updates appear nightly.*
