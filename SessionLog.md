# Session Log

## Current state

Single-file `index.html`, no build step, target deploy `roomies.kibera.com`. Stage 1 (skeleton + setup screen) is complete. Stages 2–5 are pending (house schematics, pointer drag/drop, polish).

## Stage plan

1. **Skeleton** — repo scaffolding, setup overlay with full configuration cards, play-screen shell. DONE.
2. **Setup screen** — (merged into stage 1 per plan). DONE.
3. **House schematic SVG cards** — render each house as a floor-plan grid with bedroom slots. Pending.
4. **Pointer-based drag/drop with validation** — drag kids and au pairs into bedroom slots; enforce capacity and au-pair-per-house rules. Pending.
5. **Polish + printable summary + confetti** — celebration screen, print stylesheet, final visual pass. Pending.

## Conventions

- Single `index.html`, no build step, no dependencies besides CDN scripts.
- Commit messages via heredoc with `Co-Authored-By: Claude` trailer.
- Deploy via direct push to `main`; GitHub Pages serves from root.
- Hard-refresh (`Cmd+Shift+R`) after each deploy to clear the cache.

## Design decisions (this stage)

- Emoji avatars for kids and au pairs (24-emoji palette defined in JS const).
- Responsive CSS grid planned for house schematics (deferred to stage 3).
- Pointer-based drag/drop deferred to stage 4.
- canvas-confetti celebration deferred to stage 5.
- Single parchment palette only — no blue/jade body[data-palette] variants (simpler than mapgame).
- localStorage key: `rm_setup_v1`.
- Auto-generated subtitle joins kid names with Oxford comma; falls back to au pair names if no kids.
