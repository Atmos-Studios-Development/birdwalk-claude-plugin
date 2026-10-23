---
description: Review the takes on a Birdwalk shot — look at each frame, compare against the brief and references, and recommend which to prefer.
argument-hint: <shot>
---
Review the takes on this Birdwalk shot: $ARGUMENTS

Use `birdwalk_list_shots_in_project` to find the versions, and `birdwalk_read_generation(include_image: true)` on each. Compare them against the prompt, the references and the project memory. Recommend a preferred take and the one change most likely to improve the next version. Only call `birdwalk_set_preferred_version` or `birdwalk_rate_generation` when the person confirms.
