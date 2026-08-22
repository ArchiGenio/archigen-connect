# Install ArchiGen Connect 0.1.0-beta.3

1. Download `ArchiGenConnectSetup-0.1.0-beta.3.exe` only from the [0.1.0-beta.3 GitHub Release](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.3).
2. Compare the downloaded file with the SHA-256 checksum published with that release.
3. Run the installer and follow: **Welcome** -> **Install / Repair / Uninstall** -> **System Check** -> **Installation Options** -> **Ready** -> **Install** -> **Launch ArchiGen Connect**.
4. Choose whether to create a desktop shortcut. A Start Menu shortcut is created by default.
5. Launch **ArchiGen Connect**, select your project folder, and follow the Project -> Rhino + Grasshopper -> Copilot workflow.

The installer provisions or repairs the supported Rhino MCP connection and installs the ArchiGen Rhino Bridge automatically. Do not manually copy `.rhp` files, run Yak, or configure the Rhino connector during the normal workflow.

Rhino 8.34 or later is required. Grasshopper is included with Rhino 8. Visual Studio Code and GitHub Copilot are required for the Copilot workflow.

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