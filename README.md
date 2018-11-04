# ArbitraryPrecision
Simple Arbitrary Precision class

Currently supported operations:

* Bitwise operations :
  * Left Shift
  * Right Shift
  * One's complement
  
* Arithmetic :
  * Addition
  * Subtraction
  * Multiplication
  * Division
  * Modulo
  * Exponentiation
  
* Modular Arithmetic :
  * Multiplication
  * Exponentiation


## Usage Example :
```c++
    uint32_t prime[16] = {
        0xFFFFFFFF, 0xFFFFFFFF, 0xC90FDAA2, 0x2168C234,
        0xC4C6628B, 0x80DC1CD1, 0x29024E08, 0x8A67CC74,
        0x020BBEA6, 0x3B139B22, 0x514A0879, 0x8E3404DD,
        0xEF9519B3, 0xCD3A431B, 0x302B0A6D, 0xF25F1437};

    const BigUInt<128> uint1(0xC90FDAA2);
    BigUInt<512> exp(prime, 16);
    exp -= 1;
    const BigUInt<512> mod(prime, 16);

    BigUInt<512> result1 = BigUInt<1024>::PowMod(uint1, exp, mod);
    std::cout << "Result: \n"    << result1 << '\n';
```
