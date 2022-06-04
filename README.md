# A journey to ZKP

## Plan

- [Learn the Maths by Khan Academy](#learn-the-maths-by-khan-academy)
- [zk-SNARKs](#zk-snarks)
  - [Why and How zk-SNARK Works by Maksym Petkus](#why-and-how-zk-snark-works-by-maksym-petkus)
  - [Explaining SNARKs by Ariel Gabizon](#explaining-snarks-by-ariel-gabizon)
  - [Vitalik Buterin](#vitalik-buterin-on-zk-snarks)
  - [How does PLONK work by David Wong](#how-does-plonk-work-by-david-wong)
- [zk-STARKs](#zk-starks)
  - [A journey to zk-STARKs by StarkWare](#a-journey-to-zk-starks-by-starkware)

## zk-SNARKs

### Learn the Maths by Khan Academy

Khan Academy provides two great courses dedicated to learning polynomials and modular arithmetic.

1. [Polynomials](https://www.khanacademy.org/math/algebra-home/alg-polynomials)
2. [Modular Arithmetic](https://www.khanacademy.org/computing/computer-science/cryptography#modarithmetic)

### Why and How zk-SNARK Works by Maksym Petkus

[Maksym Petkus](https://twitter.com/maksympetkus) has written 8 excellents posts explaining zk-SNARKs in detail.
Every piece of maths involved is described in detailed, computing the formulas yourselves is a must to properly understand the posts imo.

Based on [his paper](https://arxiv.org/abs/1906.07221).

1. [Why and How zk-SNARK Works 1: Introduction & the Medium of a Proof](https://medium.com/@imolfar/why-and-how-zk-snark-works-8-zero-knowledge-computation-f120339c2c55)
2. [Why and How zk-SNARK Works 2: Proving Knowledge of a Polynomial](https://medium.com/@imolfar/why-and-how-zk-snark-works-2-proving-knowledge-of-a-polynomial-f817760e2805)
3. [Why and How zk-SNARK Works 3: Non-interactivity & Distributed Setup](https://medium.com/@imolfar/why-and-how-zk-snark-works-3-non-interactivity-distributed-setup-c0310c0e5d1c)
4. [Why and How zk-SNARK Works 4: General-Purpose Computation](https://medium.com/@imolfar/why-and-how-zk-snark-works-4-general-purpose-computation-dcdc8081ee42)
5. [Why and How zk-SNARK Works 5: Variable Polynomials](https://medium.com/@imolfar/why-and-how-zk-snark-works-5-variable-polynomials-3b4e06859e30)
6. [Why and How zk-SNARK Works 6: Verifiable Computation Protocol](https://medium.com/@imolfar/why-and-how-zk-snark-works-6-verifiable-computation-protocol-1aa19f95a5cc)
7. [Why and How zk-SNARK Works 7: Constraints and Public Inputs](https://medium.com/@imolfar/why-and-how-zk-snark-works-7-constraints-and-public-inputs-e95f6596dd1c)
8. [Why and How zk-SNARK Works 8: Zero-Knowledge Computation](https://medium.com/@imolfar/why-and-how-zk-snark-works-8-zero-knowledge-computation-f120339c2c55)

### Explaining SNARKs by Ariel Gabizon

Ariel Gabizon has written 7 posts explaining zk-SNARKs. Takes a different approach compared to Maksym's posts and definitely useful !

1. [Explaining SNARKs Part I: Homomorphic Hidings](https://electriccoin.co/blog/snark-explain/)
2. [Explaining SNARKs Part II: Blind Evaluation of Polynomials](https://electriccoin.co/blog/snark-explain2/)
3. [Explaining SNARKs Part III: The Knowledge of Coefficient Test and Assumption](https://electriccoin.co/blog/snark-explain3/)
4. [Explaining SNARKs Part IV: How to make Blind Evaluation of Polynomials Verifiable](https://electriccoin.co/blog/snark-explain4/)
5. [Explaining SNARKs Part V: From Computations to Polynomials](https://electriccoin.co/blog/snark-explain5/)
6. [Explaining SNARKs Part VI: The Pinocchio Protocol](https://electriccoin.co/blog/snark-explain6/)
7. [Explaining SNARKs Part VII: Pairings of Elliptic Curves](https://electriccoin.co/blog/snark-explain7/)

### Vitalik Buterin on zk-SNARKs

The unknown founder of Ethereum has written a few posts related to zk-SNARKs and the math behind.

1. [Quadratic Arithmetic Programs: from Zero to Hero](https://medium.com/@VitalikButerin/quadratic-arithmetic-programs-from-zero-to-hero-f6d558cea649)
2. [Exploring Elliptic Curve Pairings](https://medium.com/@VitalikButerin/exploring-elliptic-curve-pairings-c73c1864e627)
3. [Zk-SNARKs: Under the Hood](https://medium.com/@VitalikButerin/zk-snarks-under-the-hood-b33151a013f6)

### How does PLONK work by David Wong

David Wong, the author of the Real-World Cryptography book and host of [cryptologie.net](https://www.cryptologie.net/) has made a serie of 11 videos explaining both the concept and math behind the PLONK protocol.

1. [How does PLONK work? Part 1: What's PLONK ?](https://www.youtube.com/watch?v=RUZcam_jrz0&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=1)
2. [How does PLONK work? Part 2: An overview](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=2)
3. [How does PLONK work? Part 3: Starting with the end: polynomials](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=3)
4. [How does PLONK work? Part 4: From programs to arithmetic circuits](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=4)
5. [How does PLONK work? Part 5: From arithmetic circuits to constraint systems](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=5)
6. [How does PLONK work? Part 6: From constraint systems to polynomials](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=6)
7. [How does PLONK work? Part 7: A sketch protocol with our polynomial](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=7)
8. [How does PLONK work? Part 8: A polynomial dance](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=8)
9. [How does PLONK work? Part 9: What's a polynomial commitment scheme (PCS) ?](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=9)
10. [How does PLONK work? Part 10: The Kate polynomial commitment scheme](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=10)
11. [How does PLONK work? Part 11: Our final protocol! (Without the copy constraints)](https://www.youtube.com/watch?v=P1JeN30RdwQ&list=PLBJMt6zV1c7Gh9Utg-Vng2V6EYVidTFCC&index=11)


## zk-STARKs

### A journey to zk-STARKs by StarkWare

StarkWare members, the founders of the zk-STARKs protocol, have written a serie of posts explaining the STARK protocol.

1. [The journey begins](https://medium.com/starkware/stark-math-the-journey-begins-51bd2b063c71)
2. [Arithmetization I](https://medium.com/starkware/arithmetization-i-15c046390862)
3. [Arithmetization II](https://medium.com/starkware/arithmetization-ii-403c3b3f4355)
4. [Low Degree Testing](https://medium.com/starkware/low-degree-testing-f7614f5172db)
5. [A Framework for Efficient STARKs](https://medium.com/starkware/a-framework-for-efficient-starks-19608ba06fbe)
