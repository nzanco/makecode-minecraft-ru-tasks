# Rules for this repository

This repository is live delivery for Neuronka's Minecraft Education course. Code Builder inside the
game downloads these files when a learner presses C. The course-planning side lives in the private
vault (`zanco-vault`); its canonical guide is
`neuronka/operations/curriculum/_production/workflows/makecode-tutorial-production.md`, Part 7.

## What must not break

- **Worlds address files without a tag,** in Mojang's form:
  `https://minecraft.makecode.com/?ipc=1&inGame=1#tutorial:github:NikolajSankovDev/makecode-minecraft-ru-tasks/<path>`.
  From inside the game, the Arcade form with `https://github.com/` and `#<tag>` opens the MakeCode home
  screen instead (tested 2026-09-14).
- **The game loads the latest release.** Every release is live in every world at once, and `main` is
  not live until a release is made.
- **Moving or renaming a file breaks every world that points at it.** Add a new path instead.
- **Every Markdown file is listed in `pxt.json`.** `main.ts` stays empty.

## Editing an `official/` file

`official/<path>.md` replaces `Mojang/EducationContent/<path>.md` for a world whose scripts were
retargeted here.

- Keep every `###` directive. The world reads the scoreboard that `@codeStart` / `@codeStop` set to
  decide whether a task counts, and `@flyoutOnly` restricts the toolbox.
- Keep the `ghost` code; change only the chat word to the course's word.
- Write Russian text for a child of 8–10: numbered steps, «ты», gender-neutral wording, block
  references with the label the Russian editor shows (``||agent:агент: переместиться||``).
- Add a `template` only where the workspace should be replaced when the tutorial opens.

## Releasing

1. Commit.
2. Tag the next version (`v0.x.y`) and create a GitHub release.
3. Browser pre-check:
   `https://minecraft.makecode.com/?ipc=1&inGame=1&noRunOnX=1#tutorial:github:NikolajSankovDev/makecode-minecraft-ru-tasks/<path>`.
4. Check in the game, starting from a fresh import of the world. The first C after an import is slow.

Never change or delete an existing tag.
