# Maple — Work v2 preview, revision 2

Maple now has a clearer six-frame inspection animation and a rebuilt eight-pose second gaze row. The inspection loop uses focused eyes, a deliberate head turn, and a curious tilt. The gaze row fixes the previous width-variation failure.

![Maple inspecting](idle-review-idle.gif)

This is the same preview stage as Cosmo's thinking update: locally validated artwork, previews, and independent visual review. It is not a new installable desktop release or a verified cloud update. Live-app testing is deferred. The existing desktop v2.1 download remains unchanged.

## Checks

- Encoded Work v2 sheet: structural PASS, 1536×2288, 73 required poses and 15 transparent unused cells.
- Gaze width variation: **1.44×**, within the **1.50×** limit; previously 1.526×.
- Independent blind direction review: all four cardinals pass. The slightly-up-left 292.5° pose is subtle in isolation; labeled sequence review accepts it with a warning.
- Independent visual review: inspection intent, identity, scale, and baseline accepted for a candidate preview. Some adjacent gaze angles remain unevenly separated.
- Only rows 8 and 10 changed. All other **59 required poses are pixel-identical** to the previous compatibility preview.
- All six inspection poses have complete tails and the same foot baseline. Two clipped generation attempts were rejected before the accepted margin correction.

The full production quality gate, live host playback, Library persistence, and cloud upload verification remain incomplete. No installed pet or active selection changed.

## Artifacts

[Sprite sheet](spritesheet.webp) · [All-state GIF](all-states.gif) · [MP4](all-states.mp4) · [Contact sheet](contact.png) · [Inspection stills](inspection-stills.png) · [Dark background](dark-background.png)

[Gaze sheet](directions.png) · [Gaze loop](look-loop.gif) · [Jump transition](idle-jump-idle.gif) · [Structural report](validation.json) · [Geometry](geometry.json) · [Blind direction check](blind-validation.json) · [Visual review](visual-review.json) · [Preservation check](preservation.json) · [Checksums](manifest.json)

The [generation prompts](generation-prompts.txt) were run with built-in ImageGen. Extraction, shared-scale registration, edge cleanup, assembly, and validation used the bundled Work Pets tools. Cleanup was retained only for the newly generated rows.

Next: test Maple and Cosmo in the host together when requested. Scripted companion behavior remains a separate future project.
