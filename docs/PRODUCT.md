# Product concept

## Mission

Make devices from different manufacturers feel like one coherent workspace, while keeping control with the person who owns them.

**Tagline:** Any device. Any brand. Your rules.

## First-user experience

1. Install the client on a Linux desktop and an Android phone.
2. Discover supported peers locally; offer manual pairing as a fallback.
3. Approve a securely authenticated pair on both endpoints.
4. See device name, operating system, connectivity and available capabilities.
5. Initiate an UltiDrop file transfer and approve the receive action.
6. View transfer status and unpair at any time.

## Concepts, not shipped features

| Concept | Function | Phase |
| --- | --- | --- |
| Device Hub | Peer presence, trust and capability display | MVP |
| UltiDrop | Intentional secure file sharing | MVP |
| UltiClip | Opt-in clipboard synchronization | 2 |
| UltiNotify | Supported notifications with fine-grained permissions | 2 |
| UltiControl | Typed, allowlisted remote actions requiring approval | 3 |
| UltiHandoff | App-specific context handoff | 3 |
| MiGy bridge | Wearable requests via phone companion | Future |

## Experience requirements

- Indicate **online**, **offline**, **pairing**, **unavailable** and **permission denied** in text as well as color.
- Never imply a device supports an operation until its capabilities are negotiated.
- Use clear consent before transferring data, especially clipboard or notifications.
- Respect system-level permission dialogs and accessibility preferences.

## Non-goals for the MVP

Cloud storage, cross-network connectivity, full remote desktop, automatic remote shell, generic AI actions, universal iOS background support, and building a custom device OS.

## MVP exit criterion

Linux and Android can discover/pair over the same LAN, reconnect, display state, unpair, and intentionally transfer a file securely.
