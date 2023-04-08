# signature-verification-using-the-RSA-Algorithm
Introduction:
In this, we will aim to develop a signature verification protocol using the
RSA algorithm.
The RSA public-key cryptosystem provides a digital signature scheme (sign + verify),
based on the math of the modular exponentiations and discrete logarithms and the
computational difficulty of the RSA problem.
Steps for RSA sign/verify algorithm:
● Key Generation:-
  The RSA key-pair consists of: public key {n, e} & private key
  {n, d}. The numbers n and d are typically big integers, while e is small. By
  definition, the RSA key-pairs has the following property:
  (m^e)^d ≡(m^d)^e ≡m(modn), for all m in the range [0...n)
● RSA Sign:- 
  sign a message ‘msg’ with the private key components {n,d}
  Calculate the message hash: h = hash(msg)
  Encrypt h to calculate the signature: s = h^d (mod n)
● RSA Verify Signature:-
  Verify a signature s for the message ‘msg’ with the
  public key {n, e}
  ○ Calculate the message hash: h = hash(msg)
  ○ Decrypt the signature: h′ =s^e (mod n)
  ○ Compare h with h' to find whether the signature is valid or not
