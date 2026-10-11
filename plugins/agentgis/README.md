# AgentGIS skills (plugin 2.1.1, bootstrap 2.1.0)

Conversational planning GIS: the agent starts the official AgentGIS local server, opens the workspace at https://agent-gis.7m7s.tech/app, and after you sign in performs imports, CRS checks, TOD / coverage-gap / site-selection analysis and PDF/PNG/GeoJSON exports. GIS data stays in your browser by default.

| Skill | Language |
|---|---|
| `skills/agentgis-bootstrap` | 简体中文 |
| `skills/agentgis-bootstrap-en` | English |

Each folder is complete: `SKILL.md` and `agents/openai.yaml`. The bootstrap pins no release: it reads the official directory `/skills/manifest.json`, verifies the Local Helper against `/helpers/manifest.json`, and after you sign in reads the current full guide from the protected catalog `/skills/catalog.json`. The same folders work in every host and rarely need updating.

## Install

Claude Code: `/plugin install agentgis --marketplace CaPaCaptain/AgentSkills` (or `claude plugin marketplace add CaPaCaptain/AgentSkills` then `claude plugin install agentgis@agentskills`).

Codex: `$skill-installer install https://github.com/CaPaCaptain/AgentSkills/tree/main/plugins/agentgis/skills/agentgis-bootstrap` (English: `agentgis-bootstrap-en`).

## Requirements and limits

- Runs on your own computer: Node.js (^22.12, ^24 or >=26) and a visible browser. Cloud sandboxes and web chat apps cannot run the local server.
- No browser extension needed: the agent opens /app in the host's visible browser if it can reach 127.0.0.1, otherwise in your system default browser.
- A free AgentGIS account. Demo/Beta: accepted end-to-end on WorkBuddy for macOS; Claude Code and Codex are being validated.
- Results are planning-grade, not survey, legal or engineering accuracy.

## Data and network access

The plugin declares one local MCP server, `agentgis`: the official AgentGIS Local Helper 0.3.0 shipped in `helper/` (Node.js, listens on 127.0.0.1 only after `agentgis_start`). The plugin downloads and runs no other program. Its skills and server contact only these services:

| Service | What is sent or received | When |
| --- | --- | --- |
| `https://agent-gis.7m7s.tech` (public) | Reads the directory `/skills/manifest.json` (hosts without the plugin's MCP server also download the Helper from `/helpers/`, SHA-256 verified) | Task start |
| `https://agent-gis.7m7s.tech` (signed in) | Reads the full guide and manuals; the page pairs with the local server; optional feedback you approve (`feedback.submit`) | After you sign in |
| `127.0.0.1:47831` (your computer) | GIS commands, the files you name, exported files | During the task |

Your GIS files are not uploaded to the cloud by default: they move only between your computer's local server and your browser. AgentGIS keeps your account, workspace and pairing records and any feedback you send; see the privacy policy. Claude conversation content is not sent to AgentGIS.

Privacy: https://agent-gis.7m7s.tech/privacy/ · Terms: https://agent-gis.7m7s.tech/terms/ · Contact: contact@7m7s.tech

Generated from the AgentGIS repository by `scripts/export-public-skills.mjs`; do not edit here.
