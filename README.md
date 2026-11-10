# veribridge

VeriBridge is a bidirectional bridge between JSON-LD-Ex and CBOR-LD-Ex that preserves veracity annotations exactly across textual and binary encodings of the same semantic graph.

Semantic data on the Web moves between verbose textual representations and compact binary encodings as it crosses from cloud services to constrained edge and IoT devices. That translation is usually lossy for exactly the metadata that matters most downstream: provenance and veracity annotations attached to individual statements. VeriBridge treats annotations as first-class graph content rather than encoding-specific side data, so a statement annotated in JSON-LD-Ex arrives in CBOR-LD-Ex with its veracity record unchanged and can return without loss: annotation identity, scope, and values are preserved exactly, not approximated or dropped.

## Packages

This monorepo holds the VeriBridge implementation in three languages, one package per ecosystem, all named `veribridge`:

| Package | Ecosystem | Path |
| --- | --- | --- |
| Python | PyPI | `packages/python` |
| Rust | crates.io | `packages/rust` |
| TypeScript | npm | `packages/typescript` |

Status: in development. The three packages implement the same bridge specification and are tested against shared round-trip fixtures.

## Paper

"VeriBridge: Preserving Veracity Annotations Between JSON-LD-Ex and CBOR-LD-Ex"
Muntaser Syed, Sheikh Abujar, Marius Silaghi, Vincent Occhiogrosso, Katherine Burge, Michael Friedberg.
Submitted to The Web Conference 2027 (WWW '27), Short Papers track (OpenReview Submission 930).

Paper repository: [github.com/jemsbhai/veribridge-paper](https://github.com/jemsbhai/veribridge-paper)

## License

MIT
