# Wallkick

Vertical arcade climber for phones. Kick between walls, hop floating platforms, and stay ahead of the rising edge of the screen. Height is score.

- Single file, no dependencies: `index.html`.
- Controls: hold the left or right half of the screen and let go to jump that way. On a wall, tapping toward the wall hops straight up it (once per wall contact) to line up a kick across. A tap is a small hop; holding longer (up to ~0.4 s) charges a bigger jump, shown by the meter over the climber. On a wall, either side kicks off. Hold a side in the air to steer. Keyboard: arrows / A-D / Space (hold and release), P to pause.
- Endless procedural tower: wall shafts, platform fields, and one-wall hybrids. Biomes change with height: Downtown, Canopy (150 m), Red Canyon (350 m), Glacier (600 m), Cloud Kingdom (900 m), Aurora (1300 m), Low Orbit (1800 m), The Beyond (2600 m).
- Platform types: normal, moving, crumbling, spring, ice. Red spike strips on walls knock you off.
- Coins: gold coins (1) sit in shafts, over platforms, along jump paths and up spring launches; gems (5) sit next to spike strips and on side platforms. Run count shows in the HUD; a lifetime total is saved. Height stays the score.

## Releasing

Run `node bump-version.js` before committing. It stamps a new build number into `index.html` and `version.json`. Open copies of the game compare their embedded build to the deployed `version.json` and show a "Tap to reload" toast when a newer build is live. If you commit without bumping, players are not notified.

## Hosting

GitHub Pages: Settings > Pages > Deploy from branch > `main` / root.
