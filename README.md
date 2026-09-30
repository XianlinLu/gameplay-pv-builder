# Gameplay PV Builder

[English](README.md) | [简体中文](README_ZH-CN.md)

Gameplay PV Builder is a reusable skill for producing coherent game trailers, concept gameplay demos, and open-world gameplay shorts from a game brief, asset set, or reference video.

It turns a reference into a time-coded gameplay structure, locks character and UI continuity before motion generation, builds short traceable shots, and assembles a 30–60 second master with synchronized audio stems.

## Outputs

- character four-view sheet and 3D form card;
- UI master and scene keyframes;
- production brief and shot manifest;
- individual gameplay shots;
- music, ambience, combat, UI, and optional voice stems;
- a 45-second master by default, or another 30–60 second duration;
- delivery and quality-control report.

## Two supported structures

- **Three-part gameplay:** guidance, story/traversal, and combat/climax.
- **Open-world urban gameplay:** city establishment, traversal, discovery, systemic interaction, escalation, and payoff.

## Use

Invoke the skill with a game concept, existing assets, or a reference video:

```text
Use $gameplay-pv-builder to build a 45-second 16:9 gameplay PV from this reference. Keep the HUD pixel-stable, show character selection, traversal, street combat, a boss encounter, and a results screen.
```

The skill first creates a continuity pack and shot manifest. It then generates or coordinates short shots and composites the approved UI master as a separate layer whenever possible.

## Lumina import

This repository is intentionally text-only for direct Lumina canvas import. Every tracked file uses one of Lumina's supported lowercase extensions: `.md`, `.json`, `.yaml`, `.yml`, or `.txt`.

To avoid the “Some documents need to be processed” error:

1. Import the repository or all tracked files as-is.
2. Do not add extensionless files such as `LICENSE` to the import set. The license here is named `LICENSE.md`.
3. Do not add video, image, audio, archive, source-code, or hidden configuration files to the skill package.
4. Keep generated media outside the package and reference it from the textual manifest using stable IDs or URLs.
5. Keep names within 64 characters and use only letters, numbers, underscores, and hyphens before the lowercase extension.

See [LUMINA_IMPORT.md](LUMINA_IMPORT.md) for the preflight checklist.

## Repository map

- `SKILL.md` — skill entrypoint and complete workflow.
- `agents/openai.yaml` — user-facing skill metadata.
- `references` — reference analysis, continuity/UI rules, and audio/delivery rules.
- `templates` — editable project brief and shot manifest.

## License

MIT. See [LICENSE.md](LICENSE.md).
