# Tao Project: VR Backrooms Spatial Memory Prototype

## 1. Project Overview

This project is a VR spatial memory prototype built in a backrooms-style maze environment.

The core idea is to study how different navigation aids may influence a user's ability to remember space and return to a fixed home location in VR.

At this checkpoint, the focus is not on a complete experiment or polished visual design. Instead, the APK demonstrates that the main project concept is already functional at a basic level.

The current prototype allows a user to:

- Start from a fixed home/spawn location
- Explore a confusing maze environment
- Use optional system guidance
- Place user-created markers
- Return to the home area
- Automatically start a new trial after returning home
- Save a simple CSV log for later analysis

---

## 2. Core Design Idea

The project compares two types of navigation support:

### System Guidance

The system provides a directional arrow that points back to the home location.

This represents direct system-provided navigation assistance.

### User-Created Markers

The user can place markers in the environment during exploration.

This represents user-controlled external memory support.

The long-term goal is to compare navigation performance under different support conditions, such as no support, system guidance, and user-created markers. For Checkpoint 1, the main goal is to show that these core mechanisms are implemented and testable.

---

## 3. Implemented APK Features

### Backrooms Maze Environment

The APK includes a maze-like backrooms environment with corridors, turns, and repeated-looking spaces.

The environment is intentionally designed to create spatial memory difficulty.

### Fixed Home / Spawn Area

The user always starts from a fixed home location.

This home area is also used as the return target. When the user returns to this area, the current round is completed.

### Trial Flow

The prototype uses a simple round-based structure:

1. The user starts at home.
2. The round begins after the user leaves the home area.
3. The user explores the maze.
4. After the exploration phase, the user returns to home.
5. When the user reaches home, the round is completed.
6. The system resets for the next round.

### System Guidance Arrow

A guidance arrow can be displayed in front of the user.

The arrow points toward the home location and can be turned on or off.

### User Marker System

The user can place visual markers in the maze.

Markers can help the user remember paths, turns, or important locations. The number of available markers is limited during each round.

### Automatic Reset

After the user returns home, the system automatically prepares the next round.

The marker count is reset, old markers are cleared, and the next round can begin from the home area.

### CSV Logging

Each completed round is saved as one row in a CSV file.

The log is designed to stay simple and easy to analyze.

---

## 4. Controls

### Movement

- **Left joystick**: Move
- **Right joystick**: Turn

### System Guidance

- **B button**: Toggle the system guidance arrow on or off

### User Markers

- **Hold left trigger**: Preview marker placement
- **Release left trigger**: Place marker

---

## 5. Log Design

The APK records one row for each completed round.

The CSV file records:

| Field | Description |
|---|---|
| trial_index | The round number |
| system_guidance_enabled | Whether the system guidance arrow was enabled |
| markers_used | Number of markers placed in the round |
| return_time | Time used to return home |
| completed | Whether the user successfully returned home |

The log is saved on the Meta Quest device under:

```text
Documents/tao-project/
````

This file can be retrieved from the Quest through USB file transfer.

---

## 6. How to Demonstrate the Prototype

To demonstrate the APK:

1. Install and open the APK on a Meta Quest headset.
2. Start from the home/spawn area.
3. Move through the backrooms maze using the joystick.
4. Press **B** to show or hide the system guidance arrow.
5. Hold and release the **left trigger** to place markers.
6. Return to the home area to complete the round.
7. Check the generated CSV log after completing rounds.

---

## 7. Current Status

The Checkpoint 1 prototype is functional.

The following core components are already working:

* VR maze environment
* Player movement
* Fixed home area
* Round start and completion logic
* System guidance toggle
* User marker placement
* Automatic reset between rounds
* CSV log output

This means the project direction is already testable at a minimal level.

---

## 8. Next Step

The next step is to turn this working prototype into a more formal experiment.

The planned experiment will compare different navigation support conditions, such as:

* No navigation aid
* System guidance only
* User-created markers only

These experimental conditions will be developed and described more fully in the next checkpoint.

```
```
