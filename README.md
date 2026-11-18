# RMK firmware project template

Fork this repository to build [RMK](https://github.com/HaoboGu/rmk) keyboard firmware in the cloud — no local Rust toolchain required.

## Use it

1. Click **Use this template → Create a new repository**.
2. Edit `keyboard.toml` (your keyboard's layout, pins, and enabled features) and `vial.json` (the Vial matrix definition). See the [configuration guide](https://rmk.rs/docs/configuration.html).
3. Commit. GitHub Actions builds your firmware automatically.
4. Open the **Actions** tab and download the compiled firmware from the run's **Artifacts** (`.uf2`, `.hex`, or `.bin`).

A build runs on every push that changes `keyboard.toml` or `vial.json`.

## Choose the RMK version

By default the firmware builds against RMK's `main`. To pin a released version, run the workflow manually: **Actions → Build RMK firmware → Run workflow**, and set **rmk_version** to a version listed in [`version-mapping.json`](https://github.com/HaoboGu/rmk-template/blob/main/version-mapping.json) (e.g. `0.8`).

> The feature set is derived from `keyboard.toml`. Pinning an older `rmk_version` may not match the current config schema, so `main`/`latest` is the supported combination.
