# crypto-lean

A small Lean 4 exploration of ElGamal encryption. Three properties are proved:

- **Correctness**: decryption inverts encryption.
- **Homomorphic property**: component-wise ciphertext multiplication corresponds to multiplying plaintexts and adding randomness.
- **Random blinding**: multiplying a uniform distribution by a fixed group element preserves uniformity (the key probabilistic lemma behind ElGamal's IND-CPA security).

See [`CryptoLean.lean`](./CryptoLean.lean) for the full definitions, proofs, and background on IND-CPA and the DDH assumption.

## Build

```
lake build
```

Uses the Lean toolchain pinned in [`lean-toolchain`](./lean-toolchain); `lake` fetches Mathlib as specified in [`lakefile.toml`](./lakefile.toml) / [`lake-manifest.json`](./lake-manifest.json).
