# Join the Beacons — game design, version 0.2

## Pitch
Rotate path tiles to carry light between two beacons on opposite board edges. A calm, readable puzzle for a 30–90 second session. Desktop mouse, keyboard and touch use the same controls.

## Core rules
- A 5 × 5 board contains straight, corner and three-way path tiles.
- Tap any movable tile to rotate it 90° clockwise. Start and goal beacon tiles do not rotate.
- Connected path segments glow. The level ends once light can reach the goal beacon.
- There is no timer or lives; a reset button restores the board and a hint identifies a tile on the intended path.
- Levels are deterministic and completable; rotating the intended path to its stored solution always wins.

## Progression and content
Twelve handcrafted beacon-to-beacon routes. The first is a straight introduction; later routes bend back, overlap nearby decoys, and use longer paths. Completing the last level offers replay. Save stores level and current board rotations; a score reports completed level. No accounts, purchases, sharing prompts or external links.

## Visual and sound direction
Midnight blue tiles with amber light and large, clearly marked start and goal beacons. Connected tiles illuminate immediately. The prototype uses SVG vector paths and CSS, so there are no image downloads. Sound is omitted in version 0.1; if added, it must obey the YouTube sound controls.

## Interface
Responsive centered square board with legible heading, progress indicator, clear instruction, reset/hint controls, and completion overlay. It does not force orientation. Tile labels support keyboard navigation and screen readers.

## Implementation and release
Single HTML5 file with the YouTube SDK loaded before game code. The game calls firstFrameReady and gameReady; uses cloud save and score when in YouTube; local browser uses localStorage for testing. Relative resources only. ZIP contains index.html at root. Test with YouTube's Playables test suite and on desktop, mobile web, Android and iOS once Developer Portal access is available. Portal participation currently requires an invitation and an onboarded channel with suitable permissions. Upload metadata, thumbnails and ZIP, create release, verify and submit for certification.

## Prototype limits and next pass
The twelve boards use simple generated decoy tiles and the first generated solution is not guaranteed unique or minimal. User playtesting should determine the difficulty curve and whether hints should rotate one tile instead of pointing to it. Before release, add suitable thumbnails, test actual YouTube SDK behavior, review localization and accessibility, and complete the platform certification suite.
