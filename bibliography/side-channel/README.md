# Side Channel Papers

### (side-channel-attack.pdf) A Side-Channel Assisted Attack on NTRU by Amund Askeland and Sondre Rønjom, 2021

Which NTRU version: Current implementation of NTRU submitted to
the NIST post-quantum standardization project on 2021

Summary: They found two strong sources of leakage in the unpacking of the secret key, by going through the NTRU C/C++ source code and measuring the power consumption. The target processor is handling data with very different Hamming weight depending on parts of the secret key. They show how one can do a partial recovery (on 75% of their cases) and a full key recovery and finally they propose some small modifications on the code to minimize the leakages.


### (2020-992.pdf) Single-Trace Attacks on Message Encoding in Lattice-Based KEMs by BO-YEON SIM, JIHOON KWON, JOOHEE LEE, IL-JU KIM, TAE-HO LEE, JAESEUNG HAN, HYOJIN YOON, JIHOON CHO AND DONG-GUK HAN, 2020

Which NTRU version: NTRU and NTRU Prime

Summary: Single-trace side-channel attacks against lattice-based KEMs the third-round candidates of NIST (CRYSTALS-KYBER, SABER, FrodoKEM, NTRU, NTRU Prime). If message μ=(μl-1,...,μ0), for each μi they find their Points of Interest (the points whose mask is already calculated,stored and loaded, where a mask value is determined based on a sensitive bit µi value) and then using some machine learning algorithms they cluster the points to two possible Hamming wieghts and therefore the coefficient of each μi is 0 or 1 and they get the message μ.

### (chosen-ciphertext-side-channel.pdf) Reveal the Invisible Secret: Chosen-Ciphertext Side-Channel Attacks on NTRU by Zhuang Xu, Owen Pemberton, David Oswald and Zhiming Zheng, 2023

Which NTRU version: all NTRU instances in Round 3 of NIST 

Summary: They utilize the leakage from the polynomial modular reduction to recover the long-term secret key. There are two attacks: a) (for all NTRU instances) they recover the differences between adjacent coefficients using appropriately chosen ciphertexts and finally reconstruct f through linear algebra and b) (for NTRU-HPS instances), they first reveal the “invisible” secret polynomial g with chosen ciphertexts and then use g and the public polynomial h to compute f. The leaky function is the Rq to S3 polynomial modular reduction in decryption in the decapsulation phase, which leaks the Hamming Weight of a secret-dependent intermediate value and then they mount chosen-ciphertext Electro-Magnetic (EM) SCA on the reference implementations of all instances.

### (generic-side-channel.pdf, generic-side-channel-long-ver.pdf) Generic Side-Channel Assisted Chosen-Ciphertext Attacks on NTRU-based KEMs by Prasanna Ravi, Martianus Frederic Ezerman, Shivam Bhasin,
Anupam Chattopadhyay and Sujoy Sinha Roy, 2022

Which NTRU version: NTRU, NTRU Prime

Summary: Side-channel assisted chosenciphertext attacks on NTRU-based KEMs. They construct malformed ciphertexts, decapsulate them and gain the full secret key. They propose many CCA's which have 3 diff types of oracles: a plaintext-checking oracle, a decryptionfailure oracle, and a full-decryption oracle.

### (scan-based-side-channel.pdf) A Scan-Based Side Channel Attack on the NTRUEncrypt Cryptosystem by Abdel Alim Kamal and Amr M. Youssef, 2012

Which NTRU version: NTRUEncrypt family of the IEEE P1363 standards

Summary: A scan-based side channel attack on NTRUEncrypt hardware implementations that employ scan based Design-for-Test (DFT) techniques. Our attack determines the scan chain structure of the polynomial multiplication circuits used in the decryption algorithm which allows the cryptanalyst to efficiently retrieve the secret key. Scan-based side channel attacks exploit the information obtained by analyzing the scanned data in order to retrieve secret information from cryptographic hardware devices that are designed with this testability feature. 


### (single-trace-side-channel.pdf) Single Trace Side Channel Analysis on NTRU Implementation by Soojung An, Suhri Kim, Sunghyun Jin, HanBit Kim and HeeSeok Kim, 2018

Which NTRU version:  NTRU Open Source and NTRUEncrypt

Summary: The first single trace attack on NTRU. Previous side-channel attacks on NTRU used numerous power traces, which increase the attack complexity and limit the target algorithm. In this paper they use a single power consumption trace obtained in the decryption phase and recover the secret key.


### (omega-small-side-channel.pdf) Single-Trace Side-Channel Attacks on ω-Small Polynomial Sampling with Applications to NTRU, NTRU Prime, and CRYSTALS-DILITHIUM by Emre Karabulut, Erdem Alkim, Aydin Aysu, 2021

Which NTRU version: NTRU, NTRU Prime, and CRYSTALS-DILITHIUM

Summary: A new single-trace side-channel targeting the ω-small polynomial sampling and we demonstrate the vulnerabilities of their sub-routines to a powerbased side-channel attack. They reveal that the sorting implementation in NTRU/NTRU Prime ω-small polynomial sampling process leaks information about the ‘-1’, ‘0’, or ‘+1’ assignments made to the coefficients and that revealing them allows secret and session key recovery for NTRU/NTRU Prime. They run the reference software submissions from NIST Round-3 software packages.The results show that our attacks can extract coefficients with a success rate of 99.78% for NTRU and NTRU Prime, reducing the
search space to 2^41 or below.

### (power-analysis-ntru-prime.pdf) Power Analysis on NTRU Prime by Wei-Lun Huang, Jiun-Peng Chen and Bo-Yin Yang, 2019

Which NTRU version: multiple NTRU Prime implementations (eg. the reference one, the one optimized using smladx, and three protected ones)

Summary: They apply a variety of power analysis techniques: vertical correlation power analysis, horizontal in-depth correlation power analysis, online template attacks, and chosen-input simple power analysis. Fully recover private keys with one single trace of short observation span, with few template traces from a fully controlled device similar to the target and no a priori power model, or sometimes even with the naked eye. The techniques target the constant-time generic polynomial multiplications in the product scanning method. Though in this work the techniques focus on the decapsulation, they also work on the key generation and encapsulation of NTRU Prime.

### (magnifying-side-channel-kyber.pdf) Magnifying Side-Channel Leakage of Lattice-Based Cryptosystems With Chosen Ciphertexts: The Case Study of Kyber by Zhuang Xu, Owen Pemberton, Sujoy Sinha Roy, David Oswald, Wang Yao and Zhiming Zheng, 2022

Which NTRU version: Mainly Kyber but they discuss the relevance of their findings to other lattice-based schemes.

Summary: Despite the various side-channel targets examined in previous studies, detail on revealing the secret-dependent information efficiently is less studied. In this paper, we propose adaptive EM side-channel attacks with carefully constructed ciphertexts on Kyber. They demonstrate that specially chosen ciphertexts allow an adversary to modulate the leakage of a target device and enable full key extraction with a small number of traces through simple power analysis. For the pqm4 implementation, we develop a message-recovery attack that leads to extraction of the full secret key.



### (sca-masked-kyber.pdf) A Side-Channel Attack on a Masked IND-CCA Secure Saber KEM by Kalle Ngo, Elena Dubrova, Qian Guo and Thomas Johansson, 2021

Which NTRU version: Only Kyber

Abstract:  The first side-channel attack on a first-order masked
implementation of IND-CCA secure Saber KEM. We show how to recover both the
session key and the long-term secret key from 16 traces by deep learning-based power
analysis without explicitly extracting the random mask at each execution. Since the
presented method is not dependent on the mask, we can improve success probability
by combining score vectors of multiple traces captured for the same ciphertext. This
is an important advantage over previous attacks on LWE/LWR-based KEMs, which
must rely on a single trace. Another advantage is that the presented method does
not require a profiling device with deactivated countermeasure, or known secret
key. Thus, if a device under attack is accessible, it can be used for profiling. This
typically maximizes the classification accuracy of deep learning models. In addition,
we discovered a leakage point in the primitive for masked logical shifting on arithmetic
shares which has not been known before. We also present a new approach for secret
key recovery, using maps from error-correcting codes. This approach can compensate
for some errors in the recovered message.



