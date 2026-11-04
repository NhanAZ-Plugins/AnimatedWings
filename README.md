# animated-Wings

Custom wing skin menu for Axolotl-PM API 5, authored by NhanAZ and licensed under MIT

[![CI](https://github.com/NhanAZ-Plugins/animated-Wings/actions/workflows/build.yml/badge.svg)](https://github.com/NhanAZ-Plugins/animated-Wings/actions/workflows/build.yml)
[![Latest release](https://img.shields.io/github/v/release/NhanAZ-Plugins/animated-Wings)](https://github.com/NhanAZ-Plugins/animated-Wings/releases/latest)
[![License](https://img.shields.io/github/license/NhanAZ-Plugins/animated-Wings)](https://github.com/NhanAZ-Plugins/animated-Wings/blob/main/LICENSE)
[![Discord](https://img.shields.io/discord/986553214889517088?label=Discord&logo=discord&logoColor=white&color=5865F2)](https://discord.gg/j2X83ujT6c)

## Overview

This plugin targets the PocketMine-MP and Axolotl-PM API 5 ecosystem and is maintained under [NhanAZ-Plugins](https://github.com/NhanAZ-Plugins).

## Compatibility

- Minimum Axolotl-PM API: `5.0.0`.
- The plugin uses Axolotl-PM's built-in form API and does not require FormAPI.
- The pinned CI matrix checks API 5.0.0 and 5.51.1 source revisions. This does not establish compatibility with every API 5.x release.
- The plugin requires PHP's GD extension to process player skin images.

## Player skin data

The plugin saves a copy of a player's login skin so it can apply and reset wing overlays. New player skin files use a SHA-256-derived filename rather than a client-provided name. The new-install default `DeleteSkinAfterQuitting: true` removes that saved skin when the player leaves; an existing server's explicit configuration is preserved. Invalid or unsupported skin payloads are rejected before image conversion. Temporary composite images use unique files and are removed after use.

These files still contain player appearance data while present. Protect the plugin data directory and review the retention setting for the server. Historical saves created by older versions with raw player-name filenames are not renamed or deleted automatically.

## Bundled asset status

The bundled wing PNG and geometry assets are authored by NhanAZ and distributed under the MIT License. The GitHub Actions workflow checks PHPStan, API 5 PHAR builds, artifact contents and plugin startup.
