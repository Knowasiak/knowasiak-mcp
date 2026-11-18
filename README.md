# Knowasiak for AI agents

[Knowasiak](https://knowasiak.com) is an online business community where founders and business owners learn, connect and share. This repository is the Knowasiak plugin for AI agents, in the [Agent Plugins](https://agent-plugins.org) format (Cursor, ChatGPT/Codex and other clients), plus a Gemini CLI extension.

## What's inside

| File | What it is |
|---|---|
| `plugin.json` | Agent Plugins manifest |
| `mcp.json` | Two remote MCP servers (Streamable HTTP): `knowasiak` (no sign-in) and `knowasiak-account` (the member's own account, OAuth sign-in on knowasiak.com) |
| `skills/find-businesses` | Find and compare suppliers, agencies and partners, by what they do and where |
| `skills/meet-people` | Discover people worth following, people like someone, and who is in a city |
| `skills/act-for-me` | Post, comment, follow and message for the signed-in member, always after showing them first |
| `.claude-plugin/plugin.json`, `.claude-plugin/marketplace.json`, `.mcp.json` | Claude Code plugin, and this repo as its own plugin marketplace |
| `gemini-extension.json`, `GEMINI.md` | Gemini CLI extension |

## Install

**Cursor and other Agent Plugins clients:** add this repository as a plugin (`https://github.com/Knowasiak/knowasiak-mcp`).

**Claude Code:**

```bash
claude plugin marketplace add Knowasiak/knowasiak-mcp
claude plugin install knowasiak@knowasiak
```

**Claude (claude.ai and the desktop app):** Settings → Connectors → Add custom connector, URL `https://knowasiak.com/mcp`.

**Gemini CLI:**

```bash
gemini extensions install https://github.com/Knowasiak/knowasiak-mcp
```

**Any MCP client:** add `https://knowasiak.com/mcp` as a remote MCP server (Streamable HTTP, no auth). For the member's own account use `https://knowasiak.com/mcp/account`; the client opens Knowasiak's sign-in page the first time.

Then ask, for example: "Find a packaging supplier in Sydney on Knowasiak", "Which businesses on Knowasiak are in Dubai?", "Find people like @AdityaGaurav on Knowasiak".

## Tools

No sign-in: `find_businesses`, `search`, `fetch`, `latest_posts`, `discover_people`, `person_details`, `people_map`, `people_in_place`. Help guides are MCP resources; a few prompts are included.

Member account (adds): `get_my_profile`, `get_my_stats`, `list_my_posts`, `create_post`, `comment_on_post`, `mark_useful`, `update_my_profile`, `follow`, `unfollow`, `list_my_connections`, `my_network_map`, `list_notifications`, `list_saved_posts`, `list_conversations`, `read_conversation`, `send_message`.

Everything follows the site's rules, with hourly limits for assistants. Nothing deletes anything. Details, limits and privacy: https://knowasiak.com/help/connect-your-ai-assistant · Server card: https://knowasiak.com/.well-known/mcp/server-card.json · Official MCP Registry: `com.knowasiak/knowasiak`.

Support: support@knowasiak.com
