# boqo for Claude Code

**boqo is an autonomous AI agent for social media**, for creators, brands and products. It finds videos worth posting, turns long videos into short vertical clips with animated captions, and schedules or auto-posts them to TikTok, Instagram and YouTube. It can also watch Twitch and Kick streams and clip the moments as they happen.

This repository is the official boqo plugin and marketplace for [Claude Code](https://docs.claude.com/en/docs/claude-code). It connects Claude Code to boqo's remote MCP server, `https://mcp.boqo.ai/mcp`, and adds a skill that tells the agent how to use it.

## Install

In Claude Code:

```
/plugin marketplace add boqo-ai/boqo-plugins
/plugin install boqo@boqo-plugins
```

The first time a boqo tool runs, Claude Code opens a sign-in window. Sign in to your boqo account (or create one, free) and allow access.

Without the plugin, you can add only the MCP server:

```
claude mcp add --transport http boqo https://mcp.boqo.ai/mcp
```

## What you can ask

- "Find three long podcast episodes about AI startups from this month and make clips from the best one."
- "Make clips from https://www.youtube.com/watch?v=… and send me the top one."
- "Schedule the three best clips to my TikTok, one a day at 18:00."
- "Turn on auto-post for this channel to my Instagram."
- "Watch twitch.tv/… while it's live and clip the big moments."
- "Blur faces in this clip", "clean up the audio", "make three unique copies".
- "How many credits do I have left, and how did last week's posts do?"

## What it can do

The server exposes boqo's own tools, the same things you can do in the app:

| Area | Tools |
|---|---|
| Find ideas | `find_videos`, `channel_videos`, `inspect_videos`, `follow_channel` |
| Make clips | `create_clips`, `create_upload`, `complete_upload`, `reanalyze_project`, `fix_clip`, `rerender_brand`, `create_uniqueizer`, `create_speech`, `enhance_audio`, `blur` |
| Live streams | `start_watch`, `stop_watch`, `list_moments`, `clip_moment`, `skip_moment` |
| Post | `schedule_post`, `list_schedule`, `get_posting`, `set_posting`, `move_post`, `reschedule_post`, `cancel_post`, `auto_post`, `auto_post_off` |
| Results | `get_analytics`, `list_clips`, `get_clip` |
| Workspace | `get_account`, `list_accounts`, `reconnect_account`, `list_projects`, `get_project`, `search`, `list_brands`, `remember_brand`, `set_project_brand`, `list_collections`, `set_collection_membership`, `set_favorite`, `rename_project`, `rename_clip`, `stop_project`, `retry_project`, `delete_project`, `restore_project`, `cancel_card` |

## Credits and safety

- Actions that make something spend credits from your boqo plan. Every account starts free; see [pricing](https://boqo.ai/pricing).
- Every action runs as soon as the agent asks. In boqo, under **Account → Connections**, you can set a daily credit cap for each connection (an action over it waits for your approval) and revoke a connection at any time.
- Download links to clips expire after one hour.

## Other clients

boqo also works in Claude, ChatGPT, Cursor and VS Code, and with an API key from any MCP client. Setup for each: [boqo.ai/mcp](https://boqo.ai/mcp).

## Links

- Website: [boqo.ai](https://boqo.ai)
- MCP server: `https://mcp.boqo.ai/mcp` (streamable HTTP, OAuth)
- Privacy: [app.boqo.ai/privacy](https://app.boqo.ai/privacy)
- Terms: [app.boqo.ai/terms](https://app.boqo.ai/terms)
