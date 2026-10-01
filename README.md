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

<p align="center"><img src="assets/archigen-connect-hero.png" alt="Conceptual illustration of ArchiGen Connect linking AI with AEC workflows"></p>

ArchiGen Connect connects compatible AI assistants to architecture, engineering and computational-design workflows. It is a connection and execution layer, not another foundation model: create, modify, inspect and verify geometry in the design tools you use.

This is the public product, documentation and download repository. Product source is not published here. Installers are distributed as GitHub Release assets, not files in this repository.

## Supported in Beta.21

AI clients: **ChatGPT, GitHub Copilot, Codex, Claude and Ollama**. Claude Desktop supports MCP connectivity; Ollama supports local AI workflows with compatible installed models.

| Software target | Beta workflow |
| --- | --- |
| Rhino 8 + Grasshopper | Parametric modeling, editable forms and native graphs |
| ComfyUI | Local creative workflow control and execution |
| Autodesk Revit 2025 | BIM workflow connectivity through MCP |

Select your project, AI client and software target in ArchiGen Connect. Readiness is reported for the selected target; you do not need to run every supported application.

Each client and target requires its own working environment, access and dependencies. ComfyUI requires the selected workflow's models and dependencies. Revit requires a working Revit 2025 installation. Neither is required for Rhino + Grasshopper. These integrations are beta capabilities, not a claim of production stability or universal model compatibility.

## Four generation modes

| Mode | What it produces |
| --- | --- |
| **Auto** (`/auto`) | Selects a suitable Form workflow first, then Creative, then Agent. |
| **Form** (`/form`) | Uses the supported ArchiGen Building workflow with editable native controls. |
| **Creative** (`/creative`) | Executes AI-generated procedural geometry inside one AI Creative Form component. |
| **Agent** (`/agent`) | Creates or edits a visible, native Grasshopper graph using standard components and wires. |

Explicit mode selection takes precedence over Auto. Choose a reusable building system, one procedural form or a visible editable graph according to the requested result.

## ArchiGen Building

Create an editable building with width, depth, floor height, floor count, rotation and taper controls. Building produces native outputs for slabs, handrails, mullions and glass, rather than a replacement Agent graph.

## AI Creative Form

Creative executes AI-generated C# geometry logic with RhinoCommon inside **one AI Creative Form component**. It exposes editable native controls and separate geometry outputs, supports same-form evolution and retains its controls when saved and reopened.

Changing an existing parameter recomputes geometry without requesting new AI-generated code. Successful execution requires resulting geometry, not merely stored code or an empty component.

Creative execution is constrained by ArchiGen's runtime validation and execution limits. It is not a claim of a perfect security sandbox. **Python execution is deferred**; this release does not ship separate public C# and Python Creative components.

## Native Agent workflows

Agent creates or edits visible native Grasshopper graphs. A rectangle-extrusion workflow, for example, uses width, depth and height sliders, standard components and normal wires. The graph remains editable in Grasshopper.

## Install and connect

1. Download the [Beta.21 installer](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/ArchiGenConnectSetup-0.1.0-beta.21.exe).
2. Run setup and approve the Windows permission prompt.
3. Sign in to ArchiGen Connect and select your project.
4. Select and connect your software target; wait for a ready connection.
5. Connect your supported AI client and begin creating, modifying, inspecting or verifying your work.

See [INSTALL.md](INSTALL.md), [REQUIREMENTS.md](REQUIREMENTS.md), [TROUBLESHOOTING.md](TROUBLESHOOTING.md) and the [ChatGPT MCP setup guide](CHATGPT_SETUP.md).

For updates, save your work and **install the new Beta over the existing installation**. Do not uninstall first. Normal settings and signed-in session state are preserved; sign in again if your session has expired.

## Download and verification

Version: **0.1.0-beta.21**. Installer: **ArchiGenConnectSetup-0.1.0-beta.21.exe**. Size: **117598158 bytes**. This is an **unsigned Public Beta** installer.

- [Download installer](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/ArchiGenConnectSetup-0.1.0-beta.21.exe)
- [Download SHA256SUMS.txt](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/SHA256SUMS.txt)
- [Release notes](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.21)
- [Changelog](CHANGELOG.md)

SHA-256:

```text
4D129CA1503E1A57BF36DD4B3037D19D45A6CB1022CBCA548BAA3F81013C1809
```

## Feedback and next releases

Use [GitHub Issues](https://github.com/ArchiGenio/archigen-connect/issues/new/choose) to report bugs or request features. Include the version and steps to reproduce, but never passwords, tokens, API keys, confidential project files or private company information.

Beta.21 features are frozen. Post-release changes are bug fixes only; new features belong to Beta.22 or later.