# Maple 2.1.0 — prototype

First public release, 2026-09-16. Build: `leg-continuity`.

## Included

- Larger left/right trot: 25.425% larger than the initial local V2.1 draft, with a tucked tail to preserve frame margins.
- Continuous textured legs with smoother joins, rounded bends and smaller paws, reducing the separate-piece appearance.
- Original approved timing and footfall paths; fixed body scale and placement across the trot.
- Subtle tail follow-through and the reviewed adult-proportion hop.
- Preserved idle, greeting, error, waiting, working/sniffing, review and all 16 look poses.
- Sprite format version 2: 1536 × 2288 RGBA, nine standard animation rows plus two gaze rows.

## Known limitations

- Sharply bent hind legs are still a little angular; dark paws can overlap in compact strides.
- Trot head is modestly smaller than standing; the crouched posture also makes the whole silhouette lower. Exact anatomical scale matching is not claimed.
- Tucked tail overlaps some rear-leg poses.
- Hop transitions and some intermediate gaze spacing remain imperfect; the 112.5-degree down-right cue is subtle.
- Curling up is not part of this release. The host controls triggers, repetition, interruption and Reduced Motion behavior.

## Verification

The final candidate passes 2,001 gait samples, atlas and frame validation with zero errors/warnings, exact left/right mirroring, unchanged-row pixel checks, and transparency checks. Independent ordered-frame review found no major visual defects; browser checks confirmed both trots playing and returning to idle. The preview was accepted by the creator. These checks do not certify the recipient's app or every live transition.

The pet contains only `pet.json` and `spritesheet.webp`. No installer executable, API access, account data or credential is needed. This is an unofficial personal pet, not an OpenAI product.
