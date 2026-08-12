# learnings

explainers on various topics

Rendered pages: **https://dougcooper.github.io/learnings/**

> GitHub shows the raw source when you click an `.html` file in this repo.
> Use the **Read** links below for the rendered versions.

## Explainers

| Topic | Read | Source |
|---|---|---|
| **TLS 1.3** — RFC 8446: the 1-RTT handshake, key schedule, record layer, 0-RTT resumption, removed TLS 1.2 features, downgrade protection | [open](https://dougcooper.github.io/learnings/rfc8446-tls13-explainer.html) | [`rfc8446-tls13-explainer.html`](rfc8446-tls13-explainer.html) |
| **Hybrid key exchange** — RFC 9954: running a traditional and a post-quantum algorithm together in TLS 1.3, KEM abstraction, concatenated key shares and secrets, the fixed-length requirement | [open](https://dougcooper.github.io/learnings/rfc9954-hybrid-kex-explainer.html) | [`rfc9954-hybrid-kex-explainer.html`](rfc9954-hybrid-kex-explainer.html) |
| **Raw public keys** — RFC 7250: sending a bare `SubjectPublicKeyInfo` instead of a certificate, the two certificate-type extensions, per-direction negotiation, out-of-band trust (DANE, provisioning) | [open](https://dougcooper.github.io/learnings/rfc7250-raw-public-keys-explainer.html) | [`rfc7250-raw-public-keys-explainer.html`](rfc7250-raw-public-keys-explainer.html) |

## Adding one

Drop a self-contained `.html` file in the repo root and add a row above.
GitHub Pages serves `main` at root, so the file is live at
`https://dougcooper.github.io/learnings/<filename>` as soon as it's pushed.
