# Security & privacy design rules

UltiEco should connect devices **without** bypassing the security boundaries of the operating systems it runs on.

## Requirements

1. **Local-first by default.** LAN functionality should not require a cloud account.
2. **Mutual pairing consent.** Both endpoints approve; peers authenticate each other.
3. **Authenticated encryption.** Use maintained crypto libraries and established protocols.
4. **Least privilege.** Per-peer, per-feature authorization; make permissions revocable.
5. **Explicit data sharing.** File transfers and clipboard/notification sharing require opt-in.
6. **No arbitrary remote command execution.** Remote operations use typed allowlists and confirmation for sensitive actions.
7. **Visible state.** Users see connected devices, requested operations, errors and revocations.
8. **No secret material in Git.** Private keys, tokens and credentials stay out of the repository.

## Threats to test

- Discovery spoofing on hostile or shared Wi-Fi
- Unauthorized pairing and device impersonation
- Replay and duplicate remote requests
- Unauthorized transfer or accidental data exposure
- Lost/stolen paired devices; immediate trust revocation
- Privacy leakage from clipboard and notifications
- Resource exhaustion caused by oversized transfers

## Reporting

Until a dedicated security reporting process exists, do not paste exploit details for an unpatched vulnerability in a public issue. A responsible-disclosure process will be documented before public beta.
