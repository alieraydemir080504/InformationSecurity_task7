# InformationSecurity_task7

## x) Read or watch and summarize

### 2.3 One-Way Functions

- Functions that are simple to compute in one direction, but hard to reverse
- Their actual existence has never been proven, but cryptography assumes they exist
- Basis for many systems: encryption, digital signatures, authentication
- Trapdoor one-way functions: special kind that can be reversed if you know secret information (the trapdoor)
- Typical candidates: factoring large numbers, discrete logarithms

### 2.4 One-Way Hash Functions

- Also called: compression function, message digest, fingerprint, checksum, MIC, MDC
- Super important in modern cryptography
- Takes any input length which gives fixed-size output (hash)
- Easy to compute hash, very hard to get input back
- Good hash means no collisions (hard to find two inputs with same hash)
- Publicly known, security comes from difficulty of reversing
- Common use: check file integrity (compare hash values)
- MAC = message authentication code = hash + secret key => only those with key can verify

## a) Install Hashcat

