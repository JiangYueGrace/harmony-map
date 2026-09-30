# Harmony Map

An interactive chord map for exploring, hearing, and understanding harmony through visual chord connections.

> **Live demo:** https://jiangyuegrace.github.io/harmony-map/

## Why I built it

Music theory is often taught as a set of rules to memorize. I wanted to explore a different approach: **learn harmony by seeing connections, hearing them immediately, and understanding why they work.**

Harmony Map turns chord relationships into an interactive graph. Instead of asking the product to recommend what to play next, users can explore all pre-defined harmonic paths and make their own choices.

## What you can do

- Choose a musical key
- Click any chord to hear it instantly
- Explore pre-defined chord-to-chord connections
- Filter paths by mood: **Happy / Sad / Dreamy / Tense**
- See a short explanation of why each transition works
- Build a chord progression step by step
- Play the full progression
- Switch between English and Chinese

## Product principles

### 1. Explore, don't recommend
The product does not tell users which chord they *should* choose. It shows the available harmonic paths and lets users explore.

### 2. Deterministic music theory
Chord relationships and explanations are precomputed rather than generated at runtime. This keeps the learning experience consistent and musically explainable.

### 3. Hear first, explain second
Every chord and transition can be played immediately. Theory is introduced after the user hears the relationship.

### 4. Keep the MVP lightweight
The first version is a single static HTML file with no backend, account system, or AI dependency.

## How it works

The MVP uses a precomputed harmony graph:

**Chord → valid harmonic connections → relationship type → mood tags → explanation**

Current relationship types include:

- Diatonic movement
- Dominant → tonic
- Secondary dominant
- Relative major / minor
- Parallel major / minor
- Borrowed iv
- Borrowed ♭VI
- Borrowed ♭VII
- Leading-tone diminished → tonic
- Triad ↔ seventh-chord color variation

## Audio

Harmony Map does not store a separate audio file for every chord.

Chord notes are stored as MIDI values, and the browser generates the sound in real time using the **Web Audio API**.

This keeps the prototype lightweight and makes it easy to support more chords, voicings, inversions, and progressions later.

## MVP scope

- 12 major-key contexts
- Major, minor, dominant 7, major 7, minor 7, and diminished chords
- Four fixed mood filters
- Prewritten explanations
- Browser-based chord and progression playback
- English / Chinese interface

Not included in the current MVP:

- AI-generated recommendations
- Personalized suggestions
- Melody analysis
- MIDI input
- DAW integration
- User accounts
- Cloud saving

## Tech

- HTML / CSS / JavaScript
- SVG
- Web Audio API
- Precomputed harmony dataset
- GitHub Pages

## Status

Early product prototype focused on validating one core loop:

**Choose → Hear → Explore → Understand → Build a progression**

## Next

Potential future directions include:

- Minor-key contexts
- More chord types and harmonic relationships
- Better instrument samples and voicings
- MIDI keyboard input
- Melody-aware chord exploration
- Saving and sharing progressions
