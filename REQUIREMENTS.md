# Requirements for Beta.21

## Supported platform

- Windows 10/11 x64

Administrator permission is needed for installation. Internet access is needed to download the installer, sign in and use online AI services. Setup checks the local environment and provides repair support for packaged prerequisites.

## Supported software targets

- Rhino 8
- Grasshopper (included with Rhino)
- ComfyUI (working local environment, workflow models and dependencies)
- Autodesk Revit 2025 (working installation and valid host access)

Rhino must be installed and available on this computer. Grasshopper must be able to open in Rhino; it is not a separate ArchiGen application. Use a valid Rhino license or trial as required by McNeel.

Only your selected target is required. ComfyUI and Revit are not prerequisites for Rhino + Grasshopper. Host applications, models and host licenses are not supplied by ArchiGen Connect.

## Supported AI clients and hosts

- ChatGPT
- GitHub Copilot
- Codex
- Claude (supported Claude Desktop MCP connection)
- Ollama (local installation and compatible downloaded model)

An ArchiGen Connect account and a signed-in session are required. Your AI client needs its own supported account, access and configuration. ChatGPT's MCP app flow additionally requires compatible Developer Mode access and a separately configured secure HTTPS connection; see [CHATGPT_SETUP.md](CHATGPT_SETUP.md).

## Optional ComfyUI connection

ComfyUI is optional for rendering workflows. A working local ComfyUI environment and the chosen workflow's models and dependencies are needed for that connection. It is not required for Rhino/Grasshopper modeling.

## Normal installation

You do not need to install a development toolchain or build ArchiGen Connect from source. Follow [INSTALL.md](INSTALL.md) and use the official packaged Windows installer.

## Current limits

This is a beta/pre-release. Host and client compatibility depends on the installed versions, access policies, models and workflows; production stability and universal model compatibility are not claimed. AutoCAD, Blender and Gemini are not supported targets/clients in Beta.21.

AI Creative Form uses C# and RhinoCommon. Python execution is deferred. Creative execution is constrained by ArchiGen's runtime validation and execution limits, not an operating-system security sandbox.