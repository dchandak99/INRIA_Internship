# INRIA_Internship

### Formal Verification of Security Protocols | Cryptography
I was a Research Intern at [INRIA](https://www.inria.fr/en) Nancy during April and May 2020, under Professors [Steve Kremer](https://members.loria.fr/SKremer/) and [Jannik Dreier](https://members.loria.fr/JDreier/).

**Highlights:**
- Studied operational semantics and equivalence properties (in *applied pi calculus* and **Tamarin** prover), the current translation of **SAPIC** (tool translating high level protocols to multiset rewrite rules, analyzable by Tamarin)
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

We generally distinguish two families of security properties:
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
  
  
**Links:**

[1] http://tamarin-prover.github.io/  
[2] https://prosecco.gforge.inria.fr/personal/bblanche/proverif/  
[3] http://sapic.gforge.inria.fr/  
[4] https://hal.inria.fr/hal-01090874/document  
[5] https://hal.inria.fr/hal-01351388/document  
[6] https://hal.archives-ouvertes.fr/hal-01337409v2/document  
  
     
### Repository Explanation:
- [Sap_Tam](Sap_Tam) contains protocols in SAPIC(.sapic) and Tamarin(.spthy). You can visualise them via the Tamarin tool. [Eq_Att](Sap_Tam/Eq_Att) contains the sapic and tamarin files to test the diff operator in sapic, and try out various corner and edge cases
- [code](code) contains various directories with directory names corresponding to the property/protocol which is explored in the code in the directory. The [ProVerif](code/ProVerif) directory contains .pv files and has the code using *diff* operator in [ProVerif](https://prosecco.gforge.inria.fr/personal/bblanche/publications/BlanchetFnTPS16.pdf)
- [Internship_Report.tex](Internship_Report.tex) contains the *definitions* and *proofs* which I have introduced:

  * Biprocesses in SAPIC  
  * Translation of Biprocesses  
  * Tamarin Equivalent Biprocess  
  * Diff Equivalence in SAPIC:
    - Static Equivalence
    - Recipes
    - Bi-Operational Semantics

- *Dummy* Events in SAPIC to unhide silent actions for the translation
- **Proof** that Tamarin Equivalence implies SAPIC equivalence i.e. ensured the soundness of the translation from SAPIC to Tamarin

