# Birdwalk plugin for Claude

A skill, slash commands and the hosted Birdwalk connector, packaged as a Claude plugin. The skill teaches Claude how a filmmaker works in Birdwalk; the connector (`https://studio.birdwalk.ai/mcp`) does the work. This repository contains no Birdwalk application code and no secrets.

## Install in Claude Code

From a terminal:

    claude plugin marketplace add Atmos-Studios-Development/birdwalk-claude-plugin
    claude plugin install birdwalk@birdwalk

Or inside a Claude Code session, run `/plugin marketplace add Atmos-Studios-Development/birdwalk-claude-plugin`, then `/plugin install birdwalk@birdwalk` and confirm the scope in the panel that opens.

The first time Claude uses Birdwalk, sign in to your Birdwalk account in the browser when asked.

## Use the skill on claude.ai

1. Add Birdwalk as a custom connector under Settings → Connectors, using the address from Birdwalk → Account → Connect AI. On the Free plan you can add one custom connector. On Team, an Owner or Primary Owner adds it for the organisation; on Enterprise, an Owner, or a custom role with "Manage access to Libraries", does.
2. Zip the `plugins/birdwalk/skills/birdwalk` folder and upload the zip under Customize → Skills. Code execution needs to be switched on.

Plan details are Anthropic's and can change.

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
