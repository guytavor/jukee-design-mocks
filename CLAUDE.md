# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jukee-mocks is a project containing HTML mockups for the Jukee Audio-Ad Creator vNext, a unified creator application that merges the previous AdTune Creator and Announcement Creator into one streamlined Gen-AI-first flow.

The mockups demonstrate the user interface for generating and customizing audio ads using AI, with features for prompt-based generation, tweaking generated content, and managing ad history.

## Repository Structure

- `/docs/`: Contains HTML mockups and documentation for the AdCreator UI
  - `AdCreator Q225 1dc9b6bf762480cba7c2e05ca6bff2f4.html`: Main specification document
  - `/AdCreator Q225 1dc9b6bf762480cba7c2e05ca6bff2f4/`: UI mockups
    - `main.html`: Main generation interface with prompt panel and chip selection
    - `tweak_(1).html`: Tweaking interface for post-generation adjustments
    - `history.html`: History panel for browsing previous ad versions
    - `image.png`: Reference image for Elevenlabs voice design

## Key UI Components

1. **Main Generation Interface**:
   - Prompt text area for describing the ad
   - Smart-chip rail for selecting tone, duration, music style, voice preference, etc.
   - Generation action bar with Generate/Reset buttons
   - Output carousel for generated audio previews

2. **Tweak Panel**:
   - Narration text editor
   - Voice actor selector
   - Music bed picker
   - Timing and volume controls
   - Brand chime toggle
   - Sound effects manager

3. **History Panel**:
   - List of previously generated ads
   - Options to use or delete previous versions
   - Status indicators (draft/saved/published)

## JSON Communication Format

The mockups define a JSON format for communication between the Gateway and UI:

1. **Render Spec**: Contains parameters for audio generation including:
   - `script_text`: The narration text
   - `voice_id`: Selected voice actor
   - `music_bed_id`: Background track
   - Timing parameters, volume settings, sound effects, etc.

2. **Session JSON**: Full state of the ad creator session including:
   - Current render spec
   - Generated previews
   - History of versions
   - Available assets (voices, music, SFX)

## Development Notes

Since this repository contains static HTML mockups, there's no build system or tests to run. The mockups are intended for reference when implementing the actual application.

When working with these files:
- HTML files can be viewed directly in a browser
- Changes to the mockups should maintain the existing structure and naming conventions
- New mockups should follow the same styling and organization patterns