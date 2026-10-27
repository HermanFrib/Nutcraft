# Nutcraft

Personal Minecraft resource pack (MC 26.3). This repo hosts the packaged zip
that the server serves as its resource pack.

## GitHub accounts — never mix

- Minecraft work is personal. Only use repos owned by **HermanFrib**.
- Never attach, read, or push to `herman-Saurus` or `zdk-labs` repos from
  Minecraft work. Those are work repos.

## Source of the pack

The pack source lives on Herman's PC (Prism Launcher instance), not in this repo:

`E:\MinecraftPrismlauncher\Instances\26.3\minecraft\resourcepacks\Nutcraft\`

## Building `Nutcraft.zip`

- `pack.mcmeta`, `pack.png` and `assets/` must be at the **zip root**, not
  nested inside a `Nutcraft/` folder.
- Exclude: any `Nutcraft.zip` inside the source folder, `backup_*` folders,
  and unused files (e.g. old `optifine/cem/skeleton*` files,
  `textures/entity/skeleton/horseman_cape.png`,
  `textures/item/horseman_head_face.png`).
- Commit the zip as `Nutcraft.zip` at the repo root on `main`.

## Serving it

- URL: `https://github.com/HermanFrib/nutcraft/raw/main/Nutcraft.zip`
- After every upload, compute the SHA-1 of the uploaded zip (download it back
  and hash it) and give it to Herman for `resource-pack-sha1=` in
  `server.properties`. The SHA-1 changes every time the zip changes.
