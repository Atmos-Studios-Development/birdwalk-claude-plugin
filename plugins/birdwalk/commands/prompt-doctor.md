---
description: Check a draft prompt against the model's rules before Generate — reference naming, camera moves, contradictions, speech and music, unsupported asks.
argument-hint: <shot or pasted prompt>
---
Review this Birdwalk prompt before it's generated: $ARGUMENTS

If a shot is named, pull the draft with `birdwalk_read_generation`. Call `birdwalk_get_shot_options` for its model, then check:
- every attached reference is named the way that model expects (the `birdwalk` skill's "Naming attached references": `@Image N` on Seedance, its own markers on Kling O3 4K, none on Kling 3 Pro or Veo);
- one camera move per beat, and no contradictions;
- speech written the way the model handles it (quoted lines on Seedance and Veo; described, not scripted, on Kling), and music exclusions explicit;
- nothing asked for that the model can't do.

Propose the corrected prompt and offer to save it with `birdwalk_update_shot_prompt`.
