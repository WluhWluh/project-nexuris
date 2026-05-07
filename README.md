# project-nexuris

Neko's Passion Game is a Unity 2D pixel-art game project.

## Quick Start

1. Install Unity Hub and the Unity editor version listed in `ProjectSettings/ProjectVersion.txt`.
2. Clone the repository:

   ```powershell
   git clone https://github.com/Programers01/project-nexuris.git
   cd project-nexuris
   ```

3. Initialize Git LFS:

   ```powershell
   git lfs install
   git lfs pull
   ```

4. Open the project root folder with Unity Hub.
5. Wait for Unity to finish importing assets, then open `Assets/Scenes/SampleScene.unity`.

## Daily Collaboration Workflow

Before starting work:

```powershell
git pull
git status
git lfs pull
```

Create a feature branch for each small task:

```powershell
git switch -c feature/player-movement
```

Commit after each meaningful step:

```powershell
git status
git add Assets ProjectSettings Packages .gitattributes README.md AGENTS.md
git commit -m "Add player movement"
git push -u origin feature/player-movement
```

Then open a Pull Request on GitHub and ask another teammate to review it before merging into `main`.

## Unity Collaboration Rules

- Do not commit `Library/`, `Temp/`, `Obj/`, `Logs/`, `UserSettings/`, `Build/`, or `Builds/`.
- Do not delete `.meta` files. Unity uses them to preserve asset identity and references.
- Avoid editing the same scene or prefab at the same time as another teammate.
- If a scene or prefab must be shared, communicate before editing it.
- Large binary assets should be tracked with Git LFS, including source art, audio, video, and model files.
- All project comments must be written in English, including C# comments, Unity notes, TODOs, and documentation comments.

## Using Codex

Good tasks for Codex:

- Write or explain Unity C# scripts.
- Review Git status, commits, and possible merge risks.
- Organize project folders and documentation.
- Break gameplay ideas into small implementation tasks.
- Create small editor tools, runtime utilities, or test scripts.

When asking Codex for help, describe the goal, relevant scene or script path, and expected Unity behavior. Example:

```text
Create a 2D player movement script under Assets/Scripts.
Use Rigidbody2D, support left/right movement and jumping,
and explain how to attach it in the Unity Inspector.
```

## Recommended Asset Layout

The project can stay simple at the beginning:

```text
Assets/
  Art/
    Sprites/
    Tilesets/
    UI/
  Audio/
    Music/
    SFX/
  Prefabs/
  Scenes/
  Scripts/
    Player/
    Enemy/
    Core/
    UI/
  Settings/
```

Prefer moving assets through Unity's Project window so Unity can keep `.meta` files and references in sync.
