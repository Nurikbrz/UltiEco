# UltiEco

![UltiEco logo](assets/ultieco-mark.svg)

**Any device. Any brand. Your rules.**

UltiEco is a proposed **open, extensible, local-first ecosystem** designed to help devices you already own work together — without forcing them to come from one manufacturer.

> **Status: concept / pre-alpha.** None of the synchronization or control features below have been implemented yet.

## The vision

Install UltiEco on supported devices, securely pair them, see them in one place, and share the things you choose to share. Local-network features should work without mandatory cloud accounts.

### Planned features

| Feature | What it should do | Priority |
| --- | --- | --- |
| Device Hub | Discover, pair and view device presence/capabilities | MVP |
| UltiDrop | User-initiated file transfer | MVP |
| UltiClip | Opt-in clipboard sync | Next |
| UltiNotify | Permission-based notification mirroring | Next |
| UltiControl | Allowlisted, approved device actions | Later |
| UltiHandoff | Resume supported activities across devices | Later |
| MiGy companion | Wearable access through a supported phone bridge | Later |

**These are design goals, not released capabilities.** Platform support depends on available APIs and permissions.

## Design first

The identity, logo and cross-device UI concepts live in [**UltiEco on Figma**](https://www.figma.com/design/iYpR16MRFiOzVNPeJsaJsS).

Design v0.1 includes a desktop hub, Android home screen, tablet transfer UI, wearable glance, logo and color system. See [Design language](docs/DESIGN.md).

## Platform rollout

1. **Linux + Android** — first working prototype.
2. **macOS + Windows** — add desktop adapters.
3. **Tablets, wearables, iOS** — explore available integrations; limitations will vary by operating system and vendor.

## Repository layout

```text
UltiEco/
├── apps/
│   ├── desktop/           # Planned desktop UI and OS adapters
│   └── android/           # Planned Android companion
├── packages/
│   ├── core/              # Trusted peers, discovery, transport
│   ├── protocol/          # Versioned messages and capabilities
│   └── ui/                # Shared design tokens and components
├── assets/                # Identity assets
├── docs/
│   ├── PRODUCT.md
│   ├── ARCHITECTURE.md
│   ├── ROADMAP.md
│   ├── SECURITY.md
│   └── DESIGN.md
└── CONTRIBUTING.md
```

## Project principles

- **Cross-brand by design:** no forced same-brand hardware.
- **Local-first:** a local network should be enough for core features.
- **Secure pairing:** approve both endpoints and revoke trust later.
- **Explicit permissions:** no silent sharing of clipboard, notifications or files.
- **Extensible, not magical:** a feature only works where supported by the platform.
- **No arbitrary remote shell execution:** use validated, allowlisted operations.

## Planning documents

- [Product concept](docs/PRODUCT.md)
- [Architecture proposal](docs/ARCHITECTURE.md)
- [Milestones and roadmap](docs/ROADMAP.md)
- [Security principles](docs/SECURITY.md)
- [Brand and interface tokens](docs/DESIGN.md)

## License

**A license has not been selected yet.** The public repository is not automatically open-source licensed. Choose and add an appropriate license before accepting external code contributions.
