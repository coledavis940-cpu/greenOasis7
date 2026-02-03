
# Copilot Instructions for greenOasis7

## Project Overview
This repository is in an early stage. The only present files are:
- `README.md` (references a Node.js structure with `index.js` and `package.json`, but these files do not exist yet)
- `LICENSE`
- `.vscode/settings.json` (Python test config, see below)
- `.vscode/launch.json` (Chrome debug configs)

## Guidance for AI Coding Agents
- **Clarify Project Intent:** Always confirm the intended language, framework, and application domain with the user before generating code or structure. Do not assume Node.js or Python unless explicitly confirmed.
- **File Discovery:** The `README.md` suggests a Node.js structure, but no source or manifest files exist. If creating them, follow standard conventions for the chosen stack.
- **VS Code Workflows:**
	- `.vscode/settings.json` configures Python `unittest` discovery (pattern: `*test.py`). Pytest is disabled. If Python code is added, use `unittest` for tests by default.
	- `.vscode/launch.json` provides Chrome debug/attach configs for web development at `http://localhost:8080`. If implementing a web server, ensure it runs on this port for out-of-the-box debugging.
- **No Build/Test Scripts:** No `package.json`, Makefile, or other build/test scripts are present. If adding them, document any nonstandard commands or workflows here.
- **No External Integrations:** No dependencies, APIs, or integration points are discoverable. Document any new ones as they are introduced.

## Example Questions to Ask the User
- What is the primary goal or application for this repository?
- Which language or framework should be used (Node.js, Python, etc.)?
- Should the project follow the structure suggested in `README.md`?
- Are there any existing design documents or requirements?

## Discoverable Patterns & Key Files
- `README.md`: Aspirational Node.js structure, not yet implemented.
- `.vscode/settings.json`: Python `unittest` config (if Python is used).
- `.vscode/launch.json`: Chrome debug configs for web apps on port 8080.

## Updating Instructions
- Update this file as the project evolves: document new patterns, workflows, and conventions as they are established.
- Reference key files and directories as they are added, and describe any project-specific approaches that differ from common practices.

---
_Update this file as the project evolves and new patterns, workflows, or conventions are established._
