# FACE–Voice Core — Product Purpose

## What this project is

FACE–Voice Core is the voice-experience subsystem for FACE. It gives members ways to communicate and participate through voice, alongside the platform's other social interactions.

It is a product subsystem—not the private voice-measurement engine and not the social network itself.

## Member voice experiences

The subsystem is intended to support:
- Voice messages in one-to-one and group conversations.
- Live voice rooms for communities and events.
- Voice participation in creator spaces and hosted sessions.
- Optional voice posts or audio attachments.
- Join, leave, mute, unmute, hand-raise, host, and moderator controls.
- Clear participant and speaking-state indicators.
- Consent-based recording only where explicitly enabled and clearly disclosed.
- Captions or transcripts when enabled, with clear notice and controls.
- Reporting, blocking, moderation, and host safety controls for voice spaces.
- Network-quality feedback and graceful recovery from interruptions.

## Experience concepts retained from the original design

The original project notes describe a voice-first experience with:
- **AI Performance Mirror:** optional, private practice feedback for a speaker or creator.
- **Unseen Audience:** a practice/simulation concept for rehearsing delivery; it must be clearly labelled as simulated and never represented as real listeners.
- **Vibe States:** user-facing session or room modes that describe the chosen atmosphere or activity, not inferred emotional states.
- **Director Rules:** transparent session facilitation rules for turn-taking, timing, and host controls.
- **Rotation:** optional, explicit speaker-turn rotation for rooms and practice sessions.

These concepts support voice participation and creator practice; they do not replace the core social voice features.

## Privacy and safety

- Voice participation is opt-in.
- Microphone access requires explicit device permission and a clear in-product indication when active.
- Recording and transcription are off unless a user knowingly enables them and the applicable participants are informed.
- Provide mute, leave, block, report, and host moderation controls.
- Do not infer a person's identity, emotion, health, age, or personality from their voice.
- Do not silently monitor members or create hidden voice profiles.
- Practice feedback is private to the participant unless they deliberately share it.

## Separation from VoiceScore Core

FACE–Voice Core owns voice product workflows, session orchestration, participant controls, and integration contracts. VoiceScore Core remains a separate private specialist engine. Any future connection must be explicit, consent-based, purpose-limited, and governed by a versioned contract. Raw audio and private analysis logic must not be exposed to FACE clients.

## Build order

1. Voice domain model and event/state contracts.
2. Voice-message lifecycle and secure media references.
3. Live-room lifecycle, membership, roles, and controls.
4. Moderation, consent, recording, and retention policies.
5. Client integration and network-failure handling.
6. Optional practice mirror and simulated audience workflows.
7. Automated tests for permissions, privacy, room state, and moderation.

## Current implementation status

This charter establishes the product purpose and safety boundaries. It does not claim that voice messaging, live rooms, media infrastructure, or AI practice tools are implemented or operational.
