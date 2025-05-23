---
title: Building Be Focus Android App
excerpt: A productivity app to improve time management and focus
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/f0a982e2d3c9039c447821e58e338a98.png
---
## Business Scenario

This project is a simple Android productivity app called "Be Focus." It helps users manage their focus sessions by allowing them to set a task name and a timer, then receive notifications and visual feedback when the session is complete. The app is suitable for students, professionals, or anyone looking to improve their time management and focus.

## Techniques

- **Platform:** Android (minSdk 24, targetSdk 34)
- **Language:** Kotlin
- **UI:** Android Views (ConstraintLayout, Spinner, EditText, etc.)
- **Build System:** Gradle (Kotlin DSL)
- **Components:**
	- **UI Components (Views):**`EditText` for Task Name, `Button` for submission, `Spinner` dropdown for time selection.
	- **Fragment:**`NotificationFragment`: Custom dialog fragment to show notifications (e.g., when the task name is empty).
	- **Intent:** start `TimerActivity` and pass task details.

## Workflow

Step 1: **Main Screen**
- User enters a task name with input validation (cannot be empty).
- User selects minutes and seconds for the focus session using spinners.
- User taps "START" to begin.

Step 2: **Timer Screen**
- Displays the task name and a countdown timer with a progress bar.
- User can pause/resume or stop the timer.
- When the timer finishes, a notification and dialog appear to congratulate the user.

Step 3: **Edit Task:**
- User can edit the current task and timer settings from the timer screen.

## Functionalities

- Add and Edit a task
<img src="/assets/obsidian/5076502f9c201fb006138ef3f5e7f49a.png" />

- Play Pause and Reset
<img src="/assets/obsidian/9e74a0fbf9b8e68fa8f0ed0f0196e5b8.png" />

- Notification when task is done
<img src="/assets/obsidian/f0a982e2d3c9039c447821e58e338a98.png" />

## Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/KY_hJifiUkg?si=2HYWo9HbTd7jlfci" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

