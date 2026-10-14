# TankStars2D

A turn-based 2D artillery game made with **Unity 6 (6000.2)** and C#. Two tanks take turns firing at each other across generated terrain until one is destroyed.

## Gameplay

- 20-second turns, a limited fuel bar for driving, and a limited ammo count per weapon
- Choose a weapon, set angle and power (a dotted trajectory preview helps), and fire; some weapons fire bursts
- Explosions deal radial damage with falloff; the last tank standing wins
- Solo mode and a main menu with scene fades

## Controls

| Key | Action |
|---|---|
| `A` / `D` or `←` / `→` | drive |
| `W` / `S` or `↑` / `↓` | aim up / down |
| `Q` / `E` | decrease / increase power |
| `Space` | fire |

## Run it

1. Install Unity 6 (editor version `6000.2.8f1`, see `ProjectSettings/ProjectVersion.txt`).
2. Open this folder in Unity Hub; Unity regenerates `Library/` and the `.csproj` files on first open.
3. Open `Assets/Scenes/MainMenu.unity` and press Play.

## Code

My own gameplay code is in `Assets/scripts/` (about 2,500 lines of C#):

- `BattelSceneScripts/Managers/` — turn state machine, battle setup, solo mode
- `BattelSceneScripts/tank/` — movement on slopes (ground sensors), aiming, shooting, fuel, missile explosions
- `BattelSceneScripts/ground/LevelGenerator.cs` — Perlin-noise terrain
- `MainMenuScripts/` — menu, game manager, scene fader

## Credits

Third-party art and UI packs (under `Assets/`): HobiSoLoved 2D Platformer Snowy sprites, Space Exploration GUI Kit, UI pack, Universal Stylized UI, TextMesh Pro. The main-menu artwork is AI-generated.
