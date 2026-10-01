# Changelog

## v0.1.0-beta.21 - Public Beta

- Added Codex client activation, Claude Desktop MCP connectivity and Ollama local AI integration.
- Added ComfyUI MCP workflow integration and Revit 2025 MCP integration.
- Unified AI-client to ArchiGen to software-target routing, with readiness and context reporting for the selected target.
- Improved launch, attach and repair flows across supported connections.
- Restored the latest ArchiGen Building with 22 inputs, including X/Y/Z positioning controls, and an improved editable component layout.
- Corrected Grasshopper icon sizing to 24x24 while retaining native Building geometry outputs.
- Retained all four generation modes: `/auto`, `/form`, `/creative` and `/agent`.
- Fixed installed desktop startup so packaged runtime connections resolve correctly after installation.
- Preserved signed-in sessions during install-over updates; improved installer and desktop launch stability.

This is a beta/pre-release, not a claim of production stability. Beta.21 features are frozen; post-release changes are bug fixes only. New features belong to Beta.22 or later.

## 0.1.0-beta.20 - Public Beta

- Improved install-over updates and signed-in session continuity.
- More consistent standalone Rhino 8 and Grasshopper startup and connection readiness.
- Four generation modes: Auto, Form, Creative and Agent, with explicit mode selection.
- Editable ArchiGen Building workflows with floor, rotation, taper and facade outputs.
- AI Creative Form executes generated C# geometry with RhinoCommon inside one component, with editable controls, separate outputs, same-form evolution and save/reopen support. Python remains deferred.
- Existing Creative parameter changes recompute geometry without new AI-generated code.
- Native Agent workflows remain visible, editable standard Grasshopper components, sliders and wires.
- Verified Windows installer and downloadable SHA-256 checksum through GitHub Releases.

Beta.20 features are frozen. Enhancements are reserved for Beta.21 or later. Revit remains under development, not current production support.

## 0.1.0-beta.18

- Fixed stale Windows shortcuts that could launch an older ArchiGen Connect build after upgrade.
- Added the installed product version to the desktop UI and installer.
- Improved Rhino MCP connector startup and readiness detection.
- Fixed an installer finish-page error.
- Preserved existing ChatGPT, GitHub Copilot, Rhino, and Grasshopper workflows.

## 0.1.0-beta.15

- Public Beta baseline for ChatGPT and GitHub Copilot / local workflows.
- Rhino and Grasshopper connection for structured AEC execution.
- Create, modify, inspect, and verify workflows for parametric design.
- Safer selective modification and bounded cleanup that preserves unrelated work.
- Improved connection reliability and a public release experience for feedback.

## 0.1.0-beta.4

- Refined the desktop WebView experience.
- Added Account, Sign In and Sign Up surfaces with website access.
- Restored the Project, Rhino and Copilot bottom action bar.
- Fixed document styling so the installed page does not expose raw CSS text.
- Preserved the existing Rhino, Grasshopper and Copilot workflow behavior.

## 0.1.0-beta.3

- New Windows installer.
- Environment checks before setup.
- Improved Rhino + Grasshopper connection.
- Project and Copilot onboarding.
- Improved connected states.
- Improved AI-assisted parametric workflow.

## 0.1.0-beta.2

- Improved Windows installation flow.
- Added environment checks for supported design applications.
- Improved Rhino and Copilot workflow guidance.

## 0.1.0-beta.1

- Initial public ArchiGen Connect Beta
- Windows installer
- Rhino and Grasshopper connectivity
- Project selection
- Copilot-compatible workflow integration
- Parametric workflow intelligence
- Local project-aware workflow foundation

This is a Beta release. Workflows, host compatibility, and setup behavior may change as feedback is incorporated.