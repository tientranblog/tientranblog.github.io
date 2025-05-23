---
title: Building Catch The Words Android App
excerpt: An Android App that helps to improve word recognition skills through interactive quizzes
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/1775529c72cc694af4067ba3f23b7ad9.png
---
## Business Scenario

Catch The Words is an educational Android app designed to help users, especially children, improve their vocabulary and word recognition skills through interactive quizzes. The app presents users with questions related to different topics, encouraging learning in a fun and engaging way.

## Techniques

- **Platform:** Android
- **Language:** Kotlin
- **UI:** Android XML layouts with Material Design components
- **Build System:** Gradle (Kotlin DSL)
- Components:
	- **Activities:**`MainActivity` (main screen), `TopicActivity` (topic selection and quiz screen)
	- **Dialog Fragment:**`RateFragment` (custom dialog for user feedback/rating)
	- **Navigation Menu:** Options menu for navigation (e.g., return to home, switch topics)
	- **UI Components:**`Button`, `ImageView`, `TextView`, `EditText` (for user interaction and display), Custom layouts defined in XML
	- **Intents:** Used for navigation between activities and passing data (e.g., selected topic)

## Workflow

**Step 1: Launch App** 
- The main screen displays the app title and navigation buttons.

**Step 2: Start Quiz** 
- Clicking "Play" navigates to the topic selection screen.

**Step 3: Select Topic** 
- User selects a topic, which updates the background and available questions.

**Step 4: Answer Questions** 
- User selects a question, views an image, and submits an answer.

**Step 5: Get Feedback** 
- The app checks the answer and displays `Correct!` or `Try again -_-`

**Step 6: Request Hint** 
- User can tap "Hint" to see a clue for the current question.

**Step 7: Rate App** 
- User can open a dialog to rate the app and submit feedback, which is displayed on the main screen.

## Functionalities

- Launch Screen
<img src="/assets/obsidian/94df8e03a3d60555f5bca99d7198271d.png" />

- Topic Screen
<img src="/assets/obsidian/1775529c72cc694af4067ba3f23b7ad9.png" />

- Question Screen
<img src="/assets/obsidian/b2c6e4680559da6c994048fb4d84d10c.png" />

## Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/URkx2IEbG5w?si=Vu6-HWzsLcM5eBkv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

