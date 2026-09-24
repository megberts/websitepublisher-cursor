# WebsitePublisher for Cursor

The AI web platform, inside [Cursor](https://cursor.com). Describe a website, app or store — it goes live on a real URL with auth, payments, forms, 114 integrations and memory built in.

WebsitePublisher gives Cursor tools for projects, pages, assets, data (entities and records), forms, integrations and scheduled tasks. Every change is live immediately — there is no separate publish step.


## Requirements

- Cursor with MCP support
- A WebsitePublisher account
- Internet access to `https://mcp.websitepublisher.ai/`

## Features

- Manage WebsitePublisher websites
- Create, update, and inspect pages (changes go live immediately)
- Manage entities and entity data
- Work with forms
- Schedule website operations
- Use WebsitePublisher through Cursor's AI tools
- Authenticate securely with OAuth

## Installation

### Plugin installation

Install **WebsitePublisher.ai** from the Cursor Plugin Marketplace when it becomes available.

For development or repository-based testing, install the plugin from this repository using Cursor's local plugin workflow, then reload Cursor and open **Customize** to confirm that the WebsitePublisher MCP server is enabled.

### Manual MCP configuration

If the plugin is not available in your marketplace, add the following to your user MCP configuration at `%USERPROFILE%\.cursor\mcp.json` (Windows), `~/.cursor/mcp.json` (macOS/Linux) or `.cursor/mcp.json` in your project folder (project only):

```json
{
	"mcpServers": {
		"websitepublisher": {
			"url": "https://mcp.websitepublisher.ai/"
		}
	}
}
```

Restart Cursor after saving the configuration. Use Agent mode and enable the WebsitePublisher server from **Customize**.

## First connection

After installation, Cursor connects to the WebsitePublisher MCP server over Streamable HTTP. On the first tool call, Cursor opens the WebsitePublisher OAuth sign-in and authorization flow.

1. Sign in to your WebsitePublisher account, or create an account.
2. Authorize Cursor to access WebsitePublisher.
3. Return to Cursor.

Once authentication is complete, the WebsitePublisher tools become available in Agent mode.

## Authentication

WebsitePublisher uses OAuth for authentication.

Your WebsitePublisher password and other credentials are not stored in the Cursor plugin.

When authentication is requested:

1. Sign in to your WebsitePublisher account.
2. Authorize Cursor to access WebsitePublisher.
3. Return to Cursor.
4. Continue using the WebsitePublisher tools.

## What you can do

Once WebsitePublisher is connected, you can interact with your websites through Cursor using natural language.

The available tools include:

- Projects and project status
- Pages, HTML, versions, and rollbacks
- Assets such as images, CSS, JavaScript, JSON, and SVG files
- Entities and records
- Forms
- Scheduling
- Connected integrations

For example:

```text
List my WebsitePublisher projects.
```

```text
Show me the pages in the <project-name> project.
```

```text
Create a test page called "<page-name>".
```

```text
List the entities available in this project.
```

```text
Show me the fields of the <entity-name> entity.
```

```text
Show me the homepage version history and summarize the latest changes.
```

```text
Create a contact form for the <project-name> project and connect it to email.
```

```text
Build a portfolio website using WebsitePublisher with home, about, and contact pages.
```

Cursor will select the appropriate WebsitePublisher tools to perform the requested operation.

Review changes before applying them — every change goes live immediately. Page replacement, asset deletion, record deletion and rollback affect the live website.

## Troubleshooting

### WebsitePublisher tools are not available

If the WebsitePublisher tools do not appear in Cursor:

1. Make sure Cursor is in Agent mode.
2. Make sure the WebsitePublisher plugin or MCP configuration is installed.
3. Open **Customize** and confirm that the server is enabled.
4. Restart Cursor after changing `mcp.json`.
5. Check Cursor's **MCP Logs** for connection errors.

### Authentication fails

If the OAuth authentication flow fails, complete the sign-in process again and make sure you authorize Cursor to access WebsitePublisher. Make sure your browser can reach `https://mcp.websitepublisher.ai/` and that pop-ups are not blocked.

If the problem persists, contact WebsitePublisher support.

### Changes are not appearing

Changes are live immediately. Hard-refresh the page (Cmd/Ctrl+Shift+R); if you use a custom domain, allow a moment for the CDN cache.

### Manual configuration does not load

Confirm that the file is located at `%USERPROFILE%\.cursor\mcp.json` (Windows), `~/.cursor/mcp.json` (macOS/Linux) or .`cursor/mcp.json` in your project folder, that it uses the `mcpServers` key, and that the server URL is exactly `https://mcp.websitepublisher.ai/`.

## Links

- [WebsitePublisher](https://www.websitepublisher.ai)
- [WebsitePublisher MCP Documentation](https://www.websitepublisher.ai/docs/mcp)
- [MCP server discovery](https://mcp.websitepublisher.ai/.well-known/mcp.json)
- [Cursor](https://cursor.com)

## Support

Contact WebsitePublisher support through [Contact](https://www.websitepublisher.ai/contact) or email [support@websitepublisher.ai](mailto:support@websitepublisher.ai)