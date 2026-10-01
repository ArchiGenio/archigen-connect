<p align="center"><img src="assets/archigen-logo.png" alt="ArchiGen" width="220"></p>

<h1 align="center">ArchiGen Connect</h1>

<p align="center"><strong>AI Agent Bridge for AEC Workflows</strong></p>
<p align="center"><strong>Any AI. One AEC Connection Layer.</strong></p>
<p align="center">0.1.0-beta.21 | Free Public Beta | Windows 10/11 x64</p>

<p align="center">
  <a href="https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/ArchiGenConnectSetup-0.1.0-beta.21.exe"><strong>Download Beta.21 for Windows</strong></a>
  | <a href="https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.21">Release Notes</a>
  | <a href="https://github.com/ArchiGenio/archigen-connect/issues/new/choose">Report Bug / Request Feature</a>
</p>

<p align="center"><img src="assets/archigen-connect-hero.png" alt="ArchiGen Connect linking AI clients with AEC software"></p>

ArchiGen Connect is a local connection and execution layer for AI-assisted architecture, engineering and computational-design workflows. It lets compatible AI clients work through one shared ArchiGen layer instead of requiring separate software-specific integrations for every assistant.

This repository is the public product, documentation and download home for ArchiGen Connect. Product source is not published here. Installers are distributed through GitHub Releases.

## What changed in Beta.21

Beta.21 expands ArchiGen Connect from a Rhino + Grasshopper bridge into a broader **multi-AI, multi-software AEC connection layer**.

### AI clients

- **ChatGPT** — general AI assistant workflows
- **GitHub Copilot** — coding and agent workflows from VS Code
- **Codex** — OpenAI coding/agent workflows
- **Claude** — MCP-native desktop workflows
- **Ollama** — local AI inference with compatible installed models

### Software targets

| Software target | Beta.21 capability |
| --- | --- |
| **Rhino 8 + Grasshopper** | Parametric modeling, native editable graphs, reusable forms and AI-generated procedural geometry |
| **ComfyUI** | Local node-workflow discovery, validation, editing, execution and output retrieval through MCP |
| **Autodesk Revit 2025** | BIM inspection and controlled model operations through the Revit MCP connection |

<p align="center"><img src="assets/archigen-connect-platform.png" alt="ArchiGen Connect platform overview"></p>

The product model is simple:

**AI Client → ArchiGen Connect → Selected Software Target**

Your project, selected AI client and selected software target remain separate, so you can change one without rebuilding the others.

## ArchiGen Genie — generation modes

The Grasshopper side includes four explicit generation modes. Use the mode prefix when you want deterministic routing, or let Auto decide.

| Genie mode | Command | Best for |
| --- | --- | --- |
| **Auto** | `/auto` | Automatically chooses Form → Creative → Agent according to the request |
| **Form** | `/form` | Reusable ArchiGen parametric systems with exposed native controls |
| **Creative** | `/creative` | One AI-generated procedural geometry program inside an AI Creative Form component |
| **Agent** | `/agent` | Visible native Grasshopper definitions made from standard components, sliders and wires |

### `/form` — ArchiGen Building

The current **ArchiGen Building** system exposes **22 inputs**, including **X/Y/Z positioning**, plus shape, size, levels, rotation, taper, slab/detail settings and facade spacing, with native outputs for:

- Floor Slab
- Handrail
- Mullions
- Glass

The result stays editable and recomputes normally when its parameters change.

### `/creative` — AI Creative Form

Creative executes AI-generated C# / RhinoCommon geometry logic inside **one AI Creative Form component**. It can expose dynamic native inputs and outputs, evolve the same form when the algorithm changes, and recompute parameter edits without regenerating code.

Python execution is deferred in this release.

### `/agent` — native Grasshopper graph

Agent creates or edits visible Grasshopper definitions using standard components and wires. The generated graph remains directly editable by the user.

### `/auto` — intelligent routing

Auto selects the lightest suitable generation strategy instead of forcing every task into one representation.

<p align="center"><img src="assets/archigen-connect-workflow.png" alt="ArchiGen Connect workflow"></p>

## Why ArchiGen Connect

ArchiGen Connect is designed around a shared AEC intelligence layer rather than a collection of one-off AI integrations.

- **One connection layer** for multiple AI clients
- **MCP-first software connectivity** where strong software MCPs already exist
- **Parametric-design intelligence** before execution, not only tool calling
- **Editable results** in Grasshopper instead of black-box geometry where possible
- **Local AI option** through Ollama
- **Project-aware routing** across supported clients and software targets
- **Repair and readiness tools** for supported connections

## Install and connect

1. Download the [Beta.21 installer](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/ArchiGenConnectSetup-0.1.0-beta.21.exe).
2. Run setup and approve the Windows permission prompt.
3. Sign in to ArchiGen Connect and select your project.
4. Choose an AI client.
5. Choose the software target you want to work with.
6. Wait for the selected target to report **READY**.
7. Work naturally from the connected AI client.

See [INSTALL.md](INSTALL.md), [REQUIREMENTS.md](REQUIREMENTS.md), [TROUBLESHOOTING.md](TROUBLESHOOTING.md) and the [ChatGPT MCP setup guide](CHATGPT_SETUP.md).

For updates, save your work and **install the new Beta over the existing installation**. Do not uninstall first. Normal settings and signed-in session state are preserved; sign in again only if the session itself has expired.

## Download and verification

Version: **0.1.0-beta.21**  
Installer: **ArchiGenConnectSetup-0.1.0-beta.21.exe**  
Size: **117608392 bytes**<br>
Installer status: **unsigned Public Beta**

- [Download installer](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/ArchiGenConnectSetup-0.1.0-beta.21.exe)
- [Download SHA256SUMS.txt](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/SHA256SUMS.txt)
- [Release notes](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.21)
- [Changelog](CHANGELOG.md)

SHA-256:

```text
4090732D5D0E522BB523D2FE359EE17AF8E3A3ACA09E880394C343A6434C4F9E
```

## Beta notes

ArchiGen Connect is still a public beta. Client availability, model quality, software versions and third-party MCP behavior may affect individual workflows.

- Claude usage depends on the user's Claude account availability and limits.
- Ollama tool use depends on the capabilities of the selected local model.
- ComfyUI workflows require their referenced local models/custom nodes.
- Revit support in Beta.21 is validated against Revit 2025 through the current compatibility provider.
- Project Memory/private Skills may require additional configured services.

## Feedback

Use [GitHub Issues](https://github.com/ArchiGenio/archigen-connect/issues/new/choose) to report bugs or request features. Include the ArchiGen Connect version and clear reproduction steps, but never share passwords, tokens, API keys, confidential project files or private company information.

Beta.21 features are frozen. Post-release changes are bug fixes only; new features belong to Beta.22 or later.
