# Majikah: Post-Quantum Security. Just like Magic.

![Majikah_Logo](https://github.com/user-attachments/assets/af9d998f-a482-4a79-8633-6f954a440028)

Welcome to the Majikah GitHub organization. We are a privacy-first technology ecosystem dedicated to future-proofing digital sovereignty. In an era of "Harvest Now, Decrypt Later" (HNDL) attacks , we build the tools necessary to ensure your data remains secure—not just today, but in the post-quantum future.

## Our Core Philosophy
We believe identity shouldn't be tied to centralized registries like phone numbers or emails. Instead, we empower users with the Majik Key: a sovereign, BIP-39 mnemonic-based identity system that eliminates social graph exposure and single points of failure.

Key Specialties:

- **Post-Quantum Cryptography**: Implementing NIST-standardized ML-KEM-768 (FIPS-203).
- **Digital Identity**: Sovereign accounts derived locally from 12-word seed phrases.
- **Tamper-Proof Integrity**: Blockchain-like hash chains for immutable communication trails.
- **Radical Transparency**: Open-source SDKs and deterministic protocols

---

## Flagship Product: Majik Message

**Majik Message** is our **zero-trust, post-quantum encrypted messaging and data-relay protocol**.  
It is designed for those who require the highest level of confidentiality, from **legal and healthcare professionals to journalists and privacy-conscious organizations**.

### Dual-Protocol Architecture

| Feature | Real-Time Chats (Ephemeral) | Persistent Threads (Immutable) |
|--------|------------------------------|--------------------------------|
| **Integrity Model** | Non-chained | SHA-256 hash chain |
| **Expiration** | 24h auto-purge | Permanent until consensus deletion |
| **Deletion** | Unilateral / self-destruct | $N$-of-$N$ collaborative consensus |
| **Encryption** | ML-KEM-768 + X25519 + AES-256-GCM | ML-KEM-768 + X25519 + AES-256-GCM |


---
## Developer Resources

We are committed to an **open ecosystem**. Our core cryptographic primitives and messaging logic are available via **Apache 2.0 licensed SDKs**.

### [Majik Message](https://message.majikah.solutions)
Secure messaging platform using Majik Keys

![npm](https://img.shields.io/npm/v/@majikah/majik-message) ![npm downloads](https://img.shields.io/npm/dm/@majikah/majik-message) ![npm bundle size](https://img.shields.io/bundlephobia/min/%40majikah%2Fmajik-message) [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue)

[Read more about Majik Message here](https://majikah.solutions/products/majik-message)

[![Majik Message Thumbnail](https://github.com/user-attachments/assets/d433c6b8-1841-4fa1-a6da-b348029d1dbe)](https://message.majikah.solutions)

> Click the image to try Majik Message live.

[Read Docs](https://majikah.solutions/products/majik-message/docs)


Also available on [Microsoft Store](https://apps.microsoft.com/detail/9pmjgvzzjspn) for free.

[Official Repository](https://github.com/Majikah/majik-message)
[SDK Library](https://www.npmjs.com/package/@majikah/majik-message)

---

### [Majik Key](https://majikah.solutions/sdk/majik-key)
**Majik Key** is a seed phrase account library for creating, managing, and parsing mnemonic-based cryptographic accounts (Majik Keys). Generate deterministic key pairs from BIP39 seed phrases with simple, developer-friendly APIs. Now supports ML-KEM-768 post-quantum key derivation alongside X25519.

![npm](https://img.shields.io/npm/v/@majikah/majik-key) ![npm downloads](https://img.shields.io/npm/dm/@majikah/majik-key) ![npm bundle size](https://img.shields.io/bundlephobia/min/%40majikah%2Fmajik-key) [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue)

[Read Docs](https://majikah.solutions/sdk/majik-key/docs)
[Official Repository](https://github.com/Majikah/majik-key)
[SDK Library](https://www.npmjs.com/package/@majikah/majik-key)

---

### [Majik Envelope](https://majikah.solutions/sdk/majik-envelope)
**Majik Envelope** is the core cryptographic engine of the [Majik Message](https://github.com/Majikah/majik-message) platform. It provides a post-quantum secure "envelope" format that handles message encryption, multi-recipient key encapsulation, and transparent compression using NIST-standardized algorithms.

![npm](https://img.shields.io/npm/v/@majikah/majik-envelope) ![npm downloads](https://img.shields.io/npm/dm/@majikah/majik-envelope) ![npm bundle size](https://img.shields.io/bundlephobia/min/%40majikah%2Fmajik-envelope) [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue)

[Read Docs](https://majikah.solutions/sdk/majik-envelope/docs)
[Official Repository](https://github.com/Majikah/majik-envelope)
[SDK Library](https://www.npmjs.com/package/@majikah/majik-envelope)

---
### [Majik File](https://majikah.solutions/sdk/majik-file)
Post-quantum file encryption for the Majik Message platform. Produces self-contained `.mjkb` binary files — sealed with **ML-KEM-768 + AES-256-GCM**, optionally Zstd-compressed, readable without any network access.

This library is designed to work within the **Majik Message ecosystem**. It expects callers to supply ML-KEM-768 key material from an identity store; it does not generate or persist keys itself.

![npm](https://img.shields.io/npm/v/@majikah/majik-file) ![npm downloads](https://img.shields.io/npm/dm/@majikah/majik-file) ![npm bundle size](https://img.shields.io/bundlephobia/min/%40majikah%2Fmajik-file) [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue)

[Read Docs](https://majikah.solutions/sdk/majik-file/docs)
[Official Repository](https://github.com/Majikah/majik-file)
[SDK Library](https://www.npmjs.com/package/@majikah/majik-file)

---

## The Hybrid Encryption Stack

We use a **defense-in-depth approach** to ensure security against both **classical and quantum threats**:

| Component | Purpose |
|----------|--------|
| **ML-KEM-768 (FIPS-203)** | Post-Quantum Key Encapsulation |
| **X25519** | Classical identity and cryptographic fingerprints |
| **AES-256-GCM** | Symmetric payload encryption |
| **Argon2id** | GPU-resistant passphrase hashing for keys at rest |

---

## Connect with Us

- **Website**: https://majikah.solutions  
- **Verification Tool**: Validate thread integrity at https://message.majikah.solutions/threads/validate  
- **Inquiries**: Majikah Information Technology Solutions

---

## Security Note

Majik Message **does not protect against device compromise or endpoint malware**.

For stronger operational privacy:

- Use a **VPN** or **Tor** if you require IP anonymity.
- User IP addresses **may be visible to the relay infrastructure**.
