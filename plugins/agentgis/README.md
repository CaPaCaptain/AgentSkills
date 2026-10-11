# AgentGIS skills (bootstrap 1.3.1)

Conversational planning GIS: the agent starts the official AgentGIS local server, opens the workspace at https://agent-gis.7m7s.tech/app, and after you sign in performs imports, CRS checks, TOD / coverage-gap / site-selection analysis and PDF/PNG/GeoJSON exports. GIS data stays in your browser by default.

| Skill | Language |
|---|---|
| `skills/agentgis-bootstrap` | 简体中文 |
| `skills/agentgis-bootstrap-en` | English |

Each folder is complete: `SKILL.md`, `agents/openai.yaml` and `references/PINNED-RELEASE.json` (SHA-256 pins for the local helper, the full guide and the manuals; the full guide is read only after you sign in).

## Install

Claude Code: `/plugin install agentgis --marketplace CaPaCaptain/AgentSkills` (or `claude plugin marketplace add CaPaCaptain/AgentSkills` then `claude plugin install agentgis@agentskills`).

Codex: `$skill-installer install https://github.com/CaPaCaptain/AgentSkills/tree/main/plugins/agentgis/skills/agentgis-bootstrap` (English: `agentgis-bootstrap-en`).

## Requirements and limits

- Runs on your own computer: Node.js (^22.12, ^24 or >=26) and a visible browser. Cloud sandboxes and web chat apps cannot run the local server.
- Claude Code: use your own Chrome (for example Claude in Chrome); the desktop app's built-in browser cannot reach 127.0.0.1 from an HTTPS page.
- A free AgentGIS account. Demo/Beta: accepted end-to-end on WorkBuddy for macOS; Claude Code and Codex are being validated.
- Results are planning-grade, not survey, legal or engineering accuracy.

Privacy: https://agent-gis.7m7s.tech/privacy/ · Terms: https://agent-gis.7m7s.tech/terms/ · Contact: contact@7m7s.tech

Generated from the AgentGIS repository by `scripts/export-public-skills.mjs`; do not edit here.
