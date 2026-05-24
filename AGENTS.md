# AGENTS.md

## Cursor Cloud specific instructions

This is a **content/documentation repository** — it contains Anthropic's skill definitions for Claude. There are no services to run, no build system, and no web application.

### Repository structure

- `skills/` — 18 skill folders, each with a `SKILL.md` and optional helper scripts/resources
- `template/` — Starter template for new skills
- `spec/` — The Agent Skills specification reference

### Lint / Validate

Run the skill validator on any skill directory:

```bash
python3 skills/skill-creator/scripts/quick_validate.py skills/<skill-name>
```

To validate all skills at once:

```bash
for d in skills/*/; do python3 skills/skill-creator/scripts/quick_validate.py "$d" || echo "FAIL: $d"; done
```

### Python dependencies

Two `requirements.txt` files exist for specific skills:

- `skills/slack-gif-creator/requirements.txt` — pillow, imageio, imageio-ffmpeg, numpy
- `skills/mcp-builder/scripts/requirements.txt` — anthropic, mcp

The validator (`quick_validate.py`) only requires `pyyaml`.

### Key scripts

| Script | Purpose |
|--------|---------|
| `skills/skill-creator/scripts/quick_validate.py` | Validates SKILL.md frontmatter and naming conventions |
| `skills/webapp-testing/scripts/with_server.py` | Utility to start server(s), wait for readiness, run a command |
| `skills/skill-creator/scripts/run_eval.py` | Skill evaluation runner |
| `skills/skill-creator/scripts/package_skill.py` | Packages a skill for distribution |

### Notes

- No CI/CD pipeline exists in this repo.
- No linter (flake8/ruff/eslint) is configured — `quick_validate.py` is the primary validation tool.
- The `mcp` Python package does not expose `__version__`; import it without version checks.
