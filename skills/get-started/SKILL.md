---
name: get-started
description: Set up Wandera and make a first AI video. Use when the user has just installed Wandera or asks how to start making videos or Meta ads with it.
---

# Get started with Wandera

1. Call `account` to check the user is signed in and see their credit balance. If they have no credits, send them to https://wandera.ai/mcp to pick a plan.
2. Ask what the video is for (ad, social post, test idea) and the aspect ratio, then call `list_video_models` with that use case.
3. Quote the price with `estimate_video_cost` before generating, and only generate after the user agrees.
4. Call `generate_video`, then `get_video` until it finishes, and share the link.
5. To test several models at once, use `compare_video_models` and share the side-by-side page.
6. For Meta ads, the user connects their ad account at https://wandera.ai/mcp. Ads are always created paused; never activate one or raise a budget unless the user explicitly asks.
