# Architecture proposal

> This is a design document, **not** an implemented architecture. Languages and frameworks remain undecided.

## High-level topology

```text
Linux desktop client                       Android companion
┌────────────────────┐                   ┌────────────────────┐
│ UI + OS adapter    │                   │ UI + OS adapter    │
│ Trusted peer store │◄─ secure channel ─►│ Trusted peer store │
│ Device discovery   │                   │ Device discovery   │
└────────┬───────────┘                   └────────┬───────────┘
         │                                        │
         └──── Shared protocol and core APIs ─────┘
```

Each device runs its own local agent or companion. A shared protocol does **not** imply a central server.

## Modules

- **Core:** discovery abstraction, device identity, trusted peers, encrypted communication, connectivity status, transfer coordination.
- **Protocol:** versioned typed messages, request correlation, capability negotiation, error representation, validation.
- **Desktop adapter:** system integrations for supported desktop OSes.
- **Android adapter:** OS permission handling and platform background limits.
- **UI:** a shared design vocabulary with platform-specific affordances.

## Concept message (not stable)

```json
{
  "version": 1,
  "requestId": "example-id",
  "type": "device.status.request",
  "targetId": "paired-device-id"
}
```

Transport must provide authentication, encryption, anti-replay handling and timeouts. An example ID here does not imply an accepted trust relationship.

## Technology candidates, not commitments

- Desktop: Tauri or another maintainable cross-platform shell.
- Core: Rust, TypeScript or another language with solid libraries and tests.
- Android: native app or cross-platform shell with native integration layer.
- Discovery: mDNS where feasible, with manual connection fallback.
- Transport: established authenticated-encryption protocols and vetted libraries; no homemade cryptography.

## Capability negotiation

Actions should be explicitly advertised by the receiving device, with versioned capabilities such as `device.status.v1` or `file.receive.v1`. Authorization is checked **per device and per capability**. Unsupported calls must fail clearly rather than silently.

## Future expansion

Mac/Windows adapters, optional remotely reachable channels, and MiGy via a phone bridge. iOS/wearables are constrained by vendor APIs and OS security boundaries. Remote or high-impact commands should require separate security review.
