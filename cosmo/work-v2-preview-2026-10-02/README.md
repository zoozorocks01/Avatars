# Cosmo Royal — Work v2 preview

Cosmo now has a six-frame thinking animation: planted feet, a paw at his chin, small head tilts, changing gaze, and a blink. This preview also includes the locally refined fabric running animation and compact basketball flip.

![Idle to thinking to idle](idle-work-idle.gif)

This is a development preview, not a new installable desktop release or a verified ChatGPT cloud update. The existing v1.1 download and catalog entry remain the desktop release.

## Files and checks

- [Sprite sheet](spritesheet.webp), [all-state GIF](all-states.gif), [MP4](all-states.mp4), and [contact sheet](contact.png).
- [Thinking stills](thinking-stills.png), [idle/jump transition](idle-jump-idle.gif), [gaze sheet](directions.png), and [gaze loop](look-loop.gif).
- [Structural validation](validation.json), [geometry checks](geometry.json), and [checksums](manifest.json).
- [Approved generation prompt](generation-prompt.txt). Built with the built-in ImageGen tool, then extracted and assembled using the Work Pets bundled tools.

The encoded sheet passes the local Work v2 structural validator: 1536×2288, 73 occupied required cells, 15 transparent unused cells. The legacy extra neutral pose was removed; idle frame zero supplies the resting reference. The six work frames are new; all other 67 required poses are pixel-identical to the compatibility source. The new row shares one scale and a one-pixel baseline adjustment.

Jump geometry measures 50 pixels of lift and a one-pixel landing difference from idle. Gaze geometry passes, with continuity warnings at the wrap boundaries. Several neighboring gaze angles remain subtle. Independent still-frame review accepts the thinking action and identity; timed host playback remains unverified. The full quality gate and cloud upload checks are not complete.

Next: finish final motion/direction review and cloud validation before promoting this preview. Scripted companion behavior remains a separate future project.

Unofficial fan creation; not affiliated with BYU or OpenAI.
