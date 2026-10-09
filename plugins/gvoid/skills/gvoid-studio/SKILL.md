---
name: gvoid-studio
description: Use when the user wants to create or edit media with GVOID — an image, a video clip, a cinematic voice line, a song, a sound effect, a 3D model or an animation for a rigged character — or asks about their GVOID balance, models, prices or past creations.
---

# Creating with GVOID

GVOID generates media in the user's own account and charges each creation in
**voids** (their balance). Everything created lands in their GVOID library.

## Before generating

1. `gvoid_me` — plan and current balance, and whether they pay from a team or
   their own voids.
2. `gvoid_models` — the model ids, their options (resolutions, ratios,
   durations, qualities, voices, emotions) and the **price in voids** of each.
   Pick a model that fits the request and tell the user the price before
   spending, unless they already said to go ahead.

## Generating

| Want | Tool |
|---|---|
| Image(s) | `gvoid_generate_image` |
| Video clip | `gvoid_generate_video` (text, reference images, or start/end frames) |
| Spoken line | `gvoid_generate_voice` (emotion, the user's voice profiles; performance tags in [brackets]) |
| Song or instrumental | `gvoid_generate_music` |
| Sound effect | `gvoid_generate_sfx` |
| 3D model (.glb) from an image | `gvoid_generate_3d` |
| Animate a rigged 3D character | `gvoid_generate_motion` |

Every generation returns a **run id**. Call `gvoid_run` with it until the status
is `completed` or `failed` (`wait_seconds` lets one call wait). Video, music and
3D take minutes, not seconds; say so instead of polling silently.

## Using the user's own files

- `gvoid_assets` lists what they already have, with ids and urls.
- `gvoid_upload` adds an image, audio, video or 3D file and returns its asset id.
- Pass asset ids as references: an image as the first frame or reference of a
  video, an image as the source of a 3D model, and so on. Chain steps this way
  (image → video, video + voice) instead of starting over.

## Good practice

- Short, concrete prompts beat long lists of adjectives: subject, action,
  camera, light, style.
- If a generation fails, read the message in `gvoid_run` and change what it
  points to (prompt, reference, option) before retrying; failed runs are not
  charged.
- Share the resulting urls with the user and offer the next step.
