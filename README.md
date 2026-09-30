<p align="center"><img src="assets/archigen-logo.png" alt="ArchiGen" width="220"></p>

<h1 align="center">ArchiGen Connect</h1>

<p align="center"><strong>AI Agent Bridge for AEC Workflows</strong></p>
<p align="center"><strong>Any AI. One AEC Connection Layer.</strong></p>
<p align="center">0.1.0-beta.20 | Free Public Beta | Windows 10/11 x64</p>

<p align="center">
  <a href="https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.20/ArchiGenConnectSetup-0.1.0-beta.20.exe"><strong>Download Beta.20 for Windows</strong></a>
  | <a href="https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.20">Release Notes</a>
  | <a href="https://github.com/ArchiGenio/archigen-connect/issues/new/choose">Report Bug / Request Feature</a>
</p>

<p align="center"><img src="assets/archigen-connect-hero.png" alt="Conceptual illustration of ArchiGen Connect linking AI with AEC workflows"></p>

ArchiGen Connect connects compatible AI assistants to architecture, engineering and computational-design workflows. It is a connection and execution layer, not another foundation model: create, modify, inspect and verify geometry in the design tools you use.

This is the public product, documentation and download repository. Product source is not published here. Installers are distributed as GitHub Release assets, not files in this repository.

## Supported in Beta.20

| Platform | AEC workflow | AI clients |
| --- | --- | --- |
| Windows 10/11 x64 | Rhino 8 and Grasshopper | ChatGPT and GitHub Copilot / local workflow |

Rhino and Grasshopper are the primary supported AEC workflow. Revit integration is under development and is not current production support. Broader AI and AEC integrations remain the platform direction, not a claim that every client or host works today.

ComfyUI is an optional local connection for rendering workflows. It depends on a working ComfyUI environment and the selected workflow's models and dependencies; it is not required for Rhino or Grasshopper.

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

1. Download the [Beta.20 installer](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.20/ArchiGenConnectSetup-0.1.0-beta.20.exe).
2. Run setup and approve the Windows permission prompt.
3. Sign in to ArchiGen Connect and select your project.
4. Start Rhino and Grasshopper from ArchiGen Connect and wait for a ready connection.
5. Connect your supported AI client and begin creating, modifying, inspecting or verifying your work.

See [INSTALL.md](INSTALL.md), [REQUIREMENTS.md](REQUIREMENTS.md), [TROUBLESHOOTING.md](TROUBLESHOOTING.md) and the [ChatGPT MCP setup guide](CHATGPT_SETUP.md).

For updates, save your work and **install the new Beta over the existing installation**. Do not uninstall first. Normal settings and signed-in session state are preserved; sign in again if your session has expired.

## Download and verification

Version: **0.1.0-beta.20**. Installer: **ArchiGenConnectSetup-0.1.0-beta.20.exe**. This is an **unsigned Public Beta** installer.

- [Download installer](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.20/ArchiGenConnectSetup-0.1.0-beta.20.exe)
- [Download SHA256SUMS.txt](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.20/SHA256SUMS.txt)
- [Release notes](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.20)
- [Changelog](CHANGELOG.md)

SHA-256:

```text
23DE6B101F9C54FB6716DED7DF3EF40F9853F04ABF4E63FB886A501C9C16FEBA
```

## Feedback and next releases

Use [GitHub Issues](https://github.com/ArchiGenio/archigen-connect/issues/new/choose) to report bugs or request features. Include the version and steps to reproduce, but never passwords, tokens, API keys, confidential project files or private company information.

Beta.20 features are frozen. Enhancements belong to Beta.21 or later. The longer-term direction is model-neutral AEC connectivity; Revit and additional AI/host integrations remain under development.