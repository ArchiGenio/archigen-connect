# Troubleshooting Beta.20

## Installation or Windows security notice

Use only the official [Beta.20 release](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.20) and compare the download against its SHA256SUMS.txt. This Public Beta installer is unsigned, so SmartScreen may appear. Proceed only after verification and where your organization's policy permits it. Installation requires the Windows permission prompt.

## Updating or repairing

Save your work, close ArchiGen Connect and run `ArchiGenConnectSetup-0.1.0-beta.20.exe` over the existing installation. Use Repair if offered. **Do not uninstall first** or manually delete application settings. Reopen ArchiGen Connect after setup, then restart the supported connections.

## Rhino is not detected

Confirm Rhino 8 is installed and can launch normally. Retry the environment check in ArchiGen Connect. Revit is under development and is not needed for Rhino/Grasshopper.

## Rhino or Grasshopper is not ready

Save your work, restart the Rhino/Grasshopper connection from ArchiGen Connect and wait for it to become ready. If Grasshopper is not visible, open it inside Rhino. If the connection still fails, rerun the Beta.20 installer to repair the packaged connection, then restart ArchiGen Connect and Rhino.

## Sign-in or session problems

Confirm your internet connection, then restart ArchiGen Connect. Updates normally preserve the signed-in session. If it has expired, sign in again through the normal account flow. Do not share credentials or delete settings as a first troubleshooting step.

## AI client does not connect

Confirm ArchiGen Connect is signed in, a project is selected and Rhino/Grasshopper is ready. Check your AI client's account and workspace permissions. For ChatGPT, follow [CHATGPT_SETUP.md](CHATGPT_SETUP.md) and rescan the app's tools after reconnecting.

## Creative produces an error or no geometry

The current Creative engine is C# with RhinoCommon; Python execution is deferred. Check component errors, valid control values and whether the declared geometry outputs are present. Retry or simplify the request when generated code fails validation or execution. An empty component or stored code is not a completed design.

Existing control changes recompute geometry without new AI generation. An algorithm change is a Creative evolution request; a visible standard-component graph belongs in Agent mode.

## Optional ComfyUI connection

Check that your local ComfyUI environment is running and that the selected workflow's models and dependencies are available. ComfyUI is optional for Rhino/Grasshopper modeling.

## Reporting a problem

Search [GitHub Issues](https://github.com/ArchiGenio/archigen-connect/issues) first, then [report a bug or request a feature](https://github.com/ArchiGenio/archigen-connect/issues/new/choose). Include Beta.20, reproducible steps and a non-confidential screenshot when useful. Never upload passwords, tokens, API keys, confidential project files or private company information.