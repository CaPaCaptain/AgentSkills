# AgentSkills

Public agent skills published by **7m7s (深圳市七分七秒智能科技有限公司)**. This repository is the single public distribution point for 7m7s skills: Claude Code installs them through the plugin marketplace in this repo, Codex installs the skill folders directly. Each skill's source of truth lives in its own project repository and is exported here; do not edit the copies in this repo by hand.

## Skills

| Plugin | Skills | What it does |
|---|---|---|
| [`agentgis`](plugins/agentgis/) | `agentgis-bootstrap` (简体中文), `agentgis-bootstrap-en` (English) | Planning GIS by conversation in the visible AgentGIS workspace: import data, check CRS, TOD / coverage-gap / site-selection analysis, PDF/PNG/GeoJSON export. Runs on your own computer. |

## Install in Claude Code

```bash
claude plugin marketplace add CaPaCaptain/AgentSkills
claude plugin install agentgis@agentskills
```

Or in one step inside a session: `/plugin install agentgis --marketplace CaPaCaptain/AgentSkills`. Update later with `claude plugin update agentgis@agentskills`.

## Install in Codex

Ask Codex to install the skill folder from GitHub:

```text
$skill-installer install https://github.com/CaPaCaptain/AgentSkills/tree/main/plugins/agentgis/skills/agentgis-bootstrap
```

(English: use `.../skills/agentgis-bootstrap-en`.) Or copy the folder into `~/.agents/skills/` and restart Codex.

## Requirements

AgentGIS skills drive a local server and a visible browser on **your own computer**. They do not work in cloud sandboxes or web chat apps. See each plugin's README for host-specific notes, privacy and terms.

Contact: contact@7m7s.tech

## License

[CC BY-ND 4.0](LICENSE): you may redistribute the skills unchanged with attribution; modified versions may not be distributed.
