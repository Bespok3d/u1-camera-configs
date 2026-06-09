# u1-camera-configs

A co-repo of Bespok3d plugins for the Snapmaker U1 that publishes its own sub-list.

Plugins:

- **webcam-builtin** - Show the built-in MIPI camera in Fluidd & Mainsail.
- **webcam-screen** - Show the on-device touchscreen as a camera tile in Fluidd & Mainsail.
- **webcam-usb** - Show the external USB camera in Fluidd & Mainsail.

## Layout

```text
u1-camera-configs/
  <plugin-id>/          # one plugin = one dir; its name is the manifest .name
    manifest.json
    files/              # payload the daemon places on the printer
    doc/README.md       # rendered in-app; not deployed
  scripts/{pack.sh,generate-atom.mjs,assemble-list.mjs}
  .github/workflows/release.yml
  index.json            # the published sub-list (committed; referenced by main-index lists[])
  dist/                 # build output (gitignored)
```

Each plugin declares WHAT (a destination `class` + a `restart` hook), never a path or a raw
command; the printer-side adapter realizes it. See `Bespok3d/doc/anatomy-of-a-plugin.md`.

## Build locally

```sh
sh scripts/pack.sh                            # -> dist/<name>-<ver>.b3 per plugin
node scripts/generate-atom.mjs --plugin <id>  # -> dist/<id>.atom.json
node scripts/assemble-list.mjs                # -> index.json from dist/*.atom.json
```

## Releasing

Bump a plugin's `manifest.json` `version` and push to `main`. CI packs each `.b3`, cuts a release
per plugin, regenerates this repo's `index.json` sub-list, and registers it in `Bespok3d/main-index`
(`lists/<repo>.json`). Secret: `MAIN_INDEX_TOKEN` (contents:write on main-index). Signing deferred.
## Maintainership

These plugins are published and maintained by the Bespok3d org, and several of them repackage or
build on upstream source material. If you own the source material a plugin is based on and would
rather manage it yourself, you are welcome to contact the org to claim it back. The one condition is
that it stays actively maintained: a claimed plugin left to rot will be reclaimed so users are never
stranded on an abandoned package.
