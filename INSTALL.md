# Install ArchiGen Connect Beta.21

## 1. Download and verify

Download [ArchiGenConnectSetup-0.1.0-beta.21.exe](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/ArchiGenConnectSetup-0.1.0-beta.21.exe) from the official [Beta.21 release](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.21). Check [REQUIREMENTS.md](REQUIREMENTS.md) before starting.

Download [SHA256SUMS.txt](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.21/SHA256SUMS.txt) from the same release. Verify your download in PowerShell:

```powershell
Get-FileHash "$env:USERPROFILE\Downloads\ArchiGenConnectSetup-0.1.0-beta.21.exe" -Algorithm SHA256
```

Expected SHA-256: `4090732D5D0E522BB523D2FE359EE17AF8E3A3ACA09E880394C343A6434C4F9E`. Expected size: **117608392 bytes**.

## 2. Install

Save your work and close ArchiGen Connect before setup. Run `ArchiGenConnectSetup-0.1.0-beta.21.exe`, approve the Windows UAC permission prompt and follow the installer.

This Public Beta installer is unsigned. Windows may show SmartScreen. Verify the official release URL and checksum before choosing **More info > Run anyway**, where your organization's policy permits it. Do not bypass an organizational security policy.

## 3. Sign in and select a project

Launch ArchiGen Connect, sign in and select the project folder you want to work with.

## 4. Select and connect your software target

Choose Rhino + Grasshopper, ComfyUI or Autodesk Revit. Only the selected target needs to be ready before sending requests.

For Rhino + Grasshopper, confirm Rhino 8 is installed and use ArchiGen Connect's start action. Open Grasshopper in Rhino if its editor is not visible. For ComfyUI, select a working local environment with the required workflow models. For Revit, use a working Revit 2025 installation and the offered connection/repair flow. These applications are separate prerequisites, not included host licenses.

## 5. Connect your AI and design

Select ChatGPT, GitHub Copilot, Codex, Claude or Ollama, then describe the workflow you want to create, modify, inspect or verify. Claude uses the supported Desktop MCP connection; Ollama requires a local installation and a compatible model. For ChatGPT, follow [CHATGPT_SETUP.md](CHATGPT_SETUP.md). Client access depends on the selected service and its account or workspace policies.

## Updating an existing Beta

**Install Beta.21 over the existing ArchiGen Connect installation. Do not uninstall first.** Save your work, close connected applications when setup requests it and run the same Beta.21 installer. Normal settings, project selection and signed-in session state are preserved. Sign in again if the session has expired.

After setup, launch ArchiGen Connect from the installer finish page or Start Menu, confirm Beta.21 and your project/account, then reconnect the selected software target and AI client. See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for help.