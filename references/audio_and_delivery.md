# Audio and delivery

## Audio stems

Deliver separate, synchronized stems when the host supports media output:

- music;
- ambience;
- player movement and weapons;
- enemy and combat impacts;
- UI and menu feedback;
- voice and dialogue, when present.

Keep a small amount of headroom on individual stems. Avoid irreversible limiting before the final mix. Use the loudness and peak specification supplied by the target platform; if none is supplied, document the chosen mastering target in the delivery report rather than claiming a universal standard.

## Synchronization checks

Check footsteps, landings, weapon swings, shots, parries, hit reactions, ability triggers, UI confirmations, objective changes, and the results reveal frame by frame. A prominent visual impact without a synchronized audio event should be treated as unfinished.

## Master delivery

Default to a 45-second, 16:9, 1920×1080, 30 fps master when the user provides no platform specification. Also provide the shot manifest and source-to-output lineage so individual shots can be regenerated without rebuilding the entire sequence.

For Lumina, keep binary video, image, and audio files outside the imported skill package. Store only textual prompts, manifests, IDs, links, checksums, and notes in supported text formats.
