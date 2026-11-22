# Majikah Solutions

![Majikah logo](https://github.com/user-attachments/assets/af9d998f-a482-4a79-8633-6f954a440028)

> **Post-quantum security and software, built around digital trust.**

**Majikah Solutions OPC** is a Philippine software and cryptographic technology company building privacy-first products, practical security infrastructure, and bespoke digital solutions for individuals, creators, developers, businesses, and organizations.

We build tools for digital signing and verification, private communication, cryptographic identity, verifiable online presence, and business workflows. Our work connects products people can use, reusable foundations developers can inspect and integrate, and tailored engineering for organizations.

[**Explore Majikah**](https://majikah.solutions) · [**About the company**](https://majikah.solutions/about) · [**Developer portal**](https://developers.majikah.solutions) · [**Contact us**](mailto:business@majikah.solutions)

[![Majik Key technical whitepaper](https://img.shields.io/badge/Technical%20Whitepaper-Zenodo-1682D4?logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.23208491)
[![Public GitHub organization](https://img.shields.io/badge/GitHub-Public%20Repositories-181717?logo=github&logoColor=white)](https://github.com/orgs/Majikah/repositories)
[![npm packages](https://img.shields.io/badge/npm-@majikah-CB3837?logo=npm&logoColor=white)](https://www.npmjs.com/~majikah)

---

## Official startup recognition

On **November 22, 2026**, Majikah Solutions OPC was recognized as a **Qualified Startup Business** under the Philippine Innovative Startup Act (Republic Act No. 11337), following verification by the ISA Review Committee. The Department of Information and Communications Technology issued the company's Certificate of Startup Registration, control number **ISA-2026-00024**, valid for one year from issuance.

This is a **company-level startup recognition**. It is not a government endorsement of an individual Majikah product, a product certification, a software security audit, or an automatic award of grants, subsidies, or other benefits.

- [View the company's Startup Philippines profile](https://startup.gov.ph/startups/view/?id=6a71f10688cff71ca40b9fcf)
- [Verify Certificate ISA-2026-00024](https://startup.gov.ph/verify/ISA-2026-00024)
- [Read the recognition announcement](https://majikah.solutions/articles/majikah-startup-registration-philippines)

---

## What we do

Majikah brings together three connected areas of work:

| Area | What it means |
|---|---|
| **Software products** | Applications for digital signing, file verification, private communication, cryptographic identity, verifiable online presence, and business workflows. **Majik Signature is our flagship product.** |
| **Cryptographic technology** | Shared key architecture, cryptographic libraries, developer SDKs, file formats, and service integrations built around established standards. |
| **Bespoke software engineering** | Custom websites, web and desktop applications, APIs, integrations, workflow tools, and security-focused infrastructure for clients. |

Our purpose is to make digital trust practical and accessible. We aim to build useful, privacy-first software and cryptographic infrastructure that helps people and organizations protect digital work, verify authenticity, and retain control.

## Flagship product — [Majik Signature](https://majikah.solutions/products/majik-signature)

[![Majik Signature product preview](https://github.com/user-attachments/assets/781bb778-9535-4b1f-bbc5-820550ecc864)](https://signature.majikah.solutions)

**Sign it. Share it. Verify it.**

Majik Signature is a digital signing and file-verification application for documents, PDFs, Office files, images, audio, video, source code, archives, and other digital assets. Its hybrid signature combines **Ed25519** with **ML-DSA-87 (NIST FIPS 204)**; both signatures must verify.

Core signing and verification are designed to run locally on the user's device. Files do not need to be uploaded just to be signed or verified, private signing keys remain local, and core offline use does not require an account or an internet connection.

### What it supports

- **Local signing and verification.** Verify signed content using public keys without access to the signer's private key.
- **Embedded and detached signatures.** Keep signature data with supported file formats or use a separate `.mjksig` signature envelope.
- **Folder manifests.** Use `.mjksmap` to represent and verify signed folder contents.
- **Multi-party signing and SignRoom.** Support signer allowlists, participant workflows, collaboration, visual stamps and revisions, audit evidence, and retention-oriented archives.
- **Native Rust foundation.** Majik Signature 1.0.0 moved key management, signing, verification, and file-processing operations onto a native Rust foundation, with zeroization-aware secret handling and native file workflows.
- **Automation paths.** The `mjksig` CLI and `mjksig-mcp` expose signing requests, verification, key/contact operations, and timestamp-related workflows. The documented local named-pipe bridge to the desktop app is Windows-specific; operations that create signatures or seals still require explicit in-app approval.
- **Optional trust services.** Trusted Timestamps can provide independently verifiable evidence of signing time. Majik Notary can anchor a sealed content hash on Solana Mainnet; the original file is not sent to the chain.

**Try it or explore the implementation:**

| Resource | Link |
|---|---|
| Web application | [signature.majikah.solutions](https://signature.majikah.solutions) |
| Product information | [Majik Signature](https://majikah.solutions/products/majik-signature) |
| Product documentation | [Signing, verification, SignRoom, CLI/MCP, and more](https://majikah.solutions/products/majik-signature/docs) |
| Desktop downloads | [Latest Windows and Linux releases](https://github.com/Majikah/majik-signature-desktop-releases/releases/latest) |
| TypeScript source | [github.com/Majikah/majik-signature](https://github.com/Majikah/majik-signature) |
| Rust implementation | [github.com/Majikah/majik-signature-rs](https://github.com/Majikah/majik-signature-rs) |
| IANA file media type | [application/vnd.majikah.mjksig](https://www.iana.org/assignments/media-types/application/vnd.majikah.mjksig) |
| IANA folder-map media type | [application/vnd.majikah.mjksmap](https://www.iana.org/assignments/media-types/application/vnd.majikah.mjksmap) |

The `.mjksig` and `.mjksmap` media types are registered with IANA. Optional services such as trusted timestamping and notarization have separate usage terms; consult the product pages for current availability and details.

---

## The Majikah product ecosystem

Majik Signature is the flagship. Other products address connected needs and share cryptographic foundations where appropriate.

| Product | What it is | Explore |
|---|---|---|
| **[Majik Message](https://majikah.solutions/products/majik-message)** | Private messaging built around cryptographic identity, with post-quantum key encapsulation, encrypted file sharing, and voice communication. | [Web app](https://message.majikah.solutions) · [Source](https://github.com/Majikah/majik-message) |
| **[Majik Buwiz](https://majikah.solutions/products/majik-buwiz)** | Offline-first invoice management for Windows, with cryptographic integrity built into invoice workflows. | [Product information](https://majikah.solutions/products/majik-buwiz) |
| **[Majik Universal ID](https://majikah.solutions/products/majik-universal-id)** | A cryptographic identity profile associated with a Majik Key account and its signing keys. Optional identity verification adds a separate real-world identity signal. | [Public identity profiles](https://id.majikah.solutions) · [Source](https://github.com/Majikah/majik-universal-id) |
| **[Majik SLink](https://majikah.solutions/products/majik-slink)** | Signed claims associating a cryptographic identity with a public URL, for ownership, attribution, or reference use cases. | [SLink](https://slink.majikah.solutions) · [Source](https://github.com/Majikah/majik-slink) |

Product availability, supported platforms, and feature maturity can vary. Each product's official page, documentation, and release notes are the source of truth for its current status.

---

## The shared cryptographic foundation — [Majik Key](https://github.com/Majikah/majik-key)

Majik Key is the shared cryptographic identity library used across parts of the ecosystem. It derives classical and post-quantum keys from a BIP-39 mnemonic and protects stored private-key material using authenticated encryption and passphrase-based key derivation.

The default core key set includes:

| Key identifier | Algorithm | Role |
|---|---|---|
| `classic:x25519` | X25519 | Classical key agreement |
| `classic:ed25519` | Ed25519 | Classical digital signatures |
| `pq:ml-kem-768` | ML-KEM-768 — NIST FIPS 203 | Post-quantum key encapsulation |
| `pq:ml-dsa-87` | ML-DSA-87 — NIST FIPS 204 | Post-quantum digital signatures |

The Rust implementation brings this account model into native Rust applications. A user-controlled identity can support multiple applications rather than requiring an unrelated key set for every product.

- [TypeScript library](https://github.com/Majikah/majik-key)
- [Rust library](https://github.com/Majikah/majik-key-rs)
- [npm package](https://www.npmjs.com/package/@majikah/majik-key)
- [Crate documentation](https://docs.rs/majik-key)
- [Technical whitepaper](https://doi.org/10.5281/zenodo.23208491)
- [Whitepaper overview](https://majikah.solutions/articles/majik-key-whitepaper)

> **Protect your recovery phrase.** A BIP-39 mnemonic is a high-value secret. Anyone who obtains it may be able to recreate the associated keys. Keep it offline, never share it, and never paste it into a website or commit it to source control.

---

## Open-source projects and developer foundations

Majikah publishes selected libraries, SDKs, specifications, and implementation resources. The organization also maintains application clients, language-specific implementations, and service integrations.

### Cryptographic, data, and product libraries

| Repository | Purpose |
|---|---|
| [`majik-key`](https://github.com/Majikah/majik-key) | TypeScript cryptographic identity, key derivation, and encrypted key storage. |
| [`majik-signature`](https://github.com/Majikah/majik-signature) | TypeScript hybrid signing, file verification, signature envelopes, multi-party signing, and sealing. |
| [`majik-envelope`](https://github.com/Majikah/majik-envelope) | Multi-recipient encrypted envelope primitives built around post-quantum key encapsulation. |
| [`majik-file`](https://github.com/Majikah/majik-file) | Encrypted file container and related file workflows. |
| [`majik-message`](https://github.com/Majikah/majik-message) | Messaging domain and protocol implementation. |
| [`majik-universal-id`](https://github.com/Majikah/majik-universal-id) | Cryptographic identity data model and verification workflows. |
| [`majik-slink`](https://github.com/Majikah/majik-slink) | Signed URL claims and identity-to-resource association. |
| [`majik-invoice`](https://github.com/Majikah/majik-invoice) | TypeScript invoice domain model and optional cryptographic envelope. |

### Rust and native application stack

| Repository | Purpose |
|---|---|
| [`majik-key-rs`](https://github.com/Majikah/majik-key-rs) | Native Rust implementation of the Majik Key account and cryptographic identity model. |
| [`majik-signature-rs`](https://github.com/Majikah/majik-signature-rs) | Rust implementation of hybrid signing and verification, designed for interoperability with the TypeScript implementation. |
| [`majik-signature-client-rs`](https://github.com/Majikah/majik-signature-client-rs) | Higher-level Rust client for key/account workflows, signing, contacts, stamps, logs, and backup/restore. |
| [`tauri-plugin-majik-signature-client`](https://github.com/Majikah/tauri-plugin-majik-signature-client) | Tauri v2 plugin exposing the Rust signature client through typed commands and events. |
| [`majik-signature-client-tauri`](https://github.com/Majikah/majik-signature-client-tauri) | TypeScript facade over the Tauri plugin for desktop application integration. |
| [`majik-file-rust`](https://github.com/Majikah/majik-file-rust) | Rust implementation of the encrypted `.mjkb` file container using ML-KEM-768 and AES-256-GCM. |

### Service integrations

| Repository | Purpose |
|---|---|
| [`majikah-sdk`](https://github.com/Majikah/majikah-sdk) | Official TypeScript SDK for Majikah public services, including MUID, Trusted Timestamping, SLink, and file notarization. |
| [`majik-notary`](https://github.com/Majikah/majik-notary) | Blockchain anchoring and on-chain verification for sealed-file hashes. |

These projects have different release cycles, dependencies, and maturity levels. Each repository is the source of truth for installation instructions, licensing, API stability, changelogs, and security guidance. Public source code supports inspection; it is not, by itself, an independent security audit.

### Start building

For local TypeScript cryptographic workflows:

```bash
npm install @majikah/majik-key @majikah/majik-signature
```

For API-backed integrations:

```bash
npm install @majikah/sdk
```

Browse [all public repositories](https://github.com/orgs/Majikah/repositories) or [published npm packages](https://www.npmjs.com/~majikah).

---

## Developer platform and public API

The [Majikah Developer Portal](https://developers.majikah.solutions) provides API documentation, an OpenAPI reference, SDK resources, and an application path for production access.

The TypeScript SDK connects applications to four public service areas:

| Service | What developers can integrate |
|---|---|
| **Majik Universal ID** | Resolve public identity profiles and verify signatures against associated public keys. |
| **Trusted Timestamping** | Request verifiable timestamps for content digests and signed file states. |
| **Majik SLink** | Create, retrieve, and verify signed claims associated with URLs and content. |
| **Majik Notary** | Anchor a sealed content hash on-chain without sending the original file. |

**Developer resources:**

- [Apply for API Early Access](https://developers.majikah.solutions/early-access)
- [OpenAPI reference](https://developers.majikah.solutions/openapi/docs)
- [TypeScript SDK documentation](https://developers.majikah.solutions/sdk/majikah-sdk/docs)
- [Public API and SDK guide](https://majikah.solutions/articles/majikah-sdk-launch)

Install the SDK with `npm install @majikah/sdk`. **Production API keys are issued to approved applicants.** Submitting an application does not guarantee approval or immediate access. Cryptographic operations that require private keys are performed locally; the SDK does not upload private signing keys to the Majikah API.

---

## Documentation, articles, and technical publications

The official website maintains product guides, technical references, implementation articles, and company announcements.

### Product documentation

Start at the [documentation hub](https://majikah.solutions/docs) or go directly to [Majik Signature documentation](https://majikah.solutions/products/majik-signature/docs).

The documentation currently covers:

- **Majik Signature:** getting started, signing and verification, supported files, PDF signing, contacts and accounts, CLI/MCP, hot folders, notarization, and SignRoom workflows—including participant signing, collaboration, visual stamps and revisions, audit evidence, and retention/archives.
- **Majik Message:** account management, contacts and invitations, messages, chats, threads, File Vault, cloud storage, and installation.
- **Majik Universal ID:** identity creation, optional identity verification, public profiles, sharing, embedding, use cases, and file verification.
- **Majik SLink:** getting started, publishing, managing, and verifying signed claims.
- **Majik Buwiz:** invoicing, contacts, tax profiles, signing and encryption, exports, exchange workflows, dashboards, and troubleshooting.
- **Cryptographic primers:** ML-KEM-768, AES-256-GCM, Argon2id, hybrid encryption, fingerprints, and invite keys.

### Recent and useful articles

| Article | Why it matters |
|---|---|
| [Majikah Solutions Recognized as a Qualified Startup Business](https://majikah.solutions/articles/majikah-startup-registration-philippines) | Details the company's November 22, 2026 Qualified Startup Business recognition and links to the official Startup Philippines profile and certificate verification. |
| [Majik Signature 1.0.0: A New Foundation for Digital Trust](https://majikah.solutions/articles/majik-signature-1-0-0-release) | Covers the native Rust foundation, private-key handling, file workflows, and release changes. |
| [Majik Signature CLI & MCP](https://majikah.solutions/articles/majik-signature-cli-mcp-automation) | Explains desktop-mediated signing automation, explicit approval, and the boundaries around private-key access. |
| [Majikah Public API & TypeScript SDK](https://majikah.solutions/articles/majikah-sdk-launch) | Introduces the MUID, TSA, SLink, and Majik Notary service APIs and Early Access requirements. |
| [Majikah Partner Program](https://majikah.solutions/articles/majikah-partner-program) | Explains partner tiers, Trusted Timestamp grants, the application process, and optional benefits. |
| [Majik Key technical whitepaper](https://majikah.solutions/articles/majik-key-whitepaper) | Describes the shared cryptographic identity foundation and its key architecture. |

---

## The Majikah Partner Program

The [Majikah Partner Program](https://partners.majikah.solutions) invites freelancers, independent professionals, creators, consultants, businesses, and communities to explore Majik Signature in real workflows, share feedback, and help make verifiable digital work more accessible.

Standard partner tiers include promotional Trusted Timestamp grants:

| Tier | Standard TSA stamp grant |
|---|---:|
| Seed | 1,500 |
| Partner | 5,000 |
| Flagship | 20,000 |

These are standard tier amounts, **not guaranteed application rewards**. Applications are reviewed individually; Majikah assigns the final tier and confirms credit issuance separately. Approved partners may also receive promotional codes, eligible TSA top-up discounts, partner resources, or other collaboration opportunities when offered and activated.

[**Apply to become a partner**](https://partners.majikah.solutions) · [**Read the partner program guide**](https://majikah.solutions/articles/majikah-partner-program)

---

## How we approach security

We aim to make security understandable without hiding implementation details or overstating what technology can guarantee.

- **Standards-led engineering.** Where post-quantum cryptography is used, relevant components build on published standards such as ML-KEM (FIPS 203) and ML-DSA (FIPS 204).
- **Privacy and user control.** We design for local-first operation, data minimization, and user-controlled cryptographic identity where the product and use case allow it.
- **Verifiable outcomes.** Signatures, file formats, and public proofs are designed so results can be checked independently using the appropriate public keys, specifications, and verification tools.
- **Clear limitations.** We distinguish algorithm standards from product certification, and cryptographic verification from real-world identity or legal authority.

### Security context and limitations

Using a NIST-standardized algorithm does **not** mean a Majikah product is NIST-certified or independently audited. Public source code, a technical whitepaper, test coverage, or third-party website ratings are not substitutes for a full independent security audit of the complete product.

A valid digital signature shows that specific content verifies against a particular public key. It does not, by itself, prove the real-world identity of the key holder, establish that the signer had legal authority, or guarantee that a document is legally valid in every jurisdiction. Verify identity and authority through a trusted process appropriate to your use case.

Post-quantum cryptography addresses specific classes of cryptographic risk; it does not protect against compromised devices, malware, exposed recovery phrases, weak passphrases, social engineering, or implementation defects. Review product-specific threat models and operational guidance before deployment.

---

## The company

**Majikah Solutions OPC** is a founder-led Philippine software company based in Mandaluyong City. We develop our own products and cryptographic technology while providing bespoke software engineering for organizations that need practical, security-conscious digital solutions.

The company was founded by **Josef Elijah Fabian (Zelijah), Founder & Lead Developer**. A self-taught software engineer and multidisciplinary creator, he worked professionally in music and creative production before shifting his focus to technology in late 2023. That background informs Majikah's focus on authorship, agreements, approvals, digital identity, and the integrity of creative work.

The [About page](https://majikah.solutions/about) covers the company's purpose, products, founder, business model, partners, and credibility foundations. The [Developer page](https://majikah.solutions/developer) provides more detail about the person designing and building the products.

Our goals are to:

1. Make practical, standards-based security more accessible to individuals, creators, teams, and businesses.
2. Build reusable cryptographic foundations and developer tools that other products and teams can integrate.
3. Grow through responsible product adoption and long-term relationships with technology, distribution, research, and institutional partners.

---

## Work with us

We welcome conversations with people and organizations interested in practical security and trustworthy digital systems.

- **Developers:** explore source repositories, SDKs, technical publications, API documentation, and the developer portal.
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
| **Founder and developer profile** | [The developer behind Majikah](https://majikah.solutions/developer) |
| **Developer portal** | [developers.majikah.solutions](https://developers.majikah.solutions) |
| **Product documentation** | [Documentation hub](https://majikah.solutions/docs) |
| **Partner program** | [partners.majikah.solutions](https://partners.majikah.solutions) |
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
