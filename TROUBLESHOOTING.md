# Troubleshooting

## Windows SmartScreen

This Beta may display SmartScreen because the installer is not yet Authenticode-signed. If you intentionally downloaded it from the official ArchiGen GitHub release, choose **More info -> Run anyway**. Do not disable Defender.

## Rhino is not detected

Use the installer **System Check** page and select **Recheck**. Confirm that Rhino 8.34 or later is installed.

## Rhino MCP is not ready

Use **Repair** from the ArchiGen Connect installer, then restart Rhino. Keep Rhino closed while repair is running. Do not manually edit package files.

## Visual Studio Code is not detected

Install Visual Studio Code from its official website, restart ArchiGen Connect, and run the system check again. Visual Studio Code is only needed for the Copilot-compatible workflow.

## Copilot does not open

Confirm that Visual Studio Code is installed and that the Copilot workflow is available to your account. Restart Visual Studio Code and ArchiGen Connect, then try again.

## Grasshopper is not connected

Retry the Rhino connection from ArchiGen Connect. Open Rhino 8 and Grasshopper after setup completes.

## Restarting ArchiGen Connect

Close ArchiGen Connect normally, leave Rhino and Revit closed, and launch ArchiGen Connect again. Re-run System Check / Preparation if requested.

## Reporting a bug

Search [GitHub Issues](https://github.com/ArchiGenio/archigen-connect/issues) first. If the issue is not already reported, use the Bug Report template. Do not upload passwords, tokens, API keys, confidential project files, or private company information.