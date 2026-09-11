# Soundr

**Algorithmic Music Production Software**  
Visual Basic .NET · Windows Forms · Audio Sequencing · Weighted Randomization · UI/UX

> **Jessica Builds — From a thought to reality through innovation.**

Soundr is a desktop music-production application designed to turn raw user-provided sounds into structured beats through programmable musical logic.

Rather than generating completely random audio, Soundr uses rule-based placement and weighted randomization to decide where uploaded sounds should appear in a 16-step sequence. The goal is to make beat creation more accessible while still preserving musical structure.

## The idea

Music production normally requires a DAW, arrangement knowledge, rhythm instincts, and a large amount of manual experimentation. Soundr explores a different approach:

**What if the musical decisions themselves could be encoded into software?**

The application allows a user to bring in audio material and lets the program make arrangement decisions automatically.

## Core system

Soundr is structured around four major layers:

```text
USER
 │
 ├── Landing / Authentication UI
 │
 └── Try Now workspace
        │
        ├── Upload audio files
        │      .wav / .mp3
        │
        ├── Smart Mix engine
        │      weighted randomization
        │      musical placement rules
        │      16-step sequencing
        │
        └── Playback engine
               Windows Media Player controls
               mix / play / pause
```

## Smart Mix algorithm

The main engineering idea is the mixing engine.

Instead of placing every sound with uniform randomness, Soundr uses **weighted randomization** and conditional logic so different instruments can have different probabilities and roles inside the sequence.

The resulting logic can be thought of as:

```text
load user audio
      ↓
classify / assign sound role
      ↓
iterate over a 16-step pattern
      ↓
apply weighted placement decisions
      ↓
construct beat arrangement
      ↓
synchronize playback
```

This converts a subjective creative task — deciding *where a sound should occur* — into a programmable decision system.

## Audio workflow

### File integration

Soundr uses the standard Windows file picker so users can load their own audio assets into the application.

Supported project workflow includes `.wav` and `.mp3` files.

### Beat generation

The **Mix** action builds the beat arrangement before playback. Program logic uses arrays, loops, conditional statements, `Select Case`, arithmetic/logical operators, and randomized decisions to construct the sequence.

### Playback

The **Play** action synchronizes the audio engine and plays the generated result.

The **Pause** action freezes playback until the user resumes.

The project integrates Windows Media Player through COM references to `WMPLib` and `AxWMPLib`.

## Application structure

The supplied Visual Basic project defines a Windows Forms application with separate UI surfaces for:

- `LandingPage`
- `LogIn`
- `SignUppage`
- `TryNow`

The project targets Windows and uses `System.Windows.Forms`, `System.Drawing`, and Windows Media Player interoperability.

## Interface design

Soundr was designed as a consumer-facing creative tool rather than a default classroom form application.

The visual system uses a black, white, and red identity with custom full-screen interface artwork embedded into the Windows Forms resources.

The `TryNow` workspace contains dedicated visual controls for:

- Mix
- Play
- Pause
- Melody upload
- multiple audio-player components

The interface design was created separately and then integrated into the Windows Forms application as background and control imagery.

## Authentication flow

The application includes sign-up and login forms as part of the user flow.

The prototype checks credentials against application-held data. This demonstrates application state, input validation, and navigation logic, but it is intentionally described here as a prototype authentication flow rather than production-grade identity infrastructure.

## Programming concepts demonstrated

- Visual Basic .NET
- Windows Forms application architecture
- modular forms
- arrays
- loops
- `If / Else` conditional logic
- `Select Case`
- arithmetic and logical operators
- timers
- Windows `OpenFileDialog`
- media-player integration
- state-driven UI behavior
- randomized algorithms
- audio sequencing logic

## Why this project matters

Soundr sits at the intersection of **software engineering and creative systems design**.

The interesting problem was not simply playing audio files. It was translating creative intuition into logic:

- When should an instrument enter?
- How frequently should it repeat?
- How can randomness create variation without creating noise?
- How should different sound layers interact?
- How can software make a creative workflow easier for someone without production experience?

That same pattern — converting human decisions into repeatable algorithms — appears throughout automation, AI systems, generative tools, and intelligent software.

## Current repository contents

The uploaded project material includes:

- Visual Basic project configuration
- Windows Forms resource files
- embedded interface artwork
- embedded media-control state
- project presentation / system documentation

The available upload does **not** include the original `.vb` source-code files for the form event handlers, so this repository documents the implemented application and preserves the project configuration/resources that are available without inventing missing source.

## Tech stack

**Language / framework**
- Visual Basic .NET
- .NET Windows Forms

**Media**
- Windows Media Player COM integration
- `WMPLib`
- `AxWMPLib`

**Application concepts**
- local file integration
- 16-step sequencing
- weighted randomization
- rule-based beat generation
- event-driven UI

## Future iterations

- restore/import the original `.vb` event-handler source files
- move sequencing into a standalone reusable music engine
- visualize the generated 16-step pattern
- expose probabilities and arrangement rules as user controls
- support BPM and key-aware generation
- add track export / rendering
- migrate authentication to persistent secure storage
- separate UI, sequencing, and audio-engine concerns into distinct modules

---

### Jessica Builds
**From a thought to reality through innovation.**
