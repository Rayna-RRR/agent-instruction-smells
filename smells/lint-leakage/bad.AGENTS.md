# AGENTS.md

## Formatting And Linting

This project uses Ruff. Ruff has many rules. Important examples include:

- `E501`: line too long.
- `F401`: unused import.
- `F841`: unused variable.
- `I001`: import sorting.
- `UP006`: use built-in generics.
- `UP007`: use `X | Y`.
- `B008`: do not call functions in argument defaults.
- `C901`: function is too complex.
- `SIM108`: use ternary operators.
- `RET504`: unnecessary assignment before return.
- `PLR0913`: too many arguments.
- `TRY003`: avoid long exception messages.

Black formats Python code with an 88-character line length. Ruff can also format code. Sometimes Ruff conflicts with Black. Run both. If they disagree, keep running them until the diff stops changing.

The lint config was copied from the platform team. If lint fails, fix all violations in the touched package and nearby packages. Do not leave any warning behind.

## Development

Use Python 3.12.

```bash
python -m pip install -e ".[dev]"
pytest
ruff check .
ruff format .
```

## Code Style Notes

Use clear names. Avoid cleverness. Prefer composition. Avoid globals. Use dataclasses when useful. Avoid dataclasses when the object has behavior. Keep functions short. Avoid too many comments. Add comments when code is complex.
