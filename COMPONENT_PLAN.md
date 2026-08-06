# 📋 Komponenten-Plan — atc-dns

> **Erstellt:** 2026-08-06 | **Agent:** Aurora (MasterBrain · Base44)

## Übersicht

**Repo:** atc-dns  
**Name:** ATC DNS — Domain Name System  
**Beschreibung:** Dezentrales DNS für A-TownChain Nodes. On-chain Domain-Resolution, Caching, DNSSEC-Äquivalent.  
**Layer:** L5 — Networking  
**Sprint:** 2.2  
**ATC-Standards:** ATC-01

---

## Komponenten

### 1. resolver.atc

**Beschreibung:** DNS-Resolver: query, recursive lookup, caching, TTL

**Status:** 📋 GEPLANT

**Schnittstellen:**
- Eingabe: —
- Ausgabe: —
- Abhängigkeiten: ATCLang Stdlib

**Akzeptanzkriterien:**
1. Datei existiert und parst mit ATCLang v0.3 Parser
2. Alle öffentlichen Funktionen haben Type-Signatures
3. Modul ist im FILE_REGISTER.md eingetragen

---

### 2. records.atc

**Beschreibung:** DNS-Records: A, AAAA, CNAME, MX, TXT, ATC-specific (CHAIN, NODE)

**Status:** 📋 GEPLANT

**Schnittstellen:**
- Eingabe: —
- Ausgabe: —
- Abhängigkeiten: ATCLang Stdlib

**Akzeptanzkriterien:**
1. Datei existiert und parst mit ATCLang v0.3 Parser
2. Alle öffentlichen Funktionen haben Type-Signatures
3. Modul ist im FILE_REGISTER.md eingetragen

---

### 3. cache.atc

**Beschreibung:** Cache-Manager: LRU cache, TTL expiry, prefetch, negative caching

**Status:** 📋 GEPLANT

**Schnittstellen:**
- Eingabe: —
- Ausgabe: —
- Abhängigkeiten: ATCLang Stdlib

**Akzeptanzkriterien:**
1. Datei existiert und parst mit ATCLang v0.3 Parser
2. Alle öffentlichen Funktionen haben Type-Signatures
3. Modul ist im FILE_REGISTER.md eingetragen

---

### 4. zones.atc

**Beschreibung:** Zone-Verwaltung: zone files, transfers, signing

**Status:** 📋 GEPLANT

**Schnittstellen:**
- Eingabe: —
- Ausgabe: —
- Abhängigkeiten: ATCLang Stdlib

**Akzeptanzkriterien:**
1. Datei existiert und parst mit ATCLang v0.3 Parser
2. Alle öffentlichen Funktionen haben Type-Signatures
3. Modul ist im FILE_REGISTER.md eingetragen

---

### 5. dnssec.atc

**Beschreibung:** Chain-based DNSSEC: cryptographic proof, trust anchors

**Status:** 📋 GEPLANT

**Schnittstellen:**
- Eingabe: —
- Ausgabe: —
- Abhängigkeiten: ATCLang Stdlib

**Akzeptanzkriterien:**
1. Datei existiert und parst mit ATCLang v0.3 Parser
2. Alle öffentlichen Funktionen haben Type-Signatures
3. Modul ist im FILE_REGISTER.md eingetragen

---

## Implementierungs-Reihenfolge

1. `resolver.atc` — DNS-Resolver
2. `records.atc` — DNS-Records
3. `cache.atc` — Cache-Manager
4. `zones.atc` — Zone-Verwaltung
5. `dnssec.atc` — Chain-based DNSSEC

## Test-Strategie

1. Parse-Test: Jede .atc Datei muss mit ATCLang v0.3 Parser parsen
2. Unit-Tests: Mindestens 3 Tests pro Komponente
3. Integration-Test: Komponenten interagieren korrekt
4. Coverage-Ziel: >80%

## Dokumentations-Requirements

- ARCHITECTURE.md: Architektur-Baum + Komponenten-Übersicht ✅
- COMPONENT_PLAN.md: Dieser Plan ✅
- FILE_REGISTER.md: Datei-Liste ✅
- STATUS.md: Aktueller Status ✅
- ROADMAP.md: Sprint-Zuordnung ✅
- CHANGELOG.md: Änderungs-Historie ✅

---
*Auto-generiert 2026-08-06 · Aurora (MasterBrain · Base44)*
