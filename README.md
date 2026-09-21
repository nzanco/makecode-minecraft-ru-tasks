# Code Builder task files in Russian

Russian task files that Minecraft Education's Code Builder opens for Neuronka's Minecraft course.
Learners never open this page: a world tells Code Builder which file to load.

## Layout

- `official/<path>.md` — Russian replacement for `Mojang/EducationContent/<path>.md`, used by
  official Minecraft Education worlds whose scripts are pointed here. The directives
  (`@codeStart`, `@codeStop`, `@flyoutOnly`) and the ghost code stay as in the original, because
  the world's scripts depend on them.
- `de/official/<path>.md` — the same file in German, for a world copy whose scripts are pointed
  at the `de/` path. Used by a cohort whose Minecraft runs in German; the block labels in the text
  are the ones the German editor shows (``||agent:Agent, bewege dich||``).
- `pxt.json` lists every file. `main.ts` stays empty.

## Links

A world points Code Builder at a file in exactly Mojang's form: one `#`, no `https://`, no tag.

`https://minecraft.makecode.com/?ipc=1&inGame=1#tutorial:github:NikolajSankovDev/makecode-minecraft-ru-tasks/official/no_coding`

The form `#tutorial:https://github.com/<repo>/<path>#<tag>` opens in a browser, but from inside the
game Code Builder shows its home screen instead (tested 2026-09-14).

Without a tag MakeCode serves the latest release. Changes on `main` reach worlds only after a new
release, so test before tagging, and never change or delete an existing tag.
