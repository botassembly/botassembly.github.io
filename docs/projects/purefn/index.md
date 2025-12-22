---
description: Deterministic functional state for games. Pure functions and immutable state for logic that can be replayed and tested.
---

# PureFN

> Deterministic functional state for games

PureFN provides patterns for game logic that can be replayed, tested, and reasoned about. Pure functions + immutable state = predictable behavior.

## Quick Start

```python
from purefn import GameState, Action

@pure
def apply_action(state: GameState, action: Action) -> GameState:
    """Pure function - same inputs always produce same outputs."""
    match action:
        case Move(direction):
            return state.move_player(direction)
        case Attack(target):
            return state.apply_damage(target)
    return state

# Replay any sequence of actions
final_state = reduce(apply_action, actions, initial_state)
```

## Features

- **Pure functions** - No side effects, fully testable
- **Immutable state** - State changes return new state
- **Replayable** - Reproduce any game state from actions
- **Deterministic** - Same inputs = same outputs, always

## Use Cases

- **Game development** - Predictable game logic
- **Simulations** - Reproducible experiments
- **Testing** - Easy to test without mocks
- **Time travel** - Undo/redo, replay, debugging

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/purefn)
- [Patterns Guide](./patterns.md)
- [Examples](./examples.md)

---

*Documentation is aggregated from the [purefn repository](https://github.com/botassembly/purefn). Updates appear nightly.*
