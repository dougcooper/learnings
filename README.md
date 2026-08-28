# learnings

explainers on various topics

Rendered pages: **https://dougcooper.github.io/learnings/**

> GitHub shows the raw source when you click an `.html` file in this repo.
> Use the **Read** links below for the rendered versions.

## TLS

| Topic | Read | Source |
|---|---|---|
| **TLS 1.3** — RFC 8446: the 1-RTT handshake, key schedule, record layer, 0-RTT resumption, removed TLS 1.2 features, downgrade protection | [open](https://dougcooper.github.io/learnings/tls/rfc8446-tls13.html) | [`tls/rfc8446-tls13.html`](tls/rfc8446-tls13.html) |
| **Hybrid key exchange** — RFC 9954: running a traditional and a post-quantum algorithm together in TLS 1.3, KEM abstraction, concatenated key shares and secrets, the fixed-length requirement | [open](https://dougcooper.github.io/learnings/tls/rfc9954-hybrid-kex.html) | [`tls/rfc9954-hybrid-kex.html`](tls/rfc9954-hybrid-kex.html) |
| **Raw public keys** — RFC 7250: sending a bare `SubjectPublicKeyInfo` instead of a certificate, the two certificate-type extensions, per-direction negotiation, out-of-band trust (DANE, provisioning) | [open](https://dougcooper.github.io/learnings/tls/rfc7250-raw-public-keys.html) | [`tls/rfc7250-raw-public-keys.html`](tls/rfc7250-raw-public-keys.html) |

## QUIC

| Topic | Read | Source |
|---|---|---|
| **QUIC** — RFC 9000: streams and flow control, the combined crypto/transport handshake, packets vs frames, connection IDs and migration, anti-amplification, stateless reset, wire encoding | [open](https://dougcooper.github.io/learnings/quic/rfc9000-quic.html) | [`quic/rfc9000-quic.html`](quic/rfc9000-quic.html) |

## SSH

| Topic | Read | Source |
|---|---|---|
| **SSH Transport** — RFC 4253: the three-layer SSH model, the plaintext version exchange, KEXINIT algorithm negotiation, Diffie-Hellman with host-key signing and TOFU, key derivation, the binary packet protocol and its never-reset sequence number, encryption/MAC/compression floors, re-keying, the service handoff to userauth | [open](https://dougcooper.github.io/learnings/ssh/rfc4253-ssh-transport.html) | [`ssh/rfc4253-ssh-transport.html`](ssh/rfc4253-ssh-transport.html) |

## Messaging

| Topic | Read | Source |
|---|---|---|
| **MLS** — RFC 9420: the ratchet tree and tree invariant, O(log n) UpdatePath key encapsulation, the epoch key schedule, the per-sender secret tree with handshake/application ratchets, Commit mechanics, message framing, external join / ReInit / branching, FS + PCS against an untrusted Delivery Service | [open](https://dougcooper.github.io/learnings/messaging/rfc9420-mls.html) | [`messaging/rfc9420-mls.html`](messaging/rfc9420-mls.html) |
| **Double Ratchet** — Signal's per-session algorithm: the symmetric-key ratchet (one-way chain key → message key per message), the Diffie-Hellman ratchet (fresh key agreement on every direction change → forward secrecy + post-compromise security), header encryption, SPQR post-quantum ratchet, the Triple Ratchet hybrid, and PQXDH for the initial shared secret | [open](https://dougcooper.github.io/learnings/messaging/double-ratchet.html) | [`messaging/double-ratchet.html`](messaging/double-ratchet.html) |
| **Triple Ratchet** — Dodis, Jost, Katsumata, Prest, Schmidt (IACR 2025/078): Signal's Double Ratchet plus a post-quantum ratchet with erasure-coded chunks, the lattice RKEM Katana (hint-MLWE), the critical security flaw in prior lattice RKEM proofs, per-epoch bandwidth 1,416 B vs Kyber's 2,272 B | [open](https://dougcooper.github.io/learnings/messaging/triple-ratchet.html) | [`messaging/triple-ratchet.html`](messaging/triple-ratchet.html) |
| **Sparse CKA** — Auerbach, Dodis, Jost, Katsumata, Schmidt (IACR 2025/2267): the epoch-vs-message mismatch under chunking, the Sparse CKA abstraction, three new protocols (Opp-UniKEM-CKA, Opp-BiKEM-CKA, Opp-RKEM-CKA) with opportunistic sending, the comparison framework on vulnerable *epoch* sets, the headline result — no protocol dominates across balanced / send-heavy / receive-heavy patterns | [open](https://dougcooper.github.io/learnings/messaging/iacr-2025-2267-explainer.html) | [`messaging/iacr-2025-2267-explainer.html`](messaging/iacr-2025-2267-explainer.html) |

## DTN

| Topic | Read | Source |
|---|---|---|
| **BPSec** — RFC 9172: the Bundle Protocol security layer for Delay-Tolerant Networking, the two services (BIB integrity, BCB confidentiality) as BP extension blocks, the Abstract Security Block CBOR structure, canonical forms and AAD, BCB-before-BIB processing with verifier/acceptor roles, block-interaction constraints, multi-source waypoint transformation, the "Olive" on-path-attacker threat model, and pluggable security contexts | [open](https://dougcooper.github.io/learnings/dtn/rfc9172-bpsec.html) | [`dtn/rfc9172-bpsec.html`](dtn/rfc9172-bpsec.html) |

## Adding one

Drop a self-contained `.html` file in a topic directory (`tls/`, or a new one)
and add a row above. GitHub Pages serves `main` at root, so the file is live at
`https://dougcooper.github.io/learnings/<dir>/<filename>` as soon as it's pushed.

Two things Jekyll cares about: don't start an `.html` file with `---` (it gets
read as front matter), and don't name a directory `_something` (it gets ignored).
