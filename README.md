[README.md](https://github.com/user-attachments/files/32411482/README.md)
# PS-16 Pocket Sampler

PS-16 is a mobile-first browser groovebox and sampler inspired by compact hardware samplers, step sequencers and acid boxes.

It runs as an installable **Progressive Web App (PWA)**, so it can be hosted on GitHub Pages, opened in Chrome on Android and installed to the home screen like an app.

## Live version

If this repository is published with GitHub Pages, the app will be available at:

`https://YOUR-USERNAME.github.io/PS16/`

For the current project:

`https://bazcando.github.io/PS16/`

## Main features

- 16-step sequencer
- Multiple instrument banks
- DRUMS, BASS and SYNTH banks
- 808-style and 909-style drum banks
- ACID monosynth bank with 303-style controls
- Multiple USER banks for imported and recorded samples
- Pattern slots and pattern chaining
- Pattern copy workflow
- Per-step pitch locks
- Step probability
- Ratchets / repeated hits
- Per-step Tone, Grit, Pan and Decay locks
- ACID root-note and scale mapping
- Sample chopping across pads
- Microphone sampling
- Full-length playback for imported and mic-recorded samples
- Live mixer with per-bank level, mute and solo
- Sequencer pad overview
- Tempo-synced Scene FX
- Floating Play / Stop transport
- Snap-to-section mobile interface
- Local project saving
- IndexedDB storage for imported and recorded samples
- WAV export for sharing tracks externally
- Offline PWA support

## ACID controls

The ACID bank has its own synth controls:

- Tune
- Cutoff
- Resonance
- Envelope Modulation
- Decay
- Accent
- Glide
- Saw / Square waveform

The ACID pads can also be remapped to a selected root note and scale.

## Scene FX

Scene FX are designed for live performance and are tempo-aware.

Available effects include:

- Stutter
- Filter Drop
- Tape Stop
- Echo Throw
- Glitch

Timing divisions are derived from the current BPM.

## Using samples

### Import a sample

1. Select a USER bank and pad.
2. Tap **LOAD SAMPLE**.
3. Choose an audio file from your device.
4. The sample is assigned to the selected pad.

### Record from the microphone

Microphone recording requires the app to be served over **HTTPS**.

1. Open the hosted PWA in Chrome.
2. Allow microphone access when prompted.
3. Select a pad.
4. Hold the sample-record control while recording.
5. Release it when the sample is finished.

If microphone permission is blocked, check Chrome's site permissions for the hosted PS-16 address.

## Sample chopping

A longer imported or recorded sample can be divided across 16 pads using **CHOP → 16**.

This is useful for:

- breaks
- drum loops
- vocal phrases
- bass loops
- field recordings

## Sequencing

Tap steps to create a pattern for the currently selected pad.

Long-press an active step to open step-specific controls such as:

- Pitch
- Probability
- Ratchets
- Tone
- Grit
- Pan
- Decay

The sequencer overview shows which pads already contain programmed steps and flashes as sounds trigger.

## Patterns and chains

PS-16 supports multiple pattern slots.

A typical workflow is:

1. Build Pattern 1.
2. Copy it to the next pattern.
3. Change drums, bass or synth parts.
4. Repeat to create variations.
5. Add patterns to the chain.
6. Enable chain playback.

Example:

`1 → 1 → 2 → 3 → 2 → 4`

## Live Mix

The LIVE MIX section provides per-bank control over:

- Level
- Mute
- Solo

Mixer faders are designed to stay fixed under the finger on mobile without dragging the page.

## Project saving

PS-16 saves project data locally in the browser.

Saved data includes:

- patterns
- chain arrangement
- step locks
- mixer settings
- BPM and swing
- pad settings
- ACID settings
- imported samples
- microphone recordings

Imported and recorded audio is stored using IndexedDB.

There are also manual **SAVE NOW** and **CLEAR SAVED PROJECT** controls.

## WAV export

Use **EXPORT AUDIO** to render the current arrangement.

- With Chain Mode on: exports the full chain once.
- With Chain Mode off: exports the current pattern.

The generated WAV can then be uploaded to services such as SoundCloud or Bandcamp.

## Installing as an app on Android

1. Open the hosted HTTPS version in Chrome.
2. Use the browser install prompt or **Add to Home screen**.
3. Launch PS-16 from the home screen.

Because it is a PWA, the app can also work offline after it has been loaded and cached.

## Hosting with GitHub Pages

1. Create a public GitHub repository.
2. Upload the contents of this project to the repository root.
3. Make sure `index.html` is at the top level.
4. Go to **Settings → Pages**.
5. Choose **Deploy from a branch**.
6. Select `main` and `/root`.
7. Save.

The app should then be available at:

`https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`

## Updating the live app

Replace the project files in the GitHub repository and commit the changes.

Because PS-16 uses a service worker, an installed copy can sometimes keep an older cached build. If that happens:

1. Close PS-16 completely.
2. Reopen the hosted URL in Chrome.
3. Refresh the page.
4. If necessary, clear site data for the PS-16 GitHub Pages site and reopen it.

## Browser requirements

PS-16 is primarily designed for modern Chromium-based mobile browsers.

For microphone sampling and full PWA behaviour, use a secure HTTPS-hosted version rather than opening `index.html` directly as a local file.

## Project status

PS-16 is an experimental groovebox project and is still evolving. The current focus is on fast mobile workflow, live performance, sampling, sequencing and DAWless-style interaction.

