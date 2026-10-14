# One master camera trajectory

The camera is a single Three.js `PerspectiveCamera` sampled from one time-keyed cubic Hermite spline. It does not switch, teleport, or reset at phase boundaries. Shared tangent estimates at each station give C1 position/velocity continuity. A forward sample of the same curve defines the look target, so orientation follows the path and retains continuous angular motion. Small bounded roll and field-of-view changes are smooth global functions of time, not phase-local resets.

| Phase boundary | Time | Path station (approximate world position) | Tangent intent |
|---|---:|---|---|
| First spark starts | 0s | (0, 0, 8) | Into the dark corridor |
| O aperture / portrait entry | 3s | (0.5, 0.1, −13) | Continue forward, arc right |
| Portrait framing bend | 5s | (0.4, 0.15, −25) | Keep portrait and label in frame with bounded angular speed |
| Portrait / media gallery | 6s | (1.8, 0.2, −31) | Follow lit rail |
| Filmmaking / edit desk | 10s | (0.1, 0.0, −53) | Settle toward center |
| Edit / software lab | 14s | (−1.2, 0.0, −76) | Drift left |
| Software / QA | 18s | (0.4, 0.1, −99) | Pass scanner |
| QA / design | 22s | (1.6, 0.0, −121) | Arc right |
| Design / content | 26s | (0.4, 0.0, −145) | Return center |
| Content / convergence | 30s | (−0.8, 0.1, −168) | Follow chart rail |
| Convergence / logo | 35s | (0.8, 0.2, −197) | Majestic inward arc |
| Logo / contact | 40s | (0.0, 0.1, −222) | Pullback starts within the chamber |
| Final hold | 45s | (0.1, 0.0, −241) | Decelerate without cutting |

The camera path is implemented in `path.js`. The first five seconds of the final 45-second path drive the prototype, so its endpoint carries a real camera pose into future production. Tunnel ribs, rails, screen plaques, and floor geometry are placed along the same coordinate system. Phase transition objects overlap in depth; no phase-specific background replacement is needed.

Validation: sample positions, forward vectors, and speed on both sides of all ten boundaries. A transition must be rejected if screen-space motion jumps or the camera intersects unintended geometry. The prototype frames at 2.933s, 3.000s, and 3.067s are the first boundary proof.
