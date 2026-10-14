# Production plan and asset decisions

## Verified inputs

- `02_BRAND_ASSETS/leon-portrait-original.png`: 1254² supplied portrait. Use without altering facial structure, skin tone, or expression. The newly shown stylized portrait is a creative reference; the more photographic uploaded source is the film identity asset.
- `02_BRAND_ASSETS/leon-identity-board-original.png`: 1536 × 1024 supplied board. The lossless `leon-primary-lockup-reference.png` crop keeps its exact raster logo/wordmark pixels, background and effects included; it is not a transparent vector master.
- `01_REFERENCES/motion-reference.mp4`: 29.605 seconds at 30 fps, 1020 × 576. It informs pace, modular cards, focus shifts and progressive type, but its bright white backgrounds and green identity are not adopted.
- The uploaded ZIP contains only these three items. GamePilot QA, Mofebissyn Edutours, verified software screenshots, and other portfolio footage are not in it. Do not label invented interfaces as those projects.

## Verified local capability

HyperFrames CLI v0.8.145 is installed and previously rendered the 30-second Leon V2 film. It supports a 1080 × 1920 `portrait` resolution, a Three.js canvas updated by deterministic `hf-seek` events, GSAP timelines, snapshots, checks, and H.264/AAC renders. The current Linux environment uses software WebGL, making 4K captures slow. This 5-second prototype uses the actual Three.js/HF adapter and the same camera path intended for the full film.

## Economical sequence

1. Lock the storyboard, single dark world, and spline camera trajectory before asset generation.
2. Render the 5-second, 150-frame opening/portrait continuity prototype at 1080 × 1920 with draft encoding. Inspect 2.933s/3.000s/3.067s boundary frames and an encoded contact sheet.
3. After approval, populate only verified portfolio screens. Use user assets first; use original labeled interface studies for gaps. Source third-party footage only after recording its license and URL in `04_SOURCED_MEDIA/SOURCES.md`.
4. Expand architecture and original screen content within this same world and path. Validate short affected ranges before one complete 45-second preview.
5. Complete sound design with original/licensed music and no narration. Export a 1080 × 1920 H.264/AAC master; 2160 × 3840 is an optional later master after visual approval.

This phase stops after the prototype and review plan. The brief explicitly asks for approval before expensive full-film rendering. Model use is determined by the active Codex environment; no model switch or credit estimate is needed to create these assets.

## Quality and honesty limits

The prototype establishes camera continuity, portrait treatment, typography and architecture. It does not yet prove all 11 content galleries, realistic screen footage, final sound design, or logo assembly. The official logo is composited from supplied raster pixels; a true transparent/vector logo would improve dimensional edge work if provided later.
