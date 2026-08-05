# ATC-DNS — Decentralized DNS

Dezentrales DNS-System für A-TownChain OS — Domain-Namen auf der Chain.

## Features
- **On-Chain DNS** — Domain-Registrierung als Smart Contract
- **Name Resolution** — `atc://myapp.a-town` → ATC-Adresse
- **TLD Management** — `.atc`, `.town`, `.kai` (On-Chain Governance)
- **DNSSEC** — Kryptographische Validierung
- **Caching** — Lokaler Resolver-Cache mit TTL

## Architektur
```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│ Application  │────→│ ATC-DNS      │────→│ Chain Query │
│             │     │ Resolver     │     │ (Smart      │
│ getaddrinfo │←────│ Cache+TTL   │←────│  Contract)  │
└─────────────┘     └──────────────┘     └─────────────┘
```

## Name-Registrierung
```atclang
contract DomainRegistry {
    fn register(name: String, owner: Address) -> bool {
        require(!exists(name), "domain already registered");
        domains[name] = owner;
        emit DomainRegistered(name, owner);
        true
    }
    
    fn resolve(name: String) -> Address {
        domains[name]
    }
}
```

## Verwandte Repos
- [atcnet](https://github.com/A-TownChain-Okosystems/atcnet) — Netzwerk-Stack
- [atc-contracts](https://github.com/A-TownChain-Okosystems/atc-contracts) — Smart Contracts

[agent: aurora-base44-superagent-6a2756186106d6f0fbb105b5]
