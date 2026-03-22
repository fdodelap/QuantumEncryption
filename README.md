# QuantumEncryption
Quantum circuit encryption using real IBM quantum hardware — BB84 protocol demo with verifiable job IDs
# Quantum Encryption Demo — Aexa Tech

Encrypt and decrypt real text using a **real IBM quantum computer**.
Not a simulation. Not classical math. Real quantum hardware.

Built by Dr. Fernando De La Peña Llaca — Founder & CEO, Aexa Aerospace LLC

---

## What this does

Takes any text, converts it to qubits, sends them to IBM's 156-qubit
quantum processor (ibm_fez), scrambles them using a secret sequence of
quantum gate operations, and returns encrypted output.

Decryption runs the same gate sequence in reverse — also on the quantum
computer. Only someone with the exact gate sequence AND access to a
quantum computer can decrypt the message.

---

## Proof — real quantum jobs

These job IDs are permanently logged on IBM's servers.
Verify at: quantum.ibm.com/jobs

| Chunk | Job ID | Machine |
|---|---|---|
| AEXA | d6vehl2f84ks73df7ue0 | ibm_fez |
| TEC  | d6vehn2tnsts73et4nog | ibm_fez |
| H 20 | d6vehp469uic73cj78p0 | ibm_fez |
| 26   | d6vehqqtnsts73et4nt0 | ibm_fez |

---

## How to run it

**Step 1** — Get a free IBM Quantum account
Go to quantum.ibm.com → Account settings → copy your API token

**Step 2** — Open the notebook in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fdodelap/quantum-encryption-demo/blob/main/quantum_encryption_aexa.ipynb)

**Step 3** — Run cells top to bottom
Paste your IBM token in Cell 2, change the message in Cell 7, run all.

**Step 4** — You get a real quantum job ID
Your message encrypted on real quantum hardware in under 2 minutes.

---

## The encryption key

The key is a secret sequence of quantum gate operations:
```
H → X → Z → H → S → H → X → H
```

| Gate | Name | What it does |
|---|---|---|
| H | Hadamard | Puts qubit in superposition |
| X | Pauli-X | Flips the qubit (0→1, 1→0) |
| Z | Pauli-Z | Flips the quantum phase |
| S | S gate | Rotates phase 90 degrees |

Share this sequence in person — never send it digitally.
That is the only key required to decrypt.

---

## Requirements
```
qiskit
qiskit-aer
qiskit-ibm-runtime
cryptography
```

Install with:
```
pip install qiskit qiskit-aer qiskit-ibm-runtime cryptography
```

---

## Honest disclaimer

The quantum gate operations used for encryption can theoretically
be replicated on a classical computer. What the quantum hardware
adds is genuine hardware-level randomness and verifiable proof
of execution via permanent job IDs.

The full vision — quantum key distribution over fiber with
physics-guaranteed security — requires physical QKD hardware
between two locations. This demo is the software pipeline
that will power that system.

---

## About Aexa Tech

Aexa Aerospace LLC builds holographic AI presence platforms
and quantum-safe communication infrastructure.

Led the world's first holoportation in space — October 2021,
ISS, in partnership with NASA and ESA.

aexa.tech | github.com/fdodelap
