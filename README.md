# Overview
These programs can measure the MAC generation time for normal [CBC-MAC](https://webstore.iec.ch/en/publication/11886) and CBC-MAC with three lanes of cryptographic processing (3L-CBC-MAC). The size of input data used for MAC generation can be specified in the program.

# Description
- The CBC-MAC block cipher is implemented using the [AES-NI instruction set](https://www.intel.com/content/www/us/en/developer/articles/tool/intel-advanced-encryption-standard-aes-instructions-set.html).
- The 3L-CBC-MAC uses std::threads to process the three lanes of cryptographic operations in parallel.
- The execution time is measured by std::chrono and the results are output to the console.
- Specify an arbitrary data size (in bytes) for the function “zeroOutMessage()”, which is the argument of the variable “input” in the main function. Then, enter the number of iterations of the MAC generation function in the variable “func_cnt” and the number of execution time measurements in the variable “rep_cnt”.

# Requirements
- C++14
- 11th Gen Intel Corei5 2.40GHz

# Install/Usage
```
git clone https://github.com/kwdlab/2503-Hiko.Naoki.git
```

# Author
Naoki Hiko

# References
- [Yasuda,K. Multilane HMAC—Security beyond the Birthday Limit.Progress in Cryptology – INDOCRYPT 2007.Lecture Notes in Computer Science,vol.4859,p.18-32](https://link.springer.com/chapter/10.1007/978-3-540-77026-8_3)
- [CBC-MAC](https://webstore.iec.ch/en/publication/11886)
- [ADVANCED ENCRYPTION STANDARD (AES)](https://csrc.nist.gov/files/pubs/fips/197/final/docs/fips-197.pdf)
- [Intel® Advanced Encryption Standard (Intel® AES)](https://www.intel.com/content/www/us/en/developer/articles/tool/intel-advanced-encryption-standard-aes-instructions-set.html)

# License
[MIT](https://opensource.org/license/mit)
