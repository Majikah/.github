# Majikah Solutions

![Majikah logo](https://github.com/user-attachments/assets/af9d998f-a482-4a79-8633-6f954a440028)

> **Post-quantum security and software, built around digital trust.**

**Majikah Solutions OPC** is a Philippine post-quantum security and software company developing privacy-first products, cryptographic technology, and bespoke digital solutions for people, creators, developers, businesses, and organizations.

We build practical tools that help people verify digital work, protect communications, manage cryptographic identity, and bring stronger security into everyday software. Our work combines our own products, reusable developer foundations, and custom engineering for organizations.

[**Explore Majikah**](https://majikah.solutions) · [**Meet the company**](https://majikah.solutions/about) · [**Developer resources**](https://developers.majikah.solutions) · [**Contact us**](mailto:business@majikah.solutions)

[![Majik Key technical whitepaper](https://img.shields.io/badge/Technical%20Whitepaper-Zenodo-1682D4?logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.23208491)
[![Public GitHub organization](https://img.shields.io/badge/GitHub-Public%20Repositories-181717?logo=github&logoColor=white)](https://github.com/orgs/Majikah/repositories)
[![npm packages](https://img.shields.io/badge/npm-@majikah-CB3837?logo=npm&logoColor=white)](https://www.npmjs.com/~majikah)

---

## What we do

Majikah brings together three connected areas of work:

| Area | What it means |
|---|---|
| **Software products** | Applications for digital signing, file verification, private communication, identity, and business workflows. **Majik Signature is our flagship product.** |
| **Cryptographic technology** | Shared key architecture, cryptographic libraries, developer SDKs, file formats, and integrations built around established standards. |
| **Bespoke software engineering** | Custom websites, web and desktop applications, APIs, integrations, workflow tools, and security-focused infrastructure for clients. |

Our purpose is to make digital trust practical and accessible. Our mission is to build useful, privacy-first software and cryptographic infrastructure that helps people and organizations protect digital work, verify authenticity, and retain control. We envision a digital environment where privacy, authenticity, and ownership are built into everyday technology—not treated as optional extras.

## Flagship product — [Majik Signature](https://majikah.solutions/products/majik-signature)

[![Majik Signature product preview](https://github.com/user-attachments/assets/781bb778-9535-4b1f-bbc5-820550ecc864)](https://signature.majikah.solutions)

**Sign it. Share it. Verify it.**

Majik Signature is a digital signing and file-verification application designed to make cryptographic proof usable in everyday work. It signs files with a hybrid scheme combining **Ed25519** and **ML-DSA-87 (NIST FIPS 204)**. Recipients can verify signed content without needing the signer's private key or a Majikah account.

Its workflows support documents, images, audio, video, source code, software releases, and other digital files.

**What it does:**

- **Sign and verify locally.** Core signing and verification are designed to run on the user's device. Files are not uploaded just to be signed or verified, and private signing keys remain local.
- **Embed or detach signatures.** Keep signature data with supported files or share a separate .mjksig envelope.
- **Support multi-party workflows.** Signer allowlists, multiple signatures, sealing, and signing-order verification help support review and approval processes.
- **Add independent evidence when needed.** Optional trusted timestamps and Majik Notary blockchain anchoring can extend the workflow; these services require network access and depend on current product/service availability.
- **Automate supported workflows.** The SDK and documented CLI/MCP capabilities provide integration paths for developers and automation.

**Try it or explore the implementation:**

| Resource | Link |
|---|---|
| Web application | [signature.majikah.solutions](https://signature.majikah.solutions) |
| Product information | [Majik Signature](https://majikah.solutions/products/majik-signature) |
| Documentation | [Product documentation](https://majikah.solutions/products/majik-signature/docs) |
| Desktop downloads | [Latest Windows and Linux releases](https://github.com/Majikah/majik-signature-desktop-releases/releases/latest) |
| TypeScript SDK and source | [github.com/Majikah/majik-signature](https://github.com/Majikah/majik-signature) |
| File format | [.mjksig IANA media type](https://www.iana.org/assignments/media-types/application/vnd.majikah.mjksig) |

Core signing and verification are free to use. Optional services such as trusted timestamping and notarization have separate usage terms; see the official product pages for current details.

---

## The Majikah product ecosystem

Majik Signature is the flagship. Other products address related needs and use shared cryptographic foundations where appropriate.

| Product | What it is | Explore |
|---|---|---|
| **[Majik Message](https://majikah.solutions/products/majik-message)** | Encrypted messaging built around cryptographic identity, with post-quantum key encapsulation using ML-KEM-768 (FIPS 203). | [Web app](https://message.majikah.solutions) · [Source and protocol](https://github.com/Majikah/majik-message) |
| **[Majik Buwiz](https://majikah.solutions/products/majik-buwiz)** | Offline-first invoicing and business workflows, with cryptographic integrity for invoice records. | [Product information](https://majikah.solutions/products/majik-buwiz) |
| **[Majik Universal ID](https://majikah.solutions/products/majik-universal-id)** | A public cryptographic identity layer that associates a profile with verifiable signing keys. | [Identity profiles](https://id.majikah.solutions) · [Source](https://github.com/Majikah/majik-universal-id) |
| **[Majik SLink](https://majikah.solutions/products/majik-slink)** | Signed claims that associate a cryptographic identity with a URL, supporting ownership, attribution, and reference use cases. | [Product information](https://majikah.solutions/products/majik-slink) · [Source](https://github.com/Majikah/majik-slink) |

Product availability, platform support, and feature maturity can vary. Use each product's official page, documentation, and release notes for the current status.

---

## The shared foundation — [Majik Key](https://github.com/Majikah/majik-key)

Majik Key is the shared cryptographic identity library used across parts of the ecosystem. It derives a set of classical and post-quantum keys from a BIP-39 mnemonic and protects stored private-key material with authenticated encryption and passphrase-based key derivation.

The default core key set includes:

| Key identifier | Algorithm | Role |
|---|---|---|
| classic:x25519 | X25519 | Classical key agreement and identity-related operations |
| classic:ed25519 | Ed25519 | Classical digital signatures |
| pq:ml-kem-768 | ML-KEM-768 — NIST FIPS 203 | Post-quantum key encapsulation |
| pq:ml-dsa-87 | ML-DSA-87 — NIST FIPS 204 | Post-quantum digital signatures |

A single user-controlled cryptographic identity can support multiple applications, rather than requiring a completely unrelated key set for every product. Additional algorithms and integrations have their own maturity and support status; consult the library documentation before relying on experimental or opt-in features.

- [TypeScript source](https://github.com/Majikah/majik-key)
- [npm package](https://www.npmjs.com/package/@majikah/majik-key)
- [Technical whitepaper](https://doi.org/10.5281/zenodo.23208491)
- [Whitepaper overview](https://majikah.solutions/articles/majik-key-whitepaper)

> **Protect your recovery phrase.** A BIP-39 mnemonic is a high-value secret. Anyone who obtains it may be able to recreate the associated keys. Keep it offline, never share it, and never paste it into a website or commit it to source control.

---

## Open-source projects and developer tools

Majikah publishes selected libraries, SDKs, specifications, and implementation resources for developers who want to inspect or integrate the technology. The organization also maintains application, client, and language-specific repositories.

### Cryptographic and data libraries

| Repository | Purpose |
|---|---|
| [`majik-key`](https://github.com/Majikah/majik-key) | Multi-algorithm cryptographic identity, key derivation, and encrypted key storage. |
| [`majik-signature`](https://github.com/Majikah/majik-signature) | Hybrid signing, file verification, signature envelopes, multi-party signing, and sealing. |
| [`majik-envelope`](https://github.com/Majikah/majik-envelope) | Multi-recipient encrypted envelope primitives built around post-quantum key encapsulation. |
| [`majik-file`](https://github.com/Majikah/majik-file) | Platform-agnostic encrypted file container and related file workflows. |
| [`majik-message`](https://github.com/Majikah/majik-message) | Messaging domain and protocol implementation. |
| [`majik-universal-id`](https://github.com/Majikah/majik-universal-id) | Cryptographic identity data model and verification workflows. |
| [`majik-slink`](https://github.com/Majikah/majik-slink) | Signed URL claims and identity-to-resource association. |
| [`majik-invoice`](https://github.com/Majikah/majik-invoice) | TypeScript invoice domain model and optional cryptographic envelope. |

### Service integrations

| Repository | Purpose |
|---|---|
| [`majikah-sdk`](https://github.com/Majikah/majikah-sdk) | TypeScript client for public Majikah services, including MUID, timestamping, SLink, and file notarization. |
| [`majik-notary`](https://github.com/Majikah/majik-notary) | Blockchain anchoring and independent verification for sealed files. |
| [`majik-api`](https://github.com/Majikah/majik-api) | API-key lifecycle and policy-management library. |

These projects have different release cycles, dependencies, and maturity levels. Each repository is the source of truth for its installation instructions, license, API stability, changelog, and security guidance. Public source code supports inspection; it is not, by itself, an independent security audit.

### Start building

For local TypeScript cryptographic workflows, start with the core packages:

```bash
npm install @majikah/majik-key @majikah/majik-signature
```

Then follow the installation and quick-start guidance in the relevant repository. Browse [all public repositories](https://github.com/orgs/Majikah/repositories) or [all published npm packages](https://www.npmjs.com/~majikah).

For API-backed integrations, visit the [Majikah Developer Portal](https://developers.majikah.solutions). Public API access is currently offered through an early-access application and is subject to approval.

---

## How we approach security

We aim to make security understandable without hiding implementation details or overstating what technology can guarantee.

- **Standards-led engineering.** Where post-quantum cryptography is used, relevant components build on published standards such as ML-KEM (FIPS 203) and ML-DSA (FIPS 204).
- **Privacy and user control.** We design for local-first operation, data minimization, and user-controlled cryptographic identity where the product and use case allow it.
- **Verifiable outcomes.** Signatures, file formats, and public proofs are designed so that the result can be checked independently using the appropriate public keys, specifications, and verification tools.
- **Clear limitations.** We distinguish algorithm standards from product certification, and cryptographic verification from real-world identity or legal authority.

### Security context and limitations

Using a NIST-standardized algorithm does **not** mean a Majikah product is NIST-certified or independently audited. We do not present public source code, a technical whitepaper, test coverage, or antivirus-vendor whitelisting as substitutes for a third-party security audit of the complete product.

A valid digital signature shows that specific content verifies against a particular public key. It does not, by itself, prove the real-world identity of the key holder, establish that the signer had legal authority, or guarantee that a document is legally valid in every jurisdiction. Verify identity and authority through a trusted process appropriate to your use case.

Post-quantum cryptography addresses specific classes of cryptographic risk; it does not protect against compromised devices, malware, exposed recovery phrases, weak passphrases, social engineering, or implementation defects. Review product-specific threat models and operational guidance before deployment.

---

## The company

**Majikah Solutions OPC** is a founder-led Philippine software company. We develop our own products and cryptographic technology while providing bespoke software engineering for organizations that need practical, security-conscious digital solutions.

**Founded and led by Josef Elijah Fabian (Zelijah), Founder & Lead Developer.** His background in music and creative production informs Majikah's focus on authorship, document integrity, digital identity, and the ability to verify work independently.

Our goals are to:

1. Make practical, standards-based security more accessible to individuals, creators, teams, and businesses.
2. Build reusable cryptographic foundations and developer tools that other products and teams can integrate.
3. Grow through responsible product adoption and long-term relationships with technology, distribution, research, and institutional partners.

Learn more about [the company and its founder](https://majikah.solutions/about).

---

## Work with us

We welcome conversations with people and organizations who share an interest in practical security and trustworthy digital systems.

- **Developers:** explore the source repositories, SDKs, technical publications, and developer portal.
- **Technology and integration partners:** discuss product integrations, co-development, and complementary infrastructure.
- **Businesses and organizations:** discuss custom websites, applications, APIs, workflow systems, and security-focused engineering.
- **Distribution and institutional partners:** explore ways to bring Majikah products and services to relevant communities and markets.
- **Investors and strategic stakeholders:** contact us to discuss the company's direction, product portfolio, and potential collaboration.

## Connect

| | |
|---|---|
| **Company website** | [majikah.solutions](https://majikah.solutions) |
| **About Majikah** | [Company, mission, and founder](https://majikah.solutions/about) |
| **Flagship product** | [Majik Signature](https://majikah.solutions/products/majik-signature) |
| **Developer portal** | [developers.majikah.solutions](https://developers.majikah.solutions) |
| **Public repositories** | [github.com/Majikah](https://github.com/Majikah) |
| **npm packages** | [npmjs.com/~majikah](https://www.npmjs.com/~majikah) |
| **Business and partnership inquiries** | [business@majikah.solutions](mailto:business@majikah.solutions) |
| **Founder** | [Josef Elijah Fabian on GitHub](https://github.com/jedlsf) · [thezelijah.world](https://thezelijah.world) |

---

<p align="center">
  <strong>Digital trust, made practical.</strong><br>
  Built in the Philippines. Designed to be verified.<br><br>
  <a href="https://majikah.solutions">majikah.solutions</a>
</p>
