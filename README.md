## Borg-themed Codex Pet

This repository contains a custom pet package for the Codex app. It is not an official OpenAI Codex pet. Official pets live in Codex Settings > Appearance > Pets; this package is a community-made custom pet that you can install locally. Resistance is futile.

## Files

```text
<pet-slug>/
  pet.json
  spritesheet.webp
```

`pet.json` describes the pet, and `spritesheet.webp` contains the animation atlas used by Codex.

## Install

1. Download or clone this repository.
2. Copy the pet folder into your local Codex pets directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/pets"
cp -R ./<pet-slug> "${CODEX_HOME:-$HOME/.codex}/pets/<pet-slug>"
```

3. Restart Codex.
4. Open Codex Settings > Appearance > Pets and select the custom pet.

## Expected Package Shape

The installed folder should look like this:

```text
${CODEX_HOME:-$HOME/.codex}/pets/<pet-slug>/
  pet.json
  spritesheet.webp
```

The manifest should reference the spritesheet by relative path:

```json
{
  "id": "<pet-slug>",
  "displayName": "<Pet Name>",
  "description": "<One short sentence about the pet.>",
  "spritesheetPath": "spritesheet.webp"
}
```

## Compatibility

This pet uses the custom Codex pet package format: a `pet.json` manifest plus a transparent animated `spritesheet.webp` atlas.
