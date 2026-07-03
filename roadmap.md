# Poor man's Quad Cortex
  
In this file you will find all the ideas that lead to this midi controller project
  
# MIDI Controller – Brainstorm & Requirements

## Vision

Design and build a premium MIDI foot controller focused on guitar plugins.

The goal is not only to send MIDI messages but to create a controller that behaves as an extension of the plugin itself, with dynamic feedback and an intuitive user experience.

---

# Design philosophy

- Compact but robust aluminium enclosure
- Minimalistic and professional appearance
- Instant readability on stage
- No unnecessary controls
- Plugin-agnostic whenever possible
- Modular firmware architecture

---

# Core features (MVP)

## Footswitches

- Multiple silent footswitches
- Configurable MIDI CC / Program Change
- LED feedback
- Bank switching

---

## Main display

Display showing:

- Current plugin
- Plugin logo (if available)
- Current operating mode
    - Preset Mode
    - Stomp Mode
- Current preset name

Example:

```
Neural DSP - Archetype Plini

Preset Mode

Lead Ambient
```

---

## MIDI

Support for:

- MIDI over USB
- Standard MIDI DIN (optional)
- Program Change
- Control Change
- Expression pedals

---

# Advanced ideas

## Dynamic stomp labels

Each footswitch has a small display above it.

Instead of fixed labels:

```
OD
Delay
Reverb
```

they become dynamic.

Example with Archetype:

```
Comp
Boost
Delay
Reverb
```

Changing plugin or mapping automatically updates every display.

---

## Plugin-independent mapping

Rather than hardcoding pedal names:

Create a mapping layer.

Example:

Plugin:

```
Neural DSP Plini
```

Mapping:

```
Switch 1 -> Compressor

Switch 2 -> Overdrive

Switch 3 -> Delay
```

Changing plugin simply loads another mapping.

---

## Stomp Mode

Each switch controls one plugin pedal.

Display above each switch always shows:

- effect name
- state
- optional color

Example

```
Boost
ON
```

---

## Preset Mode

Switches become:

```
Preset 1
Preset 2
Preset 3
Preset 4
```

Main display shows:

```
Plugin

Preset name
```

---

## Hybrid Mode

Interesting future feature:

Top row

```
Preset selection
```

Bottom row

```
Individual effects
```

---

# Displays

Possible technologies:

- OLED
- Memory LCD
- IPS LCD

One display above every footswitch.

Requirements:

- Good contrast
- Readable on stage
- Fast refresh
- Low power consumption

---

# User interface

Main screen should remain uncluttered.

Always display:

- Plugin name
- Logo
- Mode
- Current preset

Secondary information:

- MIDI channel
- Connected device
- Battery / USB state

---

# Firmware architecture

Possible abstraction:

```
Plugin

├── Presets
├── Effects
├── MIDI Mapping
└── UI
```

Changing plugin only loads another configuration.

---

# Configuration software

Long-term idea.

Desktop application allowing:

- MIDI mapping
- Display labels
- Colors
- Banks
- Presets

without reflashing firmware.

---

# Hardware ideas

- USB-C
- Optional 5-pin MIDI
- Expression pedal inputs
- TRS MIDI compatibility
- Daisy-chain possibility

---

# Mechanical design

Premium aluminium enclosure. Wooden side for style.

Goals:

- Easy access on stage
- Large spacing between switches
- Excellent visibility

---

# Stretch goals

## Automatic plugin detection

If technically possible:

Computer reports:

- active plugin
- preset
- enabled effects

Controller updates automatically.

---

## Bidirectional communication

Ideal workflow:

Plugin changes preset

↓

Controller updates displays

↓

Controller LEDs update

↓

Controller labels update

---

## Profiles

Store multiple complete configurations.

Example:

```
Neural DSP Plini

↓

Automatic profile
```

```
Helix Native

↓

Another profile
```

---

# Development roadmap

## Phase 1

- MIDI communication
- Footswitch handling
- LEDs
- Preset switching

---

## Phase 2

- Main display
- Banks
- Configuration system

---

## Phase 3

- Individual displays
- Dynamic labels
- Plugin profiles

---

## Phase 4

- Bidirectional communication
- Desktop editor
- Automatic synchronization

---

# Overall goal

Create a controller that feels like dedicated hardware for any guitar plugin rather than a generic MIDI controller.