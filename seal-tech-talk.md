---
marp: true
paginate: true
footer: "Seal"
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

/* ============================================================
   SUI CORPORATE THEME — Embedded CSS
   Palette: black bg · white headings · #8B8B8B body · #4DA2FF accent
   Canonical size: 1280 × 720 (16:9)
   ============================================================ */

/* ----- Base Section ----- */
section {
  background: #000000;
  color: #8B8B8B;
  font-family: 'Inter', 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-size: 22px;
  font-weight: 400;
  line-height: 1.5;
  padding: 60px;
  width: 1280px;
  height: 720px;
  position: relative;
}

/* ----- Typography ----- */
section h1 {
  color: #FFFFFF;
  font-size: 42px;
  font-weight: 700;
  line-height: 1.2;
  margin: 0 0 16px 0;
}

section h2 {
  color: #FFFFFF;
  font-size: 32px;
  font-weight: 600;
  line-height: 1.3;
  margin: 0 0 12px 0;
}

section h3 {
  color: #FFFFFF;
  font-size: 24px;
  font-weight: 600;
  line-height: 1.3;
  margin: 0 0 8px 0;
}

section h4 {
  color: #8B8B8B;
  font-size: 20px;
  font-weight: 500;
  line-height: 1.4;
  margin: 0 0 8px 0;
}

section p {
  margin: 0 0 12px 0;
}

section strong {
  color: #FFFFFF;
  font-weight: 600;
}

section em {
  color: #4DA2FF;
  font-style: normal;
}

section a {
  color: #4DA2FF;
  text-decoration: none;
}

section code {
  background: #1A1A1A;
  color: #4DA2FF;
  padding: 2px 6px;
  border-radius: 4px;
  font-size: 0.9em;
}

section pre {
  background: #0A0A0A;
  border: 1px solid #3A3A3A;
  border-radius: 8px;
  padding: 20px;
  margin: 12px 0;
}

section pre code {
  background: transparent;
  padding: 0;
}

section ul, section ol {
  margin: 0 0 12px 0;
  padding-left: 24px;
}

section li {
  margin-bottom: 6px;
}

section li::marker {
  color: #4DA2FF;
}

section blockquote {
  border-left: 3px solid #4DA2FF;
  padding-left: 16px;
  margin: 12px 0;
  color: #AAAAAA;
}

section table {
  width: 100%;
  border-collapse: collapse;
  margin: 12px 0;
}

section th {
  color: #FFFFFF;
  font-weight: 600;
  text-align: left;
  padding: 10px 16px;
  border-bottom: 2px solid #4DA2FF;
}

section td {
  padding: 8px 16px;
  border-bottom: 1px solid #1A1A1A;
}

section hr {
  border: none;
  border-top: 1px dashed #3A3A3A;
  margin: 24px 0;
}

/* ----- Pagination ----- */
section::after {
  color: #4DA2FF;
  font-size: 14px;
  font-weight: 600;
  background: rgba(77, 162, 255, 0.1);
  border-radius: 12px;
  padding: 2px 10px;
}

/* ----- Footer ----- */
section footer {
  color: #8B8B8B;
  font-size: 14px;
  position: absolute;
  bottom: 24px;
  left: 60px;
}

/* ----- Header ----- */
section header {
  color: #4DA2FF;
  font-size: 14px;
  font-weight: 500;
  position: absolute;
  top: 24px;
  right: 60px;
}

/* ============================================================
   GRID SYSTEM
   ============================================================ */

section .grid {
  display: grid;
  gap: 24px;
  width: 100%;
  height: auto;
}

section .col {
  display: flex;
  flex-direction: column;
}

section .col h3 {
  margin-bottom: 8px;
}

section .col p {
  font-size: 18px;
  margin: 0;
}

/* Blue square marker for column headings */
section .col h3::before {
  content: '';
  display: inline-block;
  width: 8px;
  height: 8px;
  background: #4DA2FF;
  margin-right: 10px;
  vertical-align: middle;
}

/* Dotted separator above columns */
section .col {
  border-top: 1px dashed #3A3A3A;
  padding-top: 16px;
}

/* Card item for list layouts */
section .card {
  background: #0A0A0A;
  border: 1px solid #1A1A1A;
  border-radius: 8px;
  padding: 16px 20px;
  margin-bottom: 8px;
}

section .card h4 {
  color: #FFFFFF;
  margin: 0 0 4px 0;
}

section .card p {
  margin: 0;
  font-size: 16px;
}

/* ============================================================
   LAYOUT: lead — Cover / Title Slide
   ============================================================ */
section.lead {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding-bottom: 80px;
}

section.lead h1 {
  font-size: 64px;
  font-weight: 700;
  margin-bottom: 16px;
}

section.lead p {
  font-size: 24px;
  color: #8B8B8B;
  max-width: 70%;
}

/* ============================================================
   LAYOUT: cols-3 — Three Columns
   ============================================================ */
section.cols-3 .grid {
  grid-template-columns: repeat(3, 1fr);
  margin-top: 24px;
}

/* ============================================================
   LAYOUT: cols-2-center — Two Columns, centered title
   ============================================================ */
section.cols-2-center {
  text-align: center;
}

section.cols-2-center h1 {
  text-align: center;
  width: 100%;
}

section.cols-2-center .grid {
  grid-template-columns: repeat(2, 1fr);
  margin-top: 24px;
  text-align: left;
}

/* ============================================================
   LAYOUT: grid-2x2 — 2×2 Grid, centered title
   ============================================================ */
section.grid-2x2 {
  text-align: center;
}

section.grid-2x2 h1 {
  text-align: center;
  width: 100%;
}

section.grid-2x2 .grid {
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, auto);
  margin-top: 24px;
  text-align: left;
}

/* ============================================================
   LAYOUT: split-right — Title+body right-aligned
   ============================================================ */
section.split-right {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  text-align: right;
}

section.split-right h1,
section.split-right p {
  max-width: 55%;
}

/* ============================================================
   LAYOUT: list-right — Title right, stacked cards
   ============================================================ */
section.list-right {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: start;
}

section.list-right .content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
}

section.list-right .cards {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

/* ============================================================
   PRODUCT HERO SLIDES
   ============================================================ */
section.product-seal {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  overflow: hidden;
}

section.product-seal::before {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 160px;
  font-weight: 700;
  color: rgba(255, 255, 255, 0.03);
  text-transform: uppercase;
  white-space: nowrap;
  pointer-events: none;
  z-index: 0;
  content: 'SEAL';
}

section.product-seal > * {
  position: relative;
  z-index: 1;
}

section.product-seal h1 {
  font-size: 56px;
  margin-top: 16px;
}

section.product-seal p {
  font-size: 22px;
  max-width: 600px;
}

/* ============================================================
   PRODUCT CONTENT SLIDES
   ============================================================ */
section.product-seal-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: center;
}

section.product-seal-content .content {
  display: flex;
  flex-direction: column;
}

section.product-seal-content .illustration {
  display: flex;
  align-items: center;
  justify-content: center;
}

/* ============================================================
   UTILITY CLASSES
   ============================================================ */
section .text-center { text-align: center; }
section .text-right { text-align: right; }
section .accent { color: #4DA2FF; }
section .muted { color: #555555; }
section .small { font-size: 16px; }
section .large { font-size: 28px; }
section .no-border { border-top: none; padding-top: 0; }
section .center {
  display: flex;
  align-items: center;
  justify-content: center;
}
section .badge {
  display: inline-block;
  background: rgba(77, 162, 255, 0.15);
  color: #4DA2FF;
  padding: 4px 12px;
  border-radius: 16px;
  font-size: 14px;
  font-weight: 500;
}
section .spacer {
  height: 24px;
}
</style>

<!-- ============================================================
     SLIDE 1 — Hero
     ============================================================ -->

<!-- _class: product-seal -->
<!-- _paginate: false -->

# Seal

Decentralized secrets management for Sui

---

<!-- ============================================================
     SLIDE 2 — The Problem
     ============================================================ -->

# The Problem

Blockchains give us **authentication** — proving *who* you are and *what* you own.

But they lack native **encryption** — controlling *who can read* data.

- On-chain data is public by default
- Off-chain storage has no programmable access control
- Traditional KMS solutions are centralized and opaque

**Seal bridges this gap** — programmable encryption with on-chain access policies and decentralized key servers.

---

<!-- ============================================================
     SLIDE 3 — How Seal Works
     ============================================================ -->

<!-- _class: cols-3 -->

# How Seal Works

<div class="grid">
<div class="col">

### On-Chain Policies

Access control written in **Move**. `seal_approve*` functions define who can decrypt. Evaluated read-only via dry run — no gas, no state changes.

</div>
<div class="col">

### Off-Chain Key Servers

Each holds an **IBE master secret key**. Derive identity-specific decryption keys on demand. Stateless, lightweight, horizontally scalable.

</div>
<div class="col">

### Client-Side Encryption

The SDK encrypts and decrypts **locally**. Key servers never see your data. Threshold encryption across multiple independent servers.

</div>
</div>

---

<!-- ============================================================
     SLIDE 4 — IBE Identity Model
     ============================================================ -->

<!-- _class: product-seal-content -->

<div class="content">

# IBE Identity Model

Seal uses *Identity-Based Encryption* where each identity is a namespace-qualified byte string:

`[PackageId] || [id]`

- **PackageId** — Your Move package address acts as the namespace
- **id** — Encodes policy conditions (address, timestamp, subscription ID...)
- **seal_approve*** — The Move function that gates key derivation

The domain of identities is unbounded — any byte string works.

</div>

<div class="illustration">

| Component | Role |
|-----------|------|
| `PackageId` | Namespace isolation |
| `id` | Policy-specific condition |
| `seal_approve*` | On-chain gatekeeper |
| Key Server | Derives keys per identity |

</div>

---

<!-- ============================================================
     SLIDE 5 — seal_approve Example
     ============================================================ -->

# seal_approve Example

Time-lock encryption: data unlocks after a specific timestamp.

```move
module patterns::tle;

use sui::bcs;
use sui::clock;

const ENoAccess: u64 = 1;

entry fun seal_approve(id: vector<u8>, c: &clock::Clock) {
    let mut prepared: BCS = bcs::new(id);
    let t = prepared.peel_u64();
    let leftovers = prepared.into_remainder_bytes();
    assert!((leftovers.length() == 0) && (c.timestamp_ms() >= t), ENoAccess);
}
```

Identity = `[PackageId][bcs::to_bytes(T)]` — anyone can decrypt once time exceeds `T`.

---

<!-- ============================================================
     SLIDE 6 — Encrypt & Decrypt
     ============================================================ -->

<!-- _class: cols-2-center -->

# Encrypt & Decrypt

<div class="grid">
<div class="col">

### Encryption

1. Choose key servers and threshold
2. Call `client.encrypt()` with package ID + identity
3. SDK encrypts locally using server public keys
4. Store encrypted bytes anywhere (Walrus, Sui, S3)

**No key server contact needed to encrypt.**

</div>
<div class="col">

### Decryption

1. User authorizes a *session key* (wallet signature)
2. Build a PTB calling `seal_approve*`
3. Call `client.decrypt()` — SDK contacts key servers
4. Servers evaluate policy via dry run, return derived keys
5. SDK decrypts locally with threshold shares

</div>
</div>

---

<!-- ============================================================
     SLIDE 7 — Access Control Patterns
     ============================================================ -->

<!-- _class: grid-2x2 -->

# Access Control Patterns

<div class="grid">
<div class="col">

### Private Data

Single owner controls encrypted content. Ownership transfer moves decryption rights. For personal storage, private NFTs.

</div>
<div class="col">

### Allowlist

Shared object maintains approved addresses. Update the list without re-encrypting. For partner-only data rooms, gated drops.

</div>
<div class="col">

### Subscription

Time-limited pass with price and duration. Expires automatically — no data movement needed. For premium content, paid APIs.

</div>
<div class="col">

### Time-Lock

Data unlocks at a future timestamp. Before: no one can decrypt. After: anyone can. For voting, auctions, MEV protection.

</div>
</div>

---

<!-- ============================================================
     SLIDE 8 — Trust & Threshold
     ============================================================ -->

<!-- _class: cols-2-center -->

# Trust & Threshold

<div class="grid">
<div class="col">

### Privacy Guarantee

If fewer than **t** key servers are compromised, the adversary **cannot** learn the encrypted message.

| Config | Tolerates |
|--------|-----------|
| 1-of-1 | No compromise |
| 2-of-3 | 1 compromised |
| 3-of-5 | 2 compromised |

</div>
<div class="col">

### Liveness Guarantee

If at least **t** key servers are available, decryption **always** succeeds.

| Config | Tolerates |
|--------|-----------|
| 1-of-1 | 0 unavailable |
| 2-of-3 | 1 unavailable |
| 3-of-5 | 2 unavailable |

</div>
</div>

---

<!-- ============================================================
     SLIDE 9 — Getting Started
     ============================================================ -->

<!-- _class: list-right -->

<div class="content">

# Getting Started

Four steps from zero to decrypting your first secret on testnet.

</div>

<div class="cards">
<div class="card">

#### 1. Install the SDK

`npm install @mysten/seal`

</div>
<div class="card">

#### 2. Choose Key Servers

Select from verified testnet providers — six available with open access.

</div>
<div class="card">

#### 3. Define Access Policy

Write a `seal_approve*` function in Move. Deploy with `sui client publish`.

</div>
<div class="card">

#### 4. Encrypt & Decrypt

Call `client.encrypt()` to seal data, `client.decrypt()` to retrieve it.

</div>
</div>

---

<!-- ============================================================
     SLIDE 10 — Security Essentials
     ============================================================ -->

<!-- _class: cols-3 -->

# Security Essentials

<div class="grid">
<div class="col">

### Threshold Config

Choose *2-of-3* as a good default. Balance privacy (more servers) against availability (fewer needed). Server set is **fixed** once data is encrypted.

</div>
<div class="col">

### Key Server Vetting

Treat server selection as a trust decision. Diversify operators, jurisdictions, infrastructure. Establish agreements on availability and incident response.

</div>
<div class="col">

### Envelope Encryption

For large or long-lived data: encrypt with your own key, then encrypt *that key* with Seal. Rotate servers without re-encrypting stored content.

</div>
</div>

---

<!-- ============================================================
     SLIDE 11 — Key Takeaway
     ============================================================ -->

<!-- _class: split-right -->

# Programmable Encryption

Seal lets you define **who** can decrypt **what**, and **when** — using Move code you already know. Combined with threshold key servers, it brings programmable secrets management to Sui without trusting any single party.

---

<!-- ============================================================
     SLIDE 12 — Resources
     ============================================================ -->

<!-- _class: lead -->

# Resources

**SDK** — `npm install @mysten/seal`
**Docs** — seal-docs.wal.app
**GitHub** — github.com/MystenLabs/seal
**Discord** — Seal channel on Sui Discord
