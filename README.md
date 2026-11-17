# Knowasiak for AI assistants

[Knowasiak](https://knowasiak.com) is an online business community where founders and business owners learn, connect and share. This repository connects it to Gemini CLI. The same MCP server works in any MCP client.

## Gemini CLI

```bash
gemini extensions install https://github.com/Knowasiak/knowasiak-mcp
```

Then ask, for example: "Find a packaging supplier in Sydney on Knowasiak", "Who on Knowasiak is in Dubai and here to meet people?", "How does the Knowasiak feed rank posts?"

## Any other MCP client

| Address | Sign-in | What it does |
|---|---|---|
| `https://knowasiak.com/mcp` | None | Search businesses, people, posts and help; Discover; the people map; read anything public in full |
| `https://knowasiak.com/mcp/account` | Your Knowasiak account (OAuth 2.1) | All of the above for you, plus your profile, numbers, posts, notifications and messages; post, comment, follow, message (it shows you first) |

Transport: Streamable HTTP. Tools, limits and privacy: https://knowasiak.com/help/connect-your-ai-assistant. Server card: https://knowasiak.com/.well-known/mcp/server-card.json.

## Tools (no sign-in)

`find_businesses`, `search`, `fetch`, `latest_posts`, `discover_people`, `person_details`, `people_map`, `people_in_place`. Help guides are also MCP resources, and there are a few prompts.

Support: support@knowasiak.com
