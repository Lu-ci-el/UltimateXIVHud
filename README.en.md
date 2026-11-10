# UltimateXIVHud (UXHD) 0.4.9.6

[日本語](README.md)

Use UXHD to keep GShade out of FFXIV footage shared through OBS, Discord or Discord PTB. GShade remains visible on your own game screen, while the game's normal HUD remains in the shared image.

## Download and requirements

[Download the latest version](https://github.com/Lu-ci-el/UltimateXIVHud/releases/latest)

Requires Windows x64, DirectX 11 FFXIV, and .NET 8 Desktop Runtime (x64).

This public build is for FFXIV patch 7.58. It will stop working after an FFXIV update.

## Getting started

1. Extract the entire ZIP into a writable folder of your choice.
2. **Run UXHD as administrator.**
3. Whenever possible, start **UXHD → FFXIV → Discord / Discord PTB**, wait for UXHD to connect, and then begin sharing. The stream appeared sooner in this order during testing of version 0.4.9.1.
4. **Selecting FFXIV directly as the Discord sharing target also lets you share game audio.** In OBS, select FFXIV in Game Capture. **OBS may be started in either order.**
5. Check both the preview and the actual stream to confirm that viewers see the intended image.

If you start UXHD after sharing has already begun, the previously acquired image may not switch. **You may need to stop and restart the share.** The image can turn black while a clean frame is being prepared and return afterwards. Recovery time is not guaranteed.

Use **日本語 / English** at the top of the window to change the language.

Two optional settings are available (both default to off):

- **Start automatically with Windows**: starts UXHD with administrator rights when you log on. Run UXHD as administrator to enable or disable this setting.
- **Start in the system tray**: starts with the window in the tray. Double-click the tray icon to restore it.

Minimize-to-tray and a user-defined show/hide shortcut are also available.

When switching to a newer version in another folder, turn automatic startup off and on in the new version to update the registered path. Extract the whole new ZIP into a separate folder. Do not run from inside the ZIP or mix files from different versions.

## Tested scope and streaming

Version 0.4.9.6 was checked offline against the patch 7.58 game files. **In-game operation and streaming on 7.58 have not yet been tested.** GShade was confirmed absent from Discord and Discord PTB streams during testing of version 0.4.9.1.

**Please use and stream at your own risk.** Behavior can vary with the environment and startup order. Check the preview and an actual stream before broadcasting. UXHD covers OBS Game Capture and Discord / Discord PTB sharing; desktop-wide capture is outside its scope.

## Report a problem

[Report a bug](https://github.com/Lu-ci-el/UltimateXIVHud/issues/new?template=bug_report_en.yml)

Include the app version, environment, startup order, reproduction steps and symptoms. Remove personal information and credentials from attachments. Whether an issue is addressed depends on the support received; fixes and response times are not guaranteed.

## Support development

If UXHD is useful to you, please consider supporting it through Ko-fi. Support is optional.

[Ko-fi](https://ko-fi.com/lost2)

## Credits

- MASTER: 𓆩†𓆪 Luciel 𓆩†𓆪
- DESIGNER: 𓆩✦𓆪 ASTER 𓆩✦𓆪
- DEVELOPER: 𓆩⚔𓆪 FABER 𓆩⚔𓆪
