# host0 for Claude

**host0 hosts whatever your agent creates** — HTML pages, sites, apps with a shared database, Markdown, PDFs — at a link you can share.

This plugin brings two things:

- **The host0 skill.** It teaches Claude to publish a file or folder to a live `https://<slug>.host0.app` URL with the host0 CLI, to build small team tools on host0's shared records (declared in an `h0.json`, no server code), and to manage what's live.
- **The host0 MCP server** (`https://mcp.host0.ai/mcp`, remote, OAuth sign-in). It manages apps you've already published: visibility, sharing by email, versions and restore, analytics, shared data and custom domains. It doesn't deploy.

## Setup

In Claude Code (or add it from the plugin directory in Claude and Cowork):

```
/plugin install host0 --marketplace host0-ai/skills
```

Publishing needs the host0 CLI (Node 18.18 or newer): see the install instructions at [host0.ai/docs#cli](https://host0.ai/docs#cli). The first publish starts a device login: Claude shows a link and a short code, you approve it on host0.ai in your own browser, and the CLI stores the key. Nothing personal is typed into the chat. The MCP server asks you to sign in the first time Claude uses it.

## Use it

Ask Claude:

- "Deploy this to host0"
- "Give me a link to this PDF"
- "Build a team todo list with a shared database and publish it"
- "Roll back the last deploy"

Apps are private by default: only you and people you invite can open them. Open one to anyone with the link, or make it public on the web, when you want to.

## What it sends where

Everything goes to host0 and nowhere else:

- **The skill** runs the host0 CLI, which sends the files you choose to publish (and the `h0.json` that declares shared data) to the host0 API at `host0.ai` and uploads them to `host0.app`. It also sends the email addresses you ask Claude to invite to an app.
- **The MCP server** at `mcp.host0.ai` reads and changes your apps on host0: their settings, share lists (email addresses), versions, analytics and shared records, which can hold whatever your app's visitors entered.

host0 keeps published apps, their shared records and your account until you delete them, and visit analytics for 13 months. Details: [privacy policy](https://host0.ai/legal/privacy).

Docs: [host0.ai/docs](https://host0.ai/docs). Plans: [host0.ai/pricing](https://host0.ai/pricing). Privacy: [host0.ai/legal/privacy](https://host0.ai/legal/privacy). Support: [host0.ai/support](https://host0.ai/support).

## License

MIT
