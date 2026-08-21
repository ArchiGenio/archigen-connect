# Install ArchiGen Connect 0.1.0-beta.2

1. Download `ArchiGenConnectSetup-0.1.0-beta.2.exe` only from the [0.1.0-beta.2 GitHub Release](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.2).
2. Compare the downloaded file with the SHA-256 checksum published with that release.
3. Run the installer and review its graphical prerequisite page.
4. Choose whether to create a desktop shortcut. A Start Menu shortcut is created by default.
5. Launch **ArchiGen Connect** from the Start Menu after installation.
6. Select your project folder when prompted.
7. Connect or repair Rhino MCP if the application requests it.
8. Open Rhino and Grasshopper.
9. Open the supported AI client workflow, such as the Copilot-compatible workflow.

The installer registers ArchiGen Connect in Windows Installed Apps. Uninstall it from Windows Settings or the Start Menu uninstall entry. Reinstalling uses the same Program Files location and does not replace user project data. Keep Rhino and Revit closed while setup performs installation or repair actions. Missing optional applications do not prevent installation; consult [Requirements](REQUIREMENTS.md).

## SmartScreen notice

ArchiGen Connect `0.1.0-beta.2` is an early Beta and is not yet digitally signed with a production publisher certificate. Windows Defender SmartScreen may show **Windows protected your PC**.

For Beta testers only:

1. Download only from the official ArchiGen Connect GitHub repository/release.
2. Verify the published SHA-256 if desired.
3. On the SmartScreen window select **More info**.
4. Verify the filename is the official ArchiGen Connect installer.
5. Select **Run anyway**.

Never disable Microsoft Defender or SmartScreen globally.

For problems during Beta setup, see [Troubleshooting](TROUBLESHOOTING.md).