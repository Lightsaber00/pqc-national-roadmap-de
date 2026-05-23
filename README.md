# Designing a National Roadmap for Post‑Quantum Cybersecurity

_A strategic transition framework for the Federal Republic of Germany_

> How does a modern state move from RSA and ECDSA to NIST‑standardized PQC without breaking KRITIS and eGovernment?

**Author:** Hendrik Schütz  
**Date:** April 2026  
**Context:** ITU course “Quantum Communications and Post‑Quantum Cybersecurity: The Next Frontier”, Final Policy Analysis Assignment, Theme 1

---

## Why this paper?

Cryptographically relevant quantum computers (CRQCs) will break today’s public‑key cryptography within a realistic 2030–2035 time frame. For data with long‑term confidentiality requirements, Germany is already in the danger zone described by Mosca’s Law: migration time plus threat time exceeds the required secrecy lifetime.[file:1]

At the same time, “Harvest Now, Decrypt Later” (HNDL) attacks are active today: adversaries record encrypted government and KRITIS traffic now to decrypt it once CRQC capability becomes available. German intelligence services have explicitly warned about this threat for government communications, critical infrastructure data, and classified research.[file:1]

This paper answers a simple question: **What would a credible, standards‑aligned national PQC roadmap for Germany actually look like in practice?**[file:1]

---

## What’s in this repository?

- `docs/PQC_National_Roadmap_Schuetz.pdf` – full policy paper (≈10 pages)[file:1]  
- `README.md` – high‑level overview, context, and key design choices

The paper is written from the perspective of a practitioner with operational cybersecurity certifications (CompTIA Security+, Pentest+, CySA+) and ITU training in national cybersecurity strategy, focusing on realistic migration paths instead of purely academic designs.[file:1]

---

## TL;DR of the roadmap

The paper proposes a **five‑phase national transition to post‑quantum cryptography between 2025 and 2032**, grounded in:

- **NIST FIPS 203/204/205**: ML‑KEM (Kyber), ML‑DSA (Dilithium), SLH‑DSA (SPHINCS+)[file:1]  
- **BSI TR‑02102**: German cryptographic baseline and RSA/ECDSA deprecation schedule[file:1]  
- **ENISA PQC guidance & NATO CNSA 2.0**: EU and NATO alignment for defence and cross‑border systems[file:1]

Two architectural principles are non‑negotiable:

- **Cryptographic agility** – abstraction layers to swap primitives without redesigning entire systems  
- **Hybrid schemes** – e.g. X25519 + ML‑KEM‑768 during the transition to defend against both classical and quantum‑capable adversaries[file:1]

---

## The five phases at a glance (2025–2032)

1. **Inventory (2025–2026)**  
   Build a national cryptographic bill of materials (CBOM) for federal IT and KRITIS, with HNDL‑aware risk scoring and a mandatory PQC registry. New procurements must be crypto‑agile from 2026 onward.[file:1]

2. **Pilots (2026–2027)**  
   Roll out hybrid TLS 1.3 (X25519 + ML‑KEM‑768) in federal VPN and web infrastructure, adopt ML‑DSA for federal code signing, and issue BaFin guidance to systemically important financial institutions. BSI updates TR‑02102 with clear RSA/ECDSA deprecation timelines.[file:1]

3. **KRITIS Migration (2027–2029)**  
   Overhaul national PKI (D‑TRUST, Telesec) to support PQC‑capable chains and dual‑algorithm certificates, introduce sector‑specific OT/ICS strategies (PQC gateways vs. hardware refresh), and migrate e‑health records and next‑generation BOS communication systems to PQC.[file:1]

4. **Broad Rollout (2029–2031)**  
   Co‑fund SME migration in KRITIS supply chains via a PQC voucher scheme, require all 16 federal states to publish PQC roadmaps through the IT Planning Council, and integrate PQC into BSI IT‑Grundschutz while funding PQC chairs at leading universities.[file:1]

5. **Audit & Optimization (2031–2032)**  
   Conduct an independent national PQC audit led by the Bundestag IT Committee, validate crypto agility across migrated systems, close remaining RSA/ECC deployments, and establish a permanent BSI quantum threat observatory.[file:1]

---

## Governance architecture in one picture (text‑only here)

The roadmap builds on existing governance (BSI, National Cyber Security Council, IT Planning Council) and adds a cross‑ministry **PQC Steering Committee** to enforce pace and coherence.[file:1]

Key actors:

- **BSI** – technical authority (CBOM registry, TR‑02102 updates, sector guidance, audits, quantum threat observatory)[file:1]  
- **BMI** – legislative owner for KRITIS obligations and inter‑ministerial coordination[file:1]  
- **PQC Steering Committee (proposed)** – cross‑ministry body reporting to the National Cyber Security Council and the Bundestag[file:1]  
- **IT Planning Council** – federal‑state alignment and shared procurement language[file:1]  
- **BfV / BND** – HNDL monitoring and CRQC capability tracking[file:1]  
- **BaFin / BNetzA / Gematik** – sector regulators for finance, telecoms, and healthcare[file:1]  
- **BMWi** – Mittelstand incentives and PQC‑related R&D co‑funding[file:1]

---

## Who is this for?

This work is intended for:

- policymakers and advisors working on national cyber strategies  
- CISOs and security architects in government, KRITIS, and regulated sectors  
- researchers and students exploring practical PQC migration paths

If you want to discuss or build on this roadmap, feel free to open an issue or reach out.

---

## Suggested citation

If you cite this document, you may use:

> Schütz, Hendrik (2026): Designing a National Roadmap for Post‑Quantum Cybersecurity – A Strategic Transition Framework for the Federal Republic of Germany. ITU Course “Quantum Communications and Post‑Quantum Cybersecurity: The Next Frontier”, Final Policy Analysis Assignment, Theme 1.
