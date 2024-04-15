# -Design-a-digital-circuit-that-encrypts-a-given-digital-input-using-the-DES-algorithm-on-Proteus

The problem statement describes a simplified version of the Data Encryption Standard (DES) algorithm, which is divided into two parts: combinational and sequential circuits.

Part 1:
1. The input to the circuit is an 8-bit plaintext (message to be encrypted) and an 8-bit initial key.
2. The plaintext undergoes an initial permutation using a given permutation table.
3. The permuted plaintext is then divided into two halves: the left half (L0) and the right half (R0), each 4 bits long.
4. The encryption process consists of four rounds, where in each round:
   a. A round key (RK-i) is generated from the initial key using a key generation process involving permutation, compression, and circular left shifts.
   b. The right half (Ri) is expanded and XORed with the round key (RK-i).
   c. The result of the XOR operation is split into two halves and passed through two substitution boxes (S-boxes) to produce a 4-bit output.
   d. The output of the S-boxes is permuted, and the result is XORed with the left half (Li) to produce the new right half (Ri+1) for the next round.
   e. The right half (Ri) becomes the new left half (Li+1) for the next round.
5. After the fourth round, the final left half (L4) and right half (R4) are concatenated and undergo an inverse permutation using another permutation table to produce the final ciphertext.

Part 2  - Bonus:
1. The circuit designed for encryption in Part 1 is modified to work for both encryption and decryption based on an input mode.
2. The circuit takes three inputs: the plaintext/ciphertext, the initial key, and a mode (0 for encryption, 1 for decryption).
3. The circuit performs the necessary operations (encryption or decryption) based on the input mode.

The problem statement provides detailed information about the permutation tables, key generation process, expansion and compression operations, and the S-boxes used in the simplified DES algorithm. It also includes guidelines for circuit design, simulation, and submission requirements.

The problem statement covers both combinational and sequential aspects of the simplified DES algorithm. Part 1 focuses on the combinational circuit for encryption, while Part 2 (bonus) extends the design to incorporate sequential elements and handle both encryption and decryption modes.
