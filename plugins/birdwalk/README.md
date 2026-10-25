# Birdwalk for Claude

This plugin lets Claude work in Birdwalk, the AI filmmaking platform, on your behalf. Claude can draft shots and image assets, write prompts in each video model's own style, plan 3D Stage previs, and find its way around your projects, scenes, shots and versions. Claude only saves drafts: nothing is generated or charged until you press Generate in Birdwalk.

## What it runs, sends and fetches

- **One connector:** the plugin adds the hosted Birdwalk MCP server at `https://studio.birdwalk.ai/mcp`. Nothing runs on your computer apart from Claude itself.
- **Sign-in:** the first time Claude uses it, you sign in to your Birdwalk account in the browser (OAuth). The plugin stores no passwords, keys or tokens.
- **What goes to Birdwalk:** the requests Claude makes on your behalf, such as listing your projects, reading a shot or an asset, and saving a draft prompt. These are subject to Birdwalk's Terms and Privacy Policy (https://studio.birdwalk.ai/v2/terms, https://studio.birdwalk.ai/v2/privacy).
- **What comes back:** your own Birdwalk data: project and shot details, prompts, asset previews and generation results.

## What's inside

- `skills/birdwalk/SKILL.md`: how to work in Birdwalk well.
- `commands/`: `/birdwalk:new-shot`, `/birdwalk:lookdev`, `/birdwalk:review-takes` and `/birdwalk:prompt-doctor`.
- `.mcp.json`: the Birdwalk connector.

You need only one Birdwalk connection. If you've already added Birdwalk as a connector in Claude, turn that one off under Customize → Connectors once the plugin's connection is set up; otherwise Claude sees every Birdwalk tool twice.
