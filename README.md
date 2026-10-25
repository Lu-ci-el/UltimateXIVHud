# UltimateXIVHud (UXHD)

[日本語の説明書](README.ja.md)

UltimateXIVHud helps you share FINAL FANTASY XIV through OBS and Discord while keeping supported third-party overlays out of the captured image. Your own game view keeps those overlays, and the game's normal HUD remains in the shared image.

## Download

[Download Release 0.4.5.6](https://github.com/Lu-ci-el/UltimateXIVHud/releases/download/v0.4.5.6/UltimateXIVHud_0.4.5.6.zip) · [Release page](https://github.com/Lu-ci-el/UltimateXIVHud/releases/tag/v0.4.5.6)

## What it does

UXHD supplies a clean game image to these five output paths:

| Application | Output |
| --- | --- |
| OBS Studio | Game Capture |
| Discord | Screen-share preview |
| Discord | Live screen share |
| Discord PTB | Screen-share preview |
| Discord PTB | Live screen share |

The capture paths handle supported Minion and Dalamud overlays. UXHD has connection paths for environments with and without GShade. Compatibility depends on the game, overlay and capture application versions; check the actual preview and stream before using a new combination. A connection indicator alone does not confirm what viewers see.

UXHD does not hide the entire FFXIV HUD. Desktop-wide capture and capture applications outside the list above are not covered by these five paths.

## Requirements

- Windows x64, the DirectX 11 version of FFXIV, and the .NET 8 Desktop Runtime (x64).
- The full Release package, extracted together into one folder.
- This build uses `G:\Documents\FFXIV\UXHD` for settings and runtime data. That drive and folder must be available and writable.

Do not run the executable directly from the ZIP. Keep the included DLLs, runtime files, `release.manifest.json` and `release.manifest.sig` together. UXHD checks its release signature and file hashes at startup.

## Getting started

1. Extract `UltimateXIVHud_0.4.5.6.zip` and run `UltimateXIVHud.exe`.
2. Start FFXIV, or leave your already running game open. UXHD detects the game and checks its build and startup stability automatically. You can also start UXHD after the game.
3. Wait for the FF14 connection indicator. A new game build takes longer because UXHD performs additional checks before enabling capture hooks.
4. Select FFXIV in OBS Game Capture or in the game/window sharing controls of Discord or Discord PTB.
5. Check both the preview and the actual output. Confirm that the overlays you want to exclude are absent and the normal game image is present.

Release connects automatically. The language selector does not reconnect the game or restart capture. Only one UXHD application instance can run at a time.

## Language and settings

Use the **日本語 / English** selector at the top of the window. The Release interface switches immediately and remembers your choice for the next launch. Japanese is the default.

The setting is saved in:

```text
G:\Documents\FFXIV\UXHD\MainCore\Settings\release_ui.json
```

The Settings page displays the application name, version, credits and three links: **Support (お布施)**, **Ko-fi**, and **GitHub**. Donations are optional. GitHub opens this application's repository.

The language selector is available in Release only. Developer tools and diagnostics belong to the separate Debug build.

## Connection states

| State | Meaning |
| --- | --- |
| Waiting | The game, application or capture path is not ready yet. |
| Found | UXHD detected it; capture readiness has not yet been confirmed. |
| Absent (GShade) | GShade is not loaded. GShade is optional. |
| Active / Ready | The corresponding connection or protection state is active. Verify the actual captured image too. |
| Off | A previously observed connection has ended. |
| Warning / Stopped / Quarantined | A connection or compatibility check needs attention. Read the detail shown in the window. |
| Restart required | UXHD requests a fresh FFXIV process before retrying. Restart the game yourself when convenient. |

If the game is waiting, let startup finish. If a warning remains, retain its exact text and the logs under `G:\Documents\FFXIV\UXHD\MainCore\Logs`. If the signature check fails, extract a complete original Release package again. Keep individual files from different versions separate.

## Changes in 0.4.5.6

- Keeps the recent capture performance improvements.
- Fixes black previews when the source image briefly stops updating.
- Automatically connects when UXHD is started after FFXIV.

Performance depends on your environment and capture settings; no fixed in-game FPS is guaranteed.

## Credits and links

| Role | Name |
| --- | --- |
| MASTER | 𓆩†𓆪 𝕷𝖚𝖈𝖎𝖊𝖑 𓆩†𓆪 |
| DESIGNER | 𓆩✦𓆪 ASTER 𓆩✦𓆪 |
| DEVELOPER | 𓆩⚔𓆪 FABER 𓆩⚔𓆪 |

[Support / お布施](https://ofuse.me/lost) · [Ko-fi](https://ko-fi.com/lost2) · [GitHub](https://github.com/Lu-ci-el/UltimateXIVHud)
