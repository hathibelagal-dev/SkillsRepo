# Fish Audio S2 Pro – Emotional TTS Skill

## Overview

Fish Audio S2 Pro is an advanced text-to-speech (TTS) model that enables expressive, emotionally rich speech synthesis using inline tag-based control.

Unlike traditional TTS systems with fixed presets, S2 Pro supports **free-form emotional and stylistic instructions** embedded directly in the text. This allows precise control over tone, pacing, delivery, and personality at any point in the speech.

---

## Core Concept

S2 Pro uses a simple **bracket tag syntax**:

```
[tag]
```

Tags can be inserted anywhere in the text to modify how the speech is delivered.

### Example

```
Hello there. [pause] I didn’t expect to see you. [surprised]
```

---

## Key Features

### 1. Free-Form Tag System

* Supports **15,000+ unique tags**
* Not limited to predefined labels
* Natural language descriptions are allowed

Examples:

```
[whisper in small voice]
[professional broadcast tone]
[pitch up]
[speak like a tired teacher]
```

---

### 2. Emotion and Expression Control

| Tag           | Effect                       |
| ------------- | ---------------------------- |
| `[excited]`   | Energetic, enthusiastic tone |
| `[sad]`       | Soft, emotional delivery     |
| `[angry]`     | Harsh, intense tone          |
| `[surprised]` | Sudden, reactive tone        |
| `[delight]`   | Warm, happy expression       |
| `[shocked]`   | Dramatic surprise            |

---

### 3. Voice and Volume Modulation

| Tag                             | Effect                |
| ------------------------------- | --------------------- |
| `[whisper]`                     | Very quiet speech     |
| `[low voice]`                   | Deep, subdued tone    |
| `[loud]` / `[shouting]`         | High intensity volume |
| `[volume up]` / `[volume down]` | Gradual adjustment    |
| `[screaming]`                   | Extreme intensity     |

---

### 4. Timing and Flow Control

| Tag                     | Effect           |
| ----------------------- | ---------------- |
| `[pause]`               | Natural pause    |
| `[short pause]`         | Brief pause      |
| `[long pause]`          | Extended pause   |
| `[interrupting]`        | Cuts into flow   |
| `[inhale]` / `[exhale]` | Breathing sounds |
| `[panting]`             | Heavy breathing  |

---

### 5. Pause & Flow Guidance (New)

To avoid monotone or droning TTS output, explicitly guide **timing and flow**:

1. **Do not rely on punctuation alone.** Periods, commas, and paragraph breaks are not reliably interpreted as pauses.

   * Always add `[pause]`, `[short pause]`, or `[long pause]` where a natural breath or dramatic pause is needed.

2. **Layer breathing and expressions.**

   * Use `[inhale]` before longer sentences or emotional delivery.
   * Use `[exhale]` or `[sigh]` to signal relief or tension release.
   * Combine micro-expressions like `[chuckle]`, `[soft laugh]`, `[tsk]` to create realistic pacing.

3. **Combine tag types for rhythm.**

   * Example:

     ```
     I can’t believe it. [short pause][whisper][soft laugh] This is amazing.
     ```

4. **Guiding models (like Qwen)**

   * Include instructions in your system prompt:

     ```
     Treat all punctuation as a cue for a pause:
     - Period = [short pause]
     - Comma = micro-pause
     - Paragraph = [long pause]
     Add breathing and subtle expressions to make speech natural.
     ```

5. **Best Practice**

   * Vary pause lengths to match emotion and context.
   * Avoid over-tagging; let the story flow naturally.
   * Test and refine outputs to maintain performance-level delivery.

---

### 6. Conversational Realism

| Tag                         | Effect                       |
| --------------------------- | ---------------------------- |
| `[laughing]`                | Spoken while laughing        |
| `[chuckle]` / `[chuckling]` | Light laughter               |
| `[sigh]`                    | Expresses fatigue or emotion |
| `[tsk]`                     | Disapproval sound            |
| `[clearing throat]`         | Reset tone                   |

---

### 7. Special Effects

| Tag                    | Effect              |
| ---------------------- | ------------------- |
| `[echo]`               | Echo effect         |
| `[with strong accent]` | Accented speech     |
| `[singing]`            | Melodic delivery    |
| `[audience laughter]`  | Background reaction |

---

## Example Scripts (with pauses)

**Dramatic Scene**

```
[low voice] It’s over. [pause] You had your chance. [angry][short pause] Now face the consequences.
```

**Happy Moment**

```
[bright tone] The sun shone through the window. [short pause][delight] You smiled. [inhale] Everything felt lighter. [pause][soft laugh]
```

**Comedic Delivery**

```
I walked in… [pause][laughing] and immediately regretted everything. [short pause][chuckle]
```

---

## Summary

Fish Audio S2 Pro enables:

* Fine-grained emotional control
* Dynamic, human-like speech
* Flexible, creative expression via inline tags
* **Pause and flow management for natural performance**

By following this guide, scripts will breathe, convey emotion, and sound more like a live performance rather than a monotone narration.
