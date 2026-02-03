# Copilot Instructions for greenOasis7

## Project Overview
This repository currently contains only a `README.md` and `LICENSE` file. No source code, configuration, or manifest files are present in the root directory. The project structure and purpose are not yet defined.

## Guidance for AI Coding Agents
- **Project Initialization:** If you are tasked with bootstrapping this project, clarify the intended language, framework, and application domain with the user before proceeding.
- **File Discovery:** No `index.js`, `package.json`, or other code files are present. If referenced in documentation, these files may be aspirational or planned but not yet created.
- **Conventions:** No project-specific conventions, build workflows, or integration patterns are currently discoverable.
- **Next Steps:** Recommend confirming project requirements and intended architecture with the user before generating code or structure.

## Example Questions to Ask the User
- What is the primary goal or application for this repository?
- Which language or framework should be used?
- Are there any existing design documents or requirements?

---
_This file should be updated as the project evolves and new patterns, workflows, or conventions are established._
# Copilot Instructions — theCatSaidNo

## Project Overview
This is a small Flask-based web application. The entry point is `app.py`, which defines the Flask app, routes, and static asset handling. The project follows a classic Flask layout with `templates/` and `static/` directories.

Primary goals appear to be simplicity and browser-based development (github.dev / vscode.dev compatible).

## Architecture & Structure
- `app.py`: Main Flask application and routing logic.
- `templates/`: Jinja2 HTML templates rendered via `render_template`.
- `static/`: Static assets (favicon, CSS, JS, images).
- `assets/`: Non-standard Flask folder; appears to store project resources not directly served.
- `app_test.py`: Test file (likely pytest or unittest-based).
- `requirements.txt`: Python dependencies (Flask expected).
- `.deployment/`: Deployment-related files (do not modify without intent).
- `hello.c`: Unrelated C example file; not part of Flask runtime.

Copilot should **not assume a multi-module Flask factory pattern** — this is a single-file Flask app.

## Runtime & Environment
- Python version observed: **Python 3.8.x**
- Flask is imported directly (`from flask import Flask, render_template, send_from_directory`)
- App instance is created inline: `app = Flask(__name__)`

Do not introduce features requiring newer Python versions unless explicitly requested.

## Routing & Patterns
- Routes are declared via `@app.route`.
- Static files are served explicitly for `/favicon.ico` using `send_from_directory`.
- Platform detection via `sys.platform` is used in `home()` — preserve this pattern if extending OS-specific behavior.

Example pattern to follow:
```python
@app.route("/")
def home():
    myPlatform = sys.platform
    return render_template("index.html", platform=myPlatform)
