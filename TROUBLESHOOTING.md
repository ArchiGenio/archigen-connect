# Troubleshooting Beta.15

## Rhino is not detected

Confirm Rhino 8 is installed and open, then return to ArchiGen Connect and retry the connection or environment check.

## Rhino or Grasshopper does not connect

Close and reopen Rhino, then use the Beta.15 installer and choose **Repair**. Reopen Grasshopper after the repair completes.

## AI client does not connect

Confirm that you are signed in to the selected AI client or host, that the project is selected in ArchiGen Connect, and that Rhino and Grasshopper are running.

## Sign-in or session problems

Sign out and sign in again, then restart ArchiGen Connect. If the problem persists, repeat the installer repair workflow.

## Windows security notice

Confirm that the installer came from the official [Beta.15 GitHub Release](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.15). Windows may require **More info → Run anyway** for this public Beta installer.

## Repair workflow

Run `ArchiGenConnectSetup-0.1.0-beta.15.exe`, select **Repair**, complete setup, and restart the connected applications.

## Reporting a problem

Search [GitHub Issues](https://github.com/ArchiGenio/archigen-connect/issues) first. If needed, [open a bug report](https://github.com/ArchiGenio/archigen-connect/issues/new/choose). Do not upload passwords, tokens, API keys, confidential project files, or private company information.