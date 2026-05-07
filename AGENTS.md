# Codex Collaboration Guide

This repository is a Unity 2D pixel-art game project. When Codex assists with this project, keep changes small, testable, and easy for Unity beginners to understand.

## Project Conventions

- Use the Unity version listed in `ProjectSettings/ProjectVersion.txt`.
- Do not commit `Library/`, `Temp/`, `Obj/`, `Logs/`, `UserSettings/`, `Build/`, or `Builds/`.
- Always keep Unity `.meta` files with their matching assets.
- Prefer editing scenes, prefabs, materials, animations, and other Unity YAML assets through the Unity Editor.
- Use Git LFS for large binary assets such as `.aseprite`, `.psd`, audio, video, and model files.
- All project comments must be written in English. This includes C# comments, XML documentation comments, TODOs, Unity notes, and comments in configuration files.

## Codex Working Rules

- Check the existing folder structure and Git status before making changes.
- Do not rename or move Unity assets unless the task explicitly asks for it.
- Prefer simple, direct MonoBehaviour components when writing gameplay code.
- Place new gameplay scripts under `Assets/Scripts/`. Create the folder if it does not exist.
- Keep serialized field names clear so they are understandable in the Unity Inspector.
- Prefer `[SerializeField] private` fields over public fields for Inspector-tuned values.
- After changes, explain which files were modified and how to verify the result in Unity.
- Avoid manually editing `.unity`, `.prefab`, `.asset`, `.mat`, `.anim`, or `.controller` files unless the requested change is narrow and safe to verify.

## Recommended Prompts

- "Create a movable 2D player character script using the new Input System."
- "Check whether my current changes contain Unity collaboration risks."
- "Help organize this scene structure for a pixel-art platformer."
- "Explain when each part of this script runs in the Unity lifecycle."
- "Review this Git status and tell me which files should be committed."
