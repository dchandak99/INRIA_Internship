# INRIA_Internship

### Formal Verification of Security Protocols | Cryptography
I was a Research Intern at INRIA Nancy during April and May 2020, under Professors Steve Kremer and Jannik Dreier.

**Highlights:**
- Studied operational semantics and equivalence properties (in *applied pi calculus* and **Tamarin** prover), the current translation of **SAPIC**(tool translating high level protocols to multiset rewrite rules, analyzable by Tamarin)
- Introduced biprocesses (*with bisemantics and their translation*), static equivalence and diff equivalence (*& diff operator*) in SAPIC, ensuring the soundness of the translation after the addition

### Problem Statement:
Security protocols are distributed programs that aim at ensuring
security properties, such as confidentiality, authentication or
anonymity, by the means of cryptography. Such protocols are
widely deployed, e.g., for electronic commerce on the Internet,
in banking networks, mobile phones and more recently
electronic elections. As properties need to be ensured, even if
the protocol is executed over untrusted networks (such as the
Internet), these protocols have shown extremely difficult to get
right. Formal methods have shown very useful to detect errors
and ensure their correctness.
We generally distinguish two families of security properties :
trace properties and observational equivalence properties. Trace
properties verify a predicate on a given trace and are typically
used to express authentication properties. Observational
equivalence expresses that an adversary cannot distinguish two
situations and is used to model anonymity and strong
confidentiality properties.
The Tamarin prover is a state-of-the art protocol verification tool
which has been successfully used to verify standards such as
TLS 1.3 and 5G AKA, as well as industrial protocols such as OPC
UA. SAPIC allows protocols to be specified in a high-level
protocol specification language, an extension of the applied pi-
calculus, and uses the Tamarin prover as a backend by
compiling the language into multi-set rewrite rules, the inputformat of Tamarin.
This compilation has been proven correct for any property
written in a first-order logic, allowing to express trace properties.
The goal of the internship is to extend SAPIC to observational
equivalences in order to take advantage of the recent
extensions of Tamarin.

To be updated using CV, int_details.pdf and https://help.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax
