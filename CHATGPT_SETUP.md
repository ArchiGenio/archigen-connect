# Connect ArchiGen Connect to ChatGPT

This guide documents the Beta.20 Developer Mode path for connecting ChatGPT to a signed-in local ArchiGen Connect session through MCP.

**MCP** means **Model Context Protocol**.

ChatGPT connects to ArchiGen Connect through MCP. ArchiGen Connect provides the AEC-specific tools, project context, execution, safe modification, and verification layer used to work with supported design software.

## Before you begin

You need:

- ArchiGen Connect Beta.20 installed on Windows 10/11 x64.
- A signed-in ArchiGen Connect session.
- Rhino 8 and Grasshopper available on the computer.
- ChatGPT access to the Developer Mode app-creation flow and required tool permissions. Availability depends on your plan and workspace policies; check ChatGPT's current documentation and do not assume every account supports write actions.
- A separately installed secure tunnel that can provide an HTTPS URL forwarding to a local HTTP endpoint. ArchiGen Connect does not provide or embed this tunnel.

## Setup sequence

### 1. Install ArchiGen Connect

Download and install [ArchiGen Connect Beta.20](https://github.com/ArchiGenio/archigen-connect/releases/tag/v0.1.0-beta.20). See [INSTALL.md](INSTALL.md) for normal installation and install-over updates.

### 2. Launch and sign in

Launch ArchiGen Connect and complete its normal sign-in flow. This local ArchiGen authentication must already be active before ChatGPT can use the connected session.

Use the normal ArchiGen Connect sign-in flow. Do not paste account or session credentials into ChatGPT.

### 3. Select a project

Select the project folder you want ArchiGen Connect to work with.

### 4. Connect Rhino and Grasshopper

Open Rhino 8 and Grasshopper, then connect them from ArchiGen Connect. Confirm that the applications are available before continuing.

### 5. Open ChatGPT

Open ChatGPT in a workspace that supports the Developer Mode app-creation flow.

### 6. Enable the required Developer Mode feature

Beta.20 uses ChatGPT's Developer Mode path for adding a development MCP app. Client settings may vary by account and workspace; there is no separate ArchiGen Developer Mode toggle.

### 7. Start the ArchiGen ChatGPT bridge

Open PowerShell and start the packaged bridge:

```powershell
& "$env:ProgramFiles\ArchiGen Connect\ArchiGenConnect.exe" --chatgpt-bridge
```

The packaged ChatGPT MCP connection listens locally at:

```text
http://127.0.0.1:10502/mcp
```

The local endpoint is not entered directly into ChatGPT. It is the destination for the secure tunnel.

### 8. Provide ChatGPT with the MCP endpoint

Start the separately installed secure tunnel and configure it to forward to:

```text
http://127.0.0.1:10502/mcp
```

Use the tunnel's resulting **HTTPS MCP endpoint**. Expose only this MCP connection over secure HTTPS, not unrelated local services.

In ChatGPT Developer Mode, open:

**Settings / Apps / Create**

Enter the tunnel's HTTPS MCP endpoint, then select **Scan Tools**.

Create the development app with:

- **Name:** `ArchiGen Connect`
- **Description:** `Control your local ArchiGen Connect session for Rhino and Grasshopper through natural-language design requests.`

This is an MCP server added through ChatGPT's development app flow, not an ArchiGen-specific connector download or a generic ChatGPT plugin.

### 9. Confirm the connection

After **Scan Tools** completes, confirm that ChatGPT discovers ArchiGen tools, including:

- `archigen_status`
- `archigen_execute_task`
- `archigen_inspect_task`
- Supported `gh_*` and `rhino_*` tools for the connected AEC workflow

The local status result should show that ArchiGen is authenticated and online, and that Rhino and Grasshopper are available. The current project should also be identified when one is selected.

### 10. Run the first status test

Send this prompt in ChatGPT:

```text
Check my local ArchiGen Connect status.
```

If ChatGPT asks you to address the app explicitly, use the app name **ArchiGen Connect** with the same request.

### 11. Run the first Grasshopper execution test

After the status test confirms the local connection, send:

```text
Create a Grasshopper circle with an editable radius of 8.
```

The expected workflow is planning followed by the available Grasshopper actions, then a solve and inspection step. A successful result should report the resulting task and verification state rather than only acknowledging the request.

## Troubleshooting

### ArchiGen Connect is not visible in ChatGPT

Confirm that ChatGPT Developer Mode is enabled, that you opened **Settings / Apps / Create**, and that you entered the secure tunnel's HTTPS MCP endpoint. Run **Scan Tools** again. The local `http://127.0.0.1:10502/mcp` address is not the address ChatGPT can use directly.

### Authorization or sign-in fails

Sign in again through ArchiGen Connect and retry the status test. Do not paste passwords or session credentials into ChatGPT or GitHub Issues.

### The local desktop is not connected

Confirm that the packaged bridge was started with `--chatgpt-bridge` and that it remains running. Restart the bridge, then restart or rescan the ChatGPT app.

### Rhino or Grasshopper is unavailable

Open Rhino 8 and Grasshopper, confirm they are connected in ArchiGen Connect, and rerun the status test. The first execution test requires the supported Rhino and Grasshopper workflow to be available.

### MCP actions are not refreshed or are unavailable

Confirm that the tunnel is forwarding to `http://127.0.0.1:10502/mcp`, then run **Scan Tools** again. If the tool list is still stale, restart the bridge and reconnect or recreate the development app using the current HTTPS MCP endpoint.

## Scope of this guide

This guide covers Beta.20 ChatGPT Developer Mode setup. Revit is under development. Claude, Gemini, local/Ollama AI, AutoCAD, Blender and broader integrations remain roadmap items, not current production support.