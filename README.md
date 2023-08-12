# Mouse Injector for Dolphin 5.0, DuckStation, PCSX2, and other emulators

An external app that injects cursor input into game memory.

### *If you have a game request, please go to the 'Discussions' tab and post it!*
### _Scroll to bottom for_ <font color="red"> *FREQUENTLY ASKED QUESTIONS* </font>


## Supported Emulators
| Emulator/Frontend | Version | Executable name (case sensitive) |
| --- | :---: | :---: |
| Dolphin | 5.0 and up | dolphin.exe |
| DuckStation | 0.1-5485 | duckstation-qt-x64-ReleaseLTCG.exe |
| PCSX2 Nightly | latest | pcsx2-qt.exe<br>pcsx2-qtx64.exe<br>pcsx2-qtx64-avx2.exe |
| RetroArch (see cores below) | 1.14.0 | retroarch.exe |
| PPSSPP | 1.14.4 | PPSSPPWindows.exe / PPSSPPWindows64.exe |
* NOTE: Versions given are the latest that have been tested working, may work with newer
* NOTE: PCSX2 will only hook with **BIOS versions 5XXXX and up**.

## Supported RetroArch Cores
| Console | Core | Version |
| :---: | :---: | :---: |
| N64 | Mupen64Plus-Next | 2.4-Vulkan bc24153 |
| PS1 | Beetle PSX HW | 0.9.44.1 234433f |
| PS1 | Beetle PSX | 0.9.44.1 6ed5790 |
| PS1 | PCSX-ReARMed | r23l 4373e29 |
| PS1 | DuckStation | |
| PS1 | SwanStation | 1.00 bc5f6c8 |
| SNES | bsnes-mercury Balanced | v094 |
* NOTE: For RetroArch the window needs to be focused for it to hook initially.
* NOTE: All cores have not been tested exhaustively

## How to Use
1. Start emulator first
2. Start MouseInjector, read initial information then press ctrl+1
3. Make sure game is running and press '4' to hook into the process
    1. If game is supported then the mouse will be captured at the position it was at when hooked
        * You will be <b><u>unable</u></b> to use the mouse elsewhere while it is hooked, press 4 to unhook
        * Some games depend on post startup values/addresses so hook may not happen immediately
            * DuckStation games usually will not hook until after the startup sequence
    2. Unsupported/broken games will not hook and mouse won't be captured
4. Adjust options with numbers 4-7 while in-game, ctrl+0 will lock the settings
* NOTE: The cursor still moves but gets moved back to it's initial hook position so windowed mode may not
work very well if you have also mapped the mouse buttons as you may click off the window. Fullscreen is
recommended and with dual-monitors it is recommended to put the cursor in the corner before hooking to
avoid clicking off the window.

## Supported Dolphin Titles (NTSC Only)
| Game Title | Mouse Support | Issues |
| --- | :---: | ----------- |
| 007: NightFire | Poor | <sup>Vehicle mode is semi-functional - last level is broken</sub> |
| Call of Duty 2: Big Red One | Good | <sup>None</sub> |
| Die Hard: Vendetta | Fair | <sup>Sentry mode not supported</sub> |
| Geist | Fair | <sup> ** *Requires MMU be disabled for game in Dolphin* ** <br />Camera broken on elevators, truck sentry on motorcycle level broken</sub> |
| Medal of Honor: European Assault | Good | <sup>None</sub> |
| Medal of Honor: Frontline | Fair | <sup>Minecart level is broken</sub> |
| Medal of Honor: Rising Sun | Poor | <sup>Looking down scope while in turret mode is broken</sub> |
| Metal Arms | Good | <sup>Rat driving or rat turret may not work correctly<sup> |
| Serious Sam: Next Encounter | Fair | <sup>Vehicle/submarine interfaces are not supported</sub> |
| TimeSplitters 2 | Fair | <sup>Camera/sentry modes not supported</sub> |
| TimeSplitters: Future Perfect | Poor | <sup>All non-first person modes are not supported</sub> |
| Trigger Man | Good | <sup>None</sub> |
| Turok: Evolution | Good | <sup>Optional cheats/patches in **'cheats/TurokEvolutionGTKE51.txt'**</sub> |

## Supported PS1 Titles
| Game Title | Serial | Mouse Support | Issues | In-game Options | Cheat/Patch File |
| --- | --- | :---: | :-----------: | :---: | :---: |
| 007: The World Is Not Enough (USA) | SLUS-01272 | Fair | <sup>Requires patch be applied to disc image (**See below**)</br>No clamp on lean aiming</br>Not fully tested</sub> | <sup>Auto Assist: Off</sub> | **007TWINE_SLUS-01272_patch.xdelta** |
| Alien Trilogy (USA) | SLUS-00007 | Good | <sup>Requires supplied cheat file</br>Not fully tested</sub> | - | **AlienTrilogy_SLUS-00007.cht** |
| Aquanaut's Holiday (USA) | SCUS-94603 | Good | <sup>Requires supplied cheat file</br>Very little testing</sub> | - | **AquanautsHoliday_SCUS-94603.cht** |
| Armored Core (USA) | SCUS-94182 / SLUS-01323 | Fair | <sup>VS Mode not supported</br>Not fully tested</sub> | - | - |
| Armorines: Project S.W.A.R.M. (USA) | SLUS-01022 | Fair | <sup>Not fully tested</sub> | <sup>Look Spring: Off</br>Auto Aim: Off</sub> | - |
| Baroque - Yuganda Mousou (Japan) | SLPM-86328 | Fair | <sup>Supplied cheat required to prevent camera y-axis from being reset on hit</br>Not fully tested</sub> | - | **Baroque_SLPM-86328.cht** |
| Brahma Force: The Assault on Beltlogger 9 (USA) | SLUS-00444 | Good | <sup>Not fully tested</sub> | - | - |
| Codename: Tenka (USA) | SCUS-94409 | Fair | <sup>Strafe/Lean must be set to R2 in-game for strafe to work without holding the button</sub> | - | - |
| Delta Force: Urban Warfare (USA) | SLUS-01429 | Good | <sup>Not fully tested</sub> | <sup>Aiming Mode: Manual</br>Auto Center: Off</sub> | - |
| Disruptor (USA) | SLUS-00224 | Good | <sup>Requires supplied cheat file</br>Not fully tested</sub> | - | **Disruptor_SLUS-00224.cht** |
| Duke Nukem: Time to Kill (USA) | SLUS-00583 | Fair | <sup>Requires supplied cheat file</br>Not fully tested</sub> | - | **DukeNukemTimeToKill_SLUS-00583.cht** |
| Echo Night (USA) | SLUS-00820 | Good | <sup>Not fully tested</sub> | - | - |
| Future Cop: L.A.P.D. (USA) | SLUS-00739 | Fair | <sup>Not fully tested</sub> | - | - |
| G-Police (USA) | SLUS_005.44/SLUS_005.56 | Good | <sup>Not full tested</sub> | - | - |
| Hellnight (Europe) | SLES-01562 | Good | <sup>Requires supplied cheat file</br>Not fully tested</sub> | - | **Hellnight_SLES-10562.cht** |
| Hybrid (Japan, Europe) | SLPS-01102, SLES-03531 | Fair | <sup>Requires supplied cheat file<br>Not fully tested</sub> | - | **Hybrid_SLPS-01102.cht (Japan)<br>Hybrid_SLES-03531.cht (Europe)** |
| Iron Soldier 3 (USA) | SLUS-01061 | Good | <sup>Advanced Controls not supported</br>Requires supplied cheat file</br>Not fully tested</sub> | - | **IronSoldier3_SLUS-01061.cht** |
| Jumping Flash (USA) | SCUS-94103 | Good | <sup>Requires supplied cheat file</sub> | - | **JumpingFlash_SCUS-94103.cht** |
| King's Field (II) (USA) | SLUS-00158 | Good | <sup>Not fully tested</sub> | - | - |
| King's Field (Japan) | SLPS-00017 | Good | <sup>Not fully tested, Will not hook until in-game</sub> | - | - |
| King's Field II (III) (USA) | SLUS-00255 | Good | <sup>Not fully tested</sub> | - | - |
| LSD: Dream Emulator (Japan) | SLPS-01556 | Good | <sup>Requires supplied cheat file</br>Not fully tested</sub> | - | **LSDDreamEmulator_SLPS-01556.cht** |
| Medal of Honor: Underground (USA) | SLUS-01270 | Fair | <sup>Machine Gun sentry doesn't always work (depends on objects in line of sight). Sidecar gun in 6-3 not supported. Precise aim not supported (holding trigger aiming). Controller type must be Analog/DualShock or else auto-center will be enabled. </sub> | - | - |
| Men in Black: The Series - Crashdown (NTSC) | SLUS-01387 | Good | <sup>None</sub> | <sup>Auto Aim: Off</sub> | - |
| Note, The (Europe) | SLES-00749 | Good | <sup>Not fully tested</sub> | - | - |
| Powerslave (USA) | SLUS-00102 | Good | <sup>Requires supplied cheat file</br>Not fully tested</sub> | - | **Powerslave_SLUS-00102.cht** |
| Resident Evil: Survivor (USA) | SLUS-01087 | Good | <sup>None</sub> | - | - |
| Revolution X (USA) | SLUS-00012 | Good | <sup>None</sub> | - | - |
| Shadow Tower (USA) | SLUS-00863 | Good | <sup>Not fully tested</sub> | - | - |
| South Park (USA) | SLUS-00936 | Good | <sup>Supplied cheats recommended</br>Not fully tested</sub> | - | **SouthPark_SLUS-00936.cht** |
| Uprising X (USA) | SLUS-00686 | Fair | <sup>None</sub> | - | - |
* NOTE: If DuckStation is not hooking, try restoring the default settings. 'Settings->General->Restore Defaults'
* Importing cheat files in DuckStation: 'Tools->Cheat Manager->Cheat List->Import->From File'

## How to apply patch to PS1 game
* Download and run **xdelta UI**
* Select 'Apply Patch' tab
* For 'Patch' select the provided '.xdelta' patch file for the intended game
* For 'Source File' select the game's '.bin' file
* 'Output File' should have a different name to original
    * Original: *007 The World Is Not Enough (USA).bin*
    * Patched: *007 The World Is Not Enough (USA) (MouseInjector).bin*
* Click 'Patch' and wait until the patch is successful
* Copy original game's '.cue' file to same directory as patched '.bin'
* Rename copied '.cue' to match patched '.bin'
    * Patched bin: *007 The World Is Not Enough (USA) (MouseInjector).bin*
    * Patched cue: *007 The World Is Not Enough (USA) (MouseInjector).cue*
* Open '.cue' file in a text editor and change first line to match patched file
    * *FILE "007 The World Is Not Enough (USA) (MouseInjector).bin" BINARY"*

## Supported Mupen64Plus(RetroArch)
| Game Title | Mouse Support | Issues |
| --- | :---: | ----------- |
| GoldenEye: 007 (NTSC) | Fair | <sup>None</sub> |
| Sin and Punishment (J) | Good | <sup>Not fully tested</sub> |

## Supported SNES Titles
| Game Title | Mouse Support | Issues |
| --- | :---: | ----------- |
| Pac-Man 2: The New Adventures (USA) | Good | <sup>Not fully tested</sub> |
| R-Type III: The Third Lightning (USA) | Good | <sup>Not fully tested</sub> |
| Timon & Pumbaa's Jungle Games (USA) | Good | <sup>None</sub> |
| Untouchables, The (USA) | Good | <sup>Crosshair shooting sections only</sub> |
| Wild Guns (USA) | Good | <sup>Recommended use of supplied patch to disable cursor movement when moving character (Disables x-axis cursor movement for both players)</sub> |
* NOTE: Patches must either be applied with an IPS patching tool, such as Lunar IPS, or by using softpatching with RetroArch

## Supported PCSX2 Titles
| Game Title | Serial | Mouse Support | Issues | In-game Options | Cheat File |
| ---------- | :----: | :-----------: | :----: | :-------------: | :--------: |
| 007: Agent Under Fire (USA) | SLUS-20265 | Good | <sup>Mouse movement warps camera while paused and during in-game cutscenes</br>Aim-lock not disabled on auto-scroller levels</sub> | - | - |
| 50 Cent: Bulletproof (USA) | SLUS-21315 | Good | <sup>Not fully tested</sub> | <sup>Camera->Aim Assist: Off</sub> | - |
| Armored Core 2 (USA) | SLUS-20014 | Good | <sup>Arena replays broken</br>Not fully tested</sub> | - | - |
| Beverly Hills Cop (PAL) | SLES-54456 | Fair | <sup>Not fully tested</sub> | - | - |
| Black (USA) | SLUS-21376 | Good | <sup>Not fully tested</sub> | - | - |
| Call of Duty 3 (USA) | SLUS-21426 | Good | <sup>3rd-Person Jeep camera not supported</br>Not fully tested</sub> | - | - |
| Call of Duty: Finest Hour (USA) | SLUS-20725 | Good | <sup>None</sub> | <sup>Aim Assist: Off</sub> | - |
| Cold Winter (USA) | SLUS-20845 | Good | <sup>Split-screen mode not supported</sub> | <sup>Profile options - Aim Assist: Off</sub> | - |
| Darkwatch (USA) | SLUS-21043 | Good | <sup>**Requires supplied cheat file**</br>Horse aiming is not quite right but is usable.</sub> | - | **327052E8.pnach** |
| Eternal Ring (USA) | SLUS-20015 | Good | <sup>Not fully tested</sub> | - | - |
| Ghost in the Shell: Stand Alone Complex (USA) | SLUS-21006 | Fair | <sup>Horizontal camera while climbing not clamped</sub> | - | - |
| Global Defence Force (PAL) / Chikyū Bōeigun 2 (Japan) | SLES-54464, SLPM-62652 | Good | <sup>Vehicle mouse control is experimental</br>Not fully tested</sub> | <sup>Control Type: Technical</sub> | - |
| Gunslinger Girl Vol. 1 (Japan)| SLPS-25343 | Fair | <sup>Not fully tested</sub> | - | - |
| Jurassic: The Hunted (USA) | SLUS-21907 | Good | <sup>**Requires supplied cheat file**</br>Optional 60FPS cheat recommended</sub> | <sup>Aim Assist: Off</sub> | **EFE4448F.pnach** |
| King's Field IV: The Ancient City (USA) | SLUS-20318 | Good | <sup>Not fully tested</sub> | - | - |
| Medal of Honor: Vanguard (USA) | SLUS-21597 | Good | <sup>Multiplayer mode not supported</sub> | - | - |
| Mercenaries: Playground of Destruction (USA) | SLUS-20932 | Fair | <sup>**Requires cheat file to disable aim-assist**</br> X-axis in normal vehicles not supported</sub> | - | **23510F99.pnach** |
| Michigan: Report from Hell (Europe) | SLES-53073 | Fair | <sup>Door peek camera not supported</br>Not fully tested</sub> | - | - |
| Monster Attack (PAL) / Chikyū Bōeigun (Japan) | SLES-51856, SLPM-62344 | Good | <sup>Vehicle mouse control is experimental</br>Not fully tested</sub> | <sup>Control Type: Technical</sub> | - |
| Ninja Assault (USA) | SLUS-20492 | Good | <sup>**Requires supplied cheat file to disable aim-lock**</br>Not fully tested</sub> | - | **785B28DA.pnach** |
| No One Lives Forever (USA) | SLUS-20028 | Good | <sup>Not fully tested</sub> | <sup>Auto-targeting: Off</sub> | - |
| Quake III: Revolution (USA) | SLUS-20167 | Good | <sup>None</sub> | <sup>Auto Center: No <br> Auto Aiming: No (only available from main menu options) | - |
| Red Dead Revolver (USA) | SLUS-20500 | Fair | <sup>Gatling guns and final scene may break if game is loaded from memory card after a shutdown.  **Fix below**</sub> | <sup>Target Mode: Toggle</sub> | - |
| Resident Evil: Dead Aim (USA) | SLUS-20669 | Good | <sup>**Requires supplied cheat file**</br>Third-person camera y-axis not supported</sub> | - | **FBB5290C.pnach** |
| Return to Castle Wolfenstein: Operation Resurrection (USA) | SLUS-20297 | Good | <sup>Not fully tested</sub> | <sup>Auto Center View: Off</br>Always Aim: Off</sub> | - |
| Robotech: Invasion (USA) | SLUS-20823 | Fair | <sup>Turrets not supported</br>Not fully tested</sub> | - | - |
| SOCOM U.S. Navy SEALs (USA) | SCUS-97134 | Fair | <sup>Not fully tested</sub> | <sup>Aim Assist: Off</sub> | - |
| Serious Sam: Next Encounter (USA) | SLUS-20907 | Good | <sup>Vehicles not supported</br>Not fully tested</sub> | <sup>Auto Center: Off</br>Auto Aim: Off</sub> | - |
| SWAT: Global Strike Team (USA) | SLUS-20433 | Good | <sup>Not fully tested</sub> | <sup>Auto Leveling: Off</br>Auto Aim: Off</br>Targeting Aid: Off</sub> | - |
| Time Crisis II (USA) | SLUS-20219 | Good | <sup>Not fully tested</sub> | - | - |
| TimeSplitters (v1.10, v2.00) (USA) | SLUS-20090 | Good | <sup>**Optional cheat to always show crosshair**</br>Not fully tested</sub> | <sup>Auto Lookahead: No</br>Auto Aim: Off</sub> | **B4A004F2.pnach (v1.10)</br>8966730F.pnach (v2.00)** |
| Urban Chaos: Riot Response (USA) | SLUS-21390 | Good | <sup>Not fully tested</sub> | <sup>Auto-Center: No</sub> | - |
| Vampire Night (USA) | SLUS-20221 | Good | <sup>Not fully tested</sub> | - | - |
* NOTE: PCSX2 will only hook with **BIOS versions 5XXXX and up**.
* NOTE: Some aspects may break when a game is started with overclocking. Requires testing.
* PCSX2 Settings: **Disable** *'Settings->Interface->Double-Click Toggles Fullscreen'* | **Enable** *'Settings->Interface->Hide Cursor In Fullscreen'*
* RDR Gatling/Final Scene Fix: Start a new game on a new name. When in-game, pause and quit back to menu. Reload your main save.
* Place cheat files in 'cheats/PS2' folder in the main PCSX2 directory. In PCSX2 go to 'Settings->Emulation' and tick 'Enable Cheats'.

## Supported PPSSPP Titles
| Game Title | Serial | Mouse Support | Issues | In-game Options |
| ---------- | ------ | :-----------: | ------ | --------------- |
| Coded Arms (USA) | ULUS10019 | Fair | <sup>Not fully tested</sub> | <sup>Free Look->Lock On: None</sub> |
| Ghost in the Shell: Stand Alone Complex (USA) | ULUS10020 | Fair | <sup>Not fully tested</sub> | |

# **|  FREQUENTLY ASKED QUESTIONS  |**
### Q: How do I install?
  - The program has no installation and will work from any directory. Just download the <br>
  **latest release**, extract the contents of the archive to a convenient location and run<br>
  the executable.
### Q: Why is game not hooking?
  - If the game is not hooking there are a few things to check:
    - Only one supported emulator is running
    - Emulator is supported and version matches what is listed in this README<br>
    (Newer or older versions may work, but the listed version is tested working)
    - ROM/ISO match the version/serial listed in this README
    - **PCSX2**: PS2 BIOS version is **5XXXX or higher**
    - **RetroArch**: RA window must be **focused** for it to hook initially
  - Some emulator settings prevent hooking so you can also try **restoring the default emulator settings**:
    - **PCSX2**: *Settings->Interface->Restore Defaults*
    - **DuckStation**: *Settings->General->Restore Defaults*
  - **NOTE**: The program has only been tested on **Windows 10** and may not be compatible<br>
  with other versions of Windows
  - **NOTE**: If emulator is restarted, the injector must be restarted as well
### Q: Game hooks but is not listed as supported?
  - There are many games that hook but aren't listed as supported as they are unfinished<br>
  hacks. A game is added to the supported list when enough testing has been done to assume<br>
  that the core game can be completed without any major issues.
### Q: Where is the controller input profile?
  - The releases don't include input profiles but I've added my controller profiles to the<br>
  project if you would like to use the same configuration. Although you should probably just<br>
  make your own.
### Q: Will this work with netplay/online?
  - Most likely **NO**, single-player only.

# ManyMouse

ManyMouse is Copyright (c) 2005-2012 Ryan C. Gordon and others. https://icculus.org/manymouse/
