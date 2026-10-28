# UltiEco roadmap

The roadmap is aspirational and intentionally does not assign release dates.

## Phase 0 — Identity & foundation (current)

- [x] UltiEco name, vision and tagline
- [x] Logo, palette and cross-device concept screens in Figma
- [x] Public GitHub repository
- [x] Repository starter docs and folder structure (once this scaffold is pushed)
- [ ] Review desktop/mobile accessibility and error states
- [ ] Select and add an explicit source license
- [ ] Choose implementation stack
- [ ] Document a concrete pairing threat model and protocol decisions

## Phase 1 — Linux ↔ Android MVP

- [ ] Minimal Linux application window with device status
- [ ] Minimal Android companion with OS-safe permissions
- [ ] Local peer discovery with manual fallback
- [ ] Verified two-endpoint pairing and revocation
- [ ] Reliable presence/offline indicators
- [ ] Intentional encrypted file transfer
- [ ] Reconnect/unpair testing

**Exit criterion:** a Linux PC and Android phone can securely pair over LAN and exchange one selected file.

## Phase 2 — Continuity

- [ ] Opt-in UltiClip clipboard synchronization
- [ ] UltiNotify where OS permissions permit it
- [ ] macOS and Windows adapters
- [ ] Multi-device UX and resilience testing

## Phase 3 — Extensibility

- [ ] Public adapter interfaces and documentation
- [ ] Capability-scoped UltiControl
- [ ] Optional remote transport without a mandatory account
- [ ] Handoff experiments where apps permit it
- [ ] MiGy/wearable companion proof of concept
- [ ] Assess iOS and other platforms, clearly describing restrictions

## Definition of done

Feature docs state supported OS versions, tested device pairings, security/permission behavior, user-visible error states and reproducible testing steps. Implemented and planned capabilities remain explicitly separated.
