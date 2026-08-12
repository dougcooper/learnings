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

## Adding one

Drop a self-contained `.html` file in a topic directory (`tls/`, or a new one)
and add a row above. GitHub Pages serves `main` at root, so the file is live at
`https://dougcooper.github.io/learnings/<dir>/<filename>` as soon as it's pushed.

Two things Jekyll cares about: don't start an `.html` file with `---` (it gets
read as front matter), and don't name a directory `_something` (it gets ignored).
