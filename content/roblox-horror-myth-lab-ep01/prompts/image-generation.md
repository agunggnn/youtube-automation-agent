# Image and video generation prompts — Episode 01

## Global style prompt

Create cinematic Roblox-inspired 3D stills for a YouTube horror investigation, 16:9 landscape, readable composition, cool blue moonlight with restrained amber practical lights, deep charcoal shadows, volumetric flashlight beam, high contrast while preserving dark detail, polished game-render aesthetic, clean silhouettes, subtle film grain, no gore.

**Character lock:** use RHM_INVESTIGATOR_01 from ../assets/character-reference.svg as the design reference. Keep the exact messy black swept-fringe hair with three recognizable tufts, square Roblox-like proportions, black zip hoodie with white zipper and drawstrings, charcoal pants, black-and-white chunky sneakers, and compact dark-gray flashlight. Preserve identity across every shot; only pose, camera, expression, and lighting may vary.

**Evidence integrity:** generated imagery is for illustrative transitions, chapter cards, and thumbnails only. It must not be represented as actual footage, a real game mechanic, or proof of a myth. Record actual Roblox gameplay separately and use that footage for tests and verdicts.

## Character turnaround prompt

Create a clean studio character turnaround sheet for RHM_INVESTIGATOR_01, a Roblox-inspired blocky 3D investigator avatar. Show full-body front, three-quarter, side and back views, plus four small expression views: neutral, curious, startled, relieved. Fixed design: messy black swept-fringe hair with three recognizable pointed tufts; square block head; black zip hoodie with white zipper and two white drawstrings; charcoal pants; black-and-white chunky sneakers; compact dark-gray flashlight. Neutral light-gray background, consistent proportions, soft studio lighting, no dramatic perspective, no logos. Keep every view recognizably the same character.

## Storyboard scene prompts

Generate each scene separately using the character reference. Do not ask the image model to render titles or exact text; add all titles, labels, timestamps and verdict graphics in the editor.

1. **Cold open:** first-person flashlight beam catches a generic red-eyed shadow at the far end of a narrow abandoned corridor; investigator partially visible at frame edge; genuine suspense, no gore.
2. **Challenge reveal:** investigator stands in front of a wall with ten pinned mystery cards and evidence photos; three-quarter medium shot, dramatic cool-blue rim light.
3. **Rules board:** investigator beside three clean blank verdict panels in green, red and amber; generous negative space for editor-added typography.
4. **Controlled test setup:** over-shoulder view of investigator observing a generic horror-game corridor; visible landmarks for comparing attempts.
5. **Movement test illustration:** low-angle blocky avatar moving carefully along a corridor while a shadow silhouette remains distant; illustration only, not evidence.
6. **Hiding test illustration:** investigator crouched beside a locker/alcove while the distant corridor is empty; maintain spatial continuity.
7. **Clue test illustration:** flashlight beam illuminating a subtle wall symbol; generic motif only, never claim it is a real in-game clue.
8. **Audio test illustration:** close shot of avatar wearing simple headphones, listening in a dim corridor; sound-wave graphic can be added in edit.
9. **Midpoint reset:** investigator at a board with five blank result cards marked as tested; keep verdicts blank until evidence review.
10. **Final results:** investigator beside a ten-card evidence board with blank result tiles; cinematic wide shot, space for real results.
11. **End screen:** investigator holding flashlight and gesturing toward two empty video-card spaces, dark blue background.

## Thumbnail A — main

1280x720 YouTube thumbnail, Roblox-inspired blocky investigator avatar RHM_INVESTIGATOR_01 large in foreground, exact black messy swept hair and black hoodie with white drawstrings, holding flashlight; generic red-eyed shadow silhouette in background doorway; dramatic blue/orange contrast, bright face and flashlight, simple dark background, clear space on left for editor-added words “10 HORROR MYTHS”, readable at mobile size, no watermark, no fake game UI.

## Thumbnail B — alternate

1280x720 thumbnail, same exact investigator avatar centered between a large green check and red X, ominous corridor background, bold contrast, clear space at top for editor-added “REAL OR FAKE?”, no embedded typography, no watermark, no fabricated gameplay interface.

## Thumbnail C — alternate

1280x720 thumbnail, same investigator avatar seen from behind facing a mysterious closed door with warm light leaking from the gap, flashlight beam leading the eye, cinematic game-render style, clear space on right for editor-added “SECRET FOUND?”; use this wording only if the final video truly investigates a secret.

## Continuity workflow

1. Generate the turnaround first.
2. Approve a master reference and save it as assets/character-reference.png.
3. For every scene, attach the master reference and paste the global style plus scene prompt.
4. Keep aspect ratio and seed/reference controls fixed when supported.
5. Reject outputs with altered clothing, hair, proportions, or props.
6. Track scene ID, prompt, model, reference image, generation date, and whether the asset is illustrative or real gameplay.
7. Never use generated art as evidence for a myth verdict.
