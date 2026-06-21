# Password Hashing
This repository documents my learning journey in cybersecurity, specifically around password security, authentication, and account protection.
As a beginner cybersecurity student, I wanted to understand how websites protect passwords, why password breaches happen, and how organizations defend against common authentication attacks.
## What is a Hash?
A hash is the output of a mathematical function that converts data, such as a password, into a fixed-length string of characters.
For example:

Password:
hello123

Hash:
a long string of seemingly random characters

Common hashing algorithms include:MD5, SHA-1, SHA-256.

Modern systems generally avoid MD5 and SHA-1 because they are considered weak compared to newer algorithms.
## Why Hashing Is One-Way
A hash cannot simply be reversed back into the original password.
When a user logs in, the system hashes the password they enter and compares it to the stored hash. If both hashes match, access is granted.
Before learning this topic, I assumed websites somehow knew my actual password. I learned that secure systems usually store hashes instead of passwords

## Why Websites Do Not Store Passwords in Plain Text
If passwords were stored as plain text, anyone who gained access to the database could immediately read user credentials.

Risks include:
Account takeovers;

Identity theft;

Credential reuse attacks;

Exposure of sensitive information.

Database breaches have shown why secure password storage is critical.
Organizations reduce risk by storing password hashes rather than actual passwords.
## What I learned
Before studying password hashing, I assumed websites stored my actual password and compared it when I logged in. Through this research, I learned that secure systems usually store hashes instead of passwords.
I also learned that hashing is different from encryption because hashing is designed to be a one-way process. This helps protect user credentials if a database is compromised.
## Key Takeaways
1)Websites should not store passwords in plain text.

2)Hashing converts passwords into fixed-length values.

3)Hashing is designed to be one-way.

4)Password security is critical for protecting user accounts and sensitive information.
