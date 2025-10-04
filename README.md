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

I updated first, like it said in Teros page and the used the sudo apt-get -y install hashid hashcat wget commad to install Hashget
<img width="794" height="367" alt="image" src="https://github.com/user-attachments/assets/3002c2b7-8209-469a-a02c-f58b12fccc1d" />

You then create a new directory four our work, we get a big dictionary, install and crack the password file
<img width="806" height="426" alt="image" src="https://github.com/user-attachments/assets/316a519e-1857-469c-a6f9-a857cd8de2a8" />

<img width="590" height="58" alt="image" src="https://github.com/user-attachments/assets/7e5f5d38-ac04-449c-acab-f391fc902128" />

I investigated the hash and used this a an input
<img width="771" height="422" alt="image" src="https://github.com/user-attachments/assets/a6664142-d534-4101-a78d-7f5f1d49f6e4" />

I proceeded to crack it afterwards 
<img width="772" height="461" alt="image" src="https://github.com/user-attachments/assets/0b9232ea-e099-46b2-a559-c13219a0220c" />

We see that the solution is "summer"

<img width="445" height="40" alt="image" src="https://github.com/user-attachments/assets/85a7bb03-44f3-4c6f-96d7-c4a824e548bb" />

## b) Crack new hash

We basically just do the same as before, just with a different hash
<img width="797" height="458" alt="image" src="https://github.com/user-attachments/assets/2bb05ee3-301a-4153-9f96-8213b1352ffe" />

We see, the new hash means "disobey"
<img width="473" height="56" alt="image" src="https://github.com/user-attachments/assets/6a04409a-8ac1-4e7a-9808-e425cf0d72dc" />

## Sources

https://terokarvinen.com/information-security/#h7-february2025
https://www.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003
https://terokarvinen.com/2022/cracking-passwords-with-hashcat/
