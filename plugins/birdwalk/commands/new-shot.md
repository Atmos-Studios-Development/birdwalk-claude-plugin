---
description: Draft a new Birdwalk shot from a brief — picks the model, checks its options, writes the prompt and saves a draft for the person to generate.
argument-hint: <project> <scene> <brief>
---
Draft a new shot in Birdwalk from this brief: $ARGUMENTS

Follow the `birdwalk` skill. Orient first: the project, its memory, the scene, neighbouring shots and any references the person named. Call `birdwalk_get_shot_options` for the chosen model, write the prompt in that model's shape with its own way of naming references, then save it with `birdwalk_create_shot`. Finish with the two or three things to check before pressing Generate.
