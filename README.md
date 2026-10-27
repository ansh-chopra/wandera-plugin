# Wandera plugin

Wandera generates short AI videos from a text description using models such as Seedance, Kling and Veo, compares models side by side, and turns videos into Meta (Facebook and Instagram) video ads, from inside your AI agent.

Built by [Zero Billion](https://www.zerobillion.ai). Product page: https://wandera.ai/mcp

## What's in this plugin

| Component | File | What it does |
| --- | --- | --- |
| MCP server | `.mcp.json`, `mcp.json` | Connects to Wandera's remote MCP server at `https://api.wandera.ai/mcp` over HTTPS |
| Skill | `skills/get-started/SKILL.md` | Walks the agent through checking the account, quoting a price, generating and sharing a video |

No hooks, scripts, binaries or local code. Nothing runs on your machine beyond the agent's own MCP client.

## Network endpoints

- `https://api.wandera.ai/mcp`: Wandera's MCP server (tools for video generation, model comparison and Meta ads).
- `https://api.wandera.ai/.well-known/*` and `/oauth/*`: OAuth 2.1 discovery, registration and token endpoints.
- `https://wandera.ai/oauth/consent`: the sign-in page you approve in your browser (Google sign-in).

## Credentials

Sign in with OAuth when your agent first connects; no API keys are stored in this repo. Video generation spends credits from your Wandera account. The Meta ads tools additionally use a Meta Marketing API token you connect at https://wandera.ai/mcp. Ads are created paused.

## Tools

`list_video_models`, `estimate_video_cost`, `generate_video`, `get_video`, `compare_video_models`, `list_my_videos`, `account`, `meta_list_ad_accounts`, `meta_list_campaigns`, `meta_insights`, `meta_top_ads`, `meta_upload_video`, `meta_create_video_ad`, `meta_set_status`, `meta_set_daily_budget`.

## Links

Privacy: https://wandera.ai/privacy · Terms: https://wandera.ai/terms · Support: ansh@zerobillion.ai

License: MIT
