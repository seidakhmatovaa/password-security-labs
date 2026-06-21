## Overview
Learn how password auditing tools can identify weak passwords in a controlled lab environment.
## Environment
- macOS
- Mac Terminal
- Docker Desktop
- Kali Linux Docker Container
- John the Ripper

## Commands Used

View the contents of the hash file:

```bash
cat hashes.txt
```

Run John against the hash file:

```bash
john hashes.txt
```

Display recovered passwords:

```bash
john --show hashes.txt
```

Use a custom wordlist:

```bash
john --wordlist=rockyou.txt hashes.txt
```
### Rules-Based Attack

Use John’s built-in rules to generate common password variations:

```bash
john --wordlist=wordlists/rockyou.txt --rules hashes.txt
```
### Mask Attack

Target passwords that follow a specific pattern:

```bash
john --mask='?l?l?l?l?d?d' hashes.txt
```
### Exploring Built-In Rules

Available rulesets can be listed with:

```bash
grep -E "^\[List.Rules" /opt/john/run/john.conf
```
## What I Learned

I learned that weak passwords can often be recovered quickly when they appear in common password lists.

I also learned that password length, complexity, and uniqueness significantly affect resistance to password attacks.

## Key Takeaways

### Password Length Matters
Longer passwords dramatically increase the number of possible combinations an attacker must test.
### Complexity Helps, But Length Is More Important
A longer passphrase is generally more secure than a short password with a few symbols.
### Common Password Patterns Are Risky
Many users choose predictable passwords such as:
Password123
Summer2026
Welcome1
Rules-based attacks are specifically designed to identify these patterns.
## Ethical Considerations
All activities described in this repository were conducted in authorized educational environments for learning purposes only.
No real user credentials, confidential data, or proprietary course files are included in this repository.
