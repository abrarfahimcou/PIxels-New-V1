# Pixels (Fabric 1.21.11) — by- FA. Artcell

Cyan ClickGUI (Right Shift). Tabs: Legit, Combat, Player, Render, Misc, Donut, Base, Utility, Theme.
Theme tab holds the accent colour and the Font section (shadow / bold / uppercase).

Modules so far: Sprint (Player), Fullbright (Render), Storage Scan (Base).
Add a module: new class in `module/impl`, register it in `ModuleManager.init()`.

## Build
1. Get a Fabric template for 1.21.11 from https://fabricmc.net/develop and copy its exact
   `yarn_mappings`, `loader_version`, `fabric_version`, `loom_version` into `gradle.properties`
   (the ones here are placeholders), and its `gradle/wrapper` folder + `gradlew` into this folder.
2. `./gradlew build` -> `build/libs/Pixels-1.0.0.jar` -> put in `.minecraft/mods` with Fabric API.

## If the compiler complains
This was written without being able to compile it. The 1.21.9+ input API is the most likely
place for errors: `ClickGuiScreen.mouseClicked(Click, boolean)`, and `getWindow().getHandle()` in `PixelsClient`.
