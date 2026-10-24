# Birdwalk plugin for Claude

A skill, slash commands and the hosted Birdwalk connector, packaged as a Claude plugin. The skill teaches Claude how a filmmaker works in Birdwalk; the connector (`https://studio.birdwalk.ai/mcp`) does the work.

## Install in claude.ai or the Claude desktop app

1. Go to **Customize → Plugins → Add → Add marketplace** and enter `Atmos-Studios-Development/birdwalk-claude-plugin`.
2. Install **Birdwalk**.
3. Open the plugin's **Connectors** tab and connect Birdwalk. Sign in to your Birdwalk account when asked.

If you already use the Birdwalk connector in Claude, keep it. The plugin adds the skill and the commands on top.

## Install in Claude Code

From a terminal:

    claude plugin marketplace add Atmos-Studios-Development/birdwalk-claude-plugin
    claude plugin install birdwalk@birdwalk

Or inside a Claude Code session, run `/plugin marketplace add Atmos-Studios-Development/birdwalk-claude-plugin`, then `/plugin install birdwalk@birdwalk` and confirm the scope in the panel that opens.

The first time Claude uses Birdwalk, sign in to your Birdwalk account in the browser when asked.

## Try it

- Ask Claude: "List my Birdwalk projects."
- `/birdwalk:review-takes`: compare the takes of a shot.
- `/birdwalk:prompt-doctor`: improve a prompt for its model.
- `/birdwalk:new-shot` and `/birdwalk:lookdev`: draft a new shot, or explore a look.

Claude only saves drafts. Nothing is generated or charged until you press Generate in Birdwalk.

## What's inside

    .claude-plugin/marketplace.json      the marketplace listing
    plugins/birdwalk/
    ├── .claude-plugin/plugin.json       plugin manifest
    ├── .mcp.json                        hosted Birdwalk connector
    ├── README.md                        what the plugin runs, sends and fetches
    ├── skills/birdwalk/SKILL.md         how to work in Birdwalk
    └── commands/
        ├── new-shot.md                  /birdwalk:new-shot
        ├── lookdev.md                   /birdwalk:lookdev
        ├── review-takes.md              /birdwalk:review-takes
        └── prompt-doctor.md             /birdwalk:prompt-doctor
