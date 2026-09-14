# Code Builder task files in Russian

Russian task files that Minecraft Education's Code Builder opens for Neuronka's Minecraft course.
Learners never open this page: a world tells Code Builder which file to load.

## Layout

- `official/<path>.md` — Russian replacement for `Mojang/EducationContent/<path>.md`, used by
  official Minecraft Education worlds whose scripts are pointed here. The directives
  (`@codeStart`, `@codeStop`, `@flyoutOnly`) and the ghost code stay as in the original, because
  the world's scripts depend on them.
- `pxt.json` lists every file. `main.ts` stays empty.

## Links

Worlds always point at a release tag, never at `main`:

`https://minecraft.makecode.com/?ipc=1&inGame=1#tutorial:https://github.com/NikolajSankovDev/makecode-minecraft-ru-tasks/official/no_coding#v0.1.0`

Never change or delete a tag: worlds already handed to learners point at it.
