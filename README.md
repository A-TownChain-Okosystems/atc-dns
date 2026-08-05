# atc-dns

Dezentraler DNS-Resolver für A-TownChain P2P-Netzwerk.

## Features (geplant)
- DID-basierte Namensauflösung (DID → IP:Port)
- DNS-Caching mit TTL
- Record-Typen: A, AAAA, CNAME, TXT, MX, SRV
- P2P-Propagation über Gossip-Protokoll
- Integration mit atc-shivacore/tcpip.rs
- DNS-Over-HTTPS (DoH) Support
- Anti-Spoofing (Ed25519 Signaturen)

## Build
```bash
cargo build --target x86_64-unknown-none
```

## Abhängigkeiten
- [atc-shivacore](https://github.com/A-TownChain-Okosystems/atc-shivacore) — TCP/IP-Stack, DID

## Status
- Initial: Repo erstellt 05.08.2026
- Sprache: Rust (no_std, Kernel-Modul)

---
Copyright © Michael Wroblewski / A-TownChain-Okosystems. All Rights Reserved.
