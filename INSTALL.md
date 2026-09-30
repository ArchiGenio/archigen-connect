# Install ArchiGen Connect Beta.20

## 1. Download and verify

Download [ArchiGenConnectSetup-0.1.0-beta.20.exe](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.20/ArchiGenConnectSetup-0.1.0-beta.20.exe) from the official [Beta.20 release](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.20). Check [REQUIREMENTS.md](REQUIREMENTS.md) before starting.

Download [SHA256SUMS.txt](https://github.com/ArchiGenio/archigen-connect/releases/download/v0.1.0-beta.20/SHA256SUMS.txt) from the same release. Verify your download in PowerShell:

```powershell
Get-FileHash "$env:USERPROFILE\Downloads\ArchiGenConnectSetup-0.1.0-beta.20.exe" -Algorithm SHA256
```

Expected SHA-256: `23DE6B101F9C54FB6716DED7DF3EF40F9853F04ABF4E63FB886A501C9C16FEBA`.

## 2. Install

Save your work and close ArchiGen Connect before setup. Run `ArchiGenConnectSetup-0.1.0-beta.20.exe`, approve the Windows UAC permission prompt and follow the installer.

This Public Beta installer is unsigned. Windows may show SmartScreen. Verify the official release URL and checksum before choosing **More info > Run anyway**, where your organization's policy permits it. Do not bypass an organizational security policy.

## 3. Sign in and select a project

Launch ArchiGen Connect, sign in and select the project folder you want to work with.

## 4. Start Rhino and Grasshopper

Confirm Rhino 8 is installed. Use ArchiGen Connect's Rhino/Grasshopper start action to open a standalone Rhino session with Grasshopper. Open Grasshopper in Rhino if its editor is not visible, and wait for ArchiGen Connect to report a ready connection before sending modeling requests.

Rhino and Grasshopper are the primary supported AEC workflow in Beta.20. Revit is under development, not a prerequisite.

## 5. Connect your AI and design

Connect ChatGPT or GitHub Copilot / local workflow, then describe the workflow you want to create, modify, inspect or verify. For ChatGPT, follow [CHATGPT_SETUP.md](CHATGPT_SETUP.md). Client access depends on the selected AI service and its account or workspace policies.

## Updating an existing Beta

**Install Beta.20 over the existing ArchiGen Connect installation. Do not uninstall first.** Save your work, close connected applications when setup requests it and run the same Beta.20 installer. Normal settings, project selection and signed-in session state are preserved. Sign in again if the session has expired.

After setup, reopen ArchiGen Connect, confirm the project and account, then start Rhino/Grasshopper and reconnect your AI client. See [TROUBLESHOOTING.md](TROUBLESHOOTING.md) for help.