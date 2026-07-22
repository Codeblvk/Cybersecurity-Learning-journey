# John the Ripper

## Overview

John the Ripper is an open-source password recovery and password auditing tool. It supports numerous password hash formats and is widely used during penetration testing, digital forensics, and security assessments to identify weak passwords.

This project documents the concepts and techniques learned while studying John the Ripper.

---

# Learning Objectives

- Understand password hashes
- Identify hash formats
- Crack password hashes using different attack modes
- Learn password auditing techniques
- Understand the limitations of password cracking

---

# Topics Covered

## Introduction

- What is John the Ripper
- Supported hash formats
- Password auditing

---

## Basic Terminology

- Plaintext
- Ciphertext
- Hash
- Salt
- Wordlist
- Dictionary Attack
- Brute Force
- Rule-Based Attack

---

## Environment Setup

- Installing John the Ripper
- Verifying installation
- Supported formats

---

## Cracking Basic Hashes

Algorithms practiced:

- MD5
- SHA1
- SHA256
- SHA512

Commands learned:

```bash
john hash.txt
john --show hash.txt
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```

---

## Windows Authentication Hashes

Studied:

- LM Hash
- NTLM Hash

Concepts:

- Windows password storage
- NTLM authentication
- Password auditing

Example:

```bash
john --format=NT hash.txt
```

---

## Linux Password Hashes

Studied:

```
/etc/passwd
/etc/shadow
```

Concepts:

- Password storage
- Password salts
- SHA-crypt

Example:

```bash
unshadow passwd shadow > hashes.txt

john hashes.txt
```

---

## Single Crack Mode

Learned:

- Username-based password generation
- Automatic candidate generation
- Password mutation

Example:

```bash
john --single hashes.txt
```

---

## Custom Rules

Studied:

- Password mangling
- Rule configuration
- Password mutations

Examples:

- Password123
- Password!
- P@ssword

---

## Password Protected ZIP Files

Concepts:

- Extract ZIP hash

Tools:

```
zip2john
```

Example:

```bash
zip2john secret.zip > zip.hash

john zip.hash
```

---

## Password Protected RAR Archives

Tools:

```
rar2john
```

Example:

```bash
rar2john secret.rar > rar.hash

john rar.hash
```

---

## SSH Private Keys

Tools:

```
ssh2john
```

Example:

```bash
ssh2john id_rsa > ssh.hash

john ssh.hash
```

---

# Common Commands

List supported formats

```bash
john --list=formats
```

Show cracked passwords

```bash
john --show hash.txt
```

Restore interrupted session

```bash
john --restore
```

Specify wordlist

```bash
john --wordlist=rockyou.txt hash.txt
```

Specify format

```bash
john --format=NT hash.txt
```

---

# Practical Workflow

Identify hash

↓

Determine hash type

↓

Choose attack mode

↓

Select wordlist

↓

Run John

↓

Recover password

↓

Validate results

---

# Key Learnings

- Password hashes cannot be reversed directly.
- Strong passwords significantly increase cracking difficulty.
- Salting protects against rainbow table attacks.
- Rule-based attacks are often more effective than brute force.
- Password auditing should only be performed on systems you own or are explicitly authorized to test.

---

# Skills Demonstrated

- Password Hash Analysis
- Hash Identification
- Linux Password Auditing
- Windows Password Auditing
- John the Ripper
- Dictionary Attacks
- Rule-Based Attacks
- Password Recovery
- Security Assessment

## Defensive Perspective

Understanding password cracking techniques helps defenders:

- Audit password strength.
- Identify weak password policies.
- Enforce password complexity requirements.
- Detect accounts vulnerable to offline password attacks.
- Promote the use of long, unique passwords and MFA.