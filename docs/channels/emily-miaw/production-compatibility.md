# Emily Miaw — Silent Video Production Compatibility

**Status:** Audit notes / proposed design; no code changed and no production job run.

## Intended output

- 45–60 second vertical short.
- No spoken narration and no narration-derived subtitles.
- Music bed built around playful plucks, with comedy SFX and controlled pauses.
- Storyboard timing is the source of truth for scene duration.
- Final review includes visual continuity, runtime, audio peaks/loudness, and confirmation that the video remains understandable when muted.

## Known incompatibility in the existing Media-Fabric build path

The current repository's `tools/build_jev.py` path was previously audited and has narration-dependent assumptions:

- Requires a VO audio file (`vo-en.mp3` or `--vo`) and errors when it is missing.
- Scales storyboard timing against VO duration.
- Generates subtitle cues from `vo_text`.
- Always adds VO as an audio input and mixes music relative to VO.
- Validates final runtime and loudness against the VO duration and target audio settings.

Therefore, the existing builder is **not compatible with true narration-free production as currently written**. A dummy VO track is not an acceptable workaround because it would obscure the actual timing and audio requirements.

## Proposed implementation direction — not approved for implementation

Add a clearly separated silent mode or assembly path that:
1. Uses approved storyboard timing as the runtime source of truth.
2. Does not require a VO file and does not synthesize narration.
3. Does not force narration-derived subtitle cues.
4. Mixes music and per-shot SFX with explicit gain, fades, peak limits, and audio-duration checks.
5. Preserves normal video QC and verifies actual output duration, frame dimensions, frame rate, decode success, and audio stream behavior.
6. Fails clearly if a requested music/SFX asset is missing rather than silently substituting fake content.
7. Keeps the existing narrated workflow unchanged by default.

## Media-Fabric integration checks

Before implementation, inspect the actual current backend/API contract and confirm:
- How still-image references and character consistency are passed.
- Whether generated video clips support reference images and fixed durations.
- How music and discrete SFX are attached, mixed, or passed through to FFmpeg.
- Whether the workflow supports silent jobs end to end without synthesizing VO.
- Whether job status, artifact paths, retries, and failures are observable.
- Whether any defaults inject narration, captions, or generated text.

The live Media-Fabric backend was not independently verified in this documentation pass. Do not assume support until tested against its actual contract.

## Required approval gates

- [ ] Story premise and revised beat outline approved.
- [ ] Character descriptions and visual bible approved.
- [ ] Character-sheet generation explicitly approved.
- [ ] Silent-mode implementation plan approved.
- [ ] Code changes reviewed before production execution.
- [ ] Stills, animation, final render, and publication each receive their intended review.

**No assets were generated, no PC job was run, no production files were modified, and no video was published as part of this documentation.**
