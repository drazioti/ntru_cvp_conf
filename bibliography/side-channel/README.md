# Side Channel Papers

### (side-channel-attack.pdf) A Side-Channel Assisted Attack on NTRU by Amund Askeland and Sondre Rønjom, 2021

Which NTRU version: Current implementation of NTRU submitted to
the NIST post-quantum standardization project on 2021

Summary: They found two strong sources of leakage in the unpacking of the secret key, by going through the NTRU C/C++ source code and measuring the power consumption. The target processor is handling data with very different Hamming weight depending on parts of the secret key. They show how one can do a partial recovery (on 75% of their cases) and a full key recovery and finally they propose some small modifications on the code to minimize the leakages.


### (2020-992.pdf) Single-Trace Attacks on Message Encoding in Lattice-Based KEMs by BO-YEON SIM, JIHOON KWON, JOOHEE LEE, IL-JU KIM, TAE-HO LEE, JAESEUNG HAN, HYOJIN YOON, JIHOON CHO AND DONG-GUK HAN, 2020

Which NTRU version: NTRU and NTRU Prime

Summary: Single-trace side-channel attacks against lattice-based KEMs the third-round candidates of NIST (CRYSTALS-KYBER, SABER, FrodoKEM, NTRU, NTRU Prime). If message μ=(μl-1,...,μ0), for each μi they find their Points of Interest (the points whose mask is already calculated,stored and loaded, where a mask value is determined based on a sensitive bit µi value) and then using some machine learning algorithms they cluster the points to two possible Hamming wieghts and therefore the coefficient of each μi is 0 or 1 and they get the message μ.

### (chosen-ciphertext-side-channel.pdf) Reveal the Invisible Secret: Chosen-Ciphertext Side-Channel Attacks on NTRU Zhuang Xu, Owen Pemberton, David Oswald and Zhiming Zheng, 2023

Which NTRU version: all NTRU instances in Round 3 of NIST 

Summary: They utilize the leakage from the polynomial modular reduction to recover the long-term secret key. There are two attacks: a) (for all NTRU instances) they recover the differences between adjacent coefficients using appropriately chosen ciphertexts and finally reconstruct f through linear algebra and b) (for NTRU-HPS instances), they first reveal the “invisible” secret polynomial g with chosen ciphertexts and then use g and the public polynomial h to compute f. The leaky function is the Rq to S3 polynomial modular reduction in decryption in the decapsulation phase, which leaks the Hamming Weight of a secret-dependent intermediate value and then they mount chosen-ciphertext Electro-Magnetic (EM) SCA on the reference implementations of all instances.
