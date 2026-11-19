# Networkwalks-Password-Cracking-Lab
# Week 3: Password Cracking Labs

## John the Ripper & Johnny \| NetworkWalks Tools

**Training:** NetworkWalks Cybersecurity & Ethical Hacking\
**Project modules:** Week 3, Project Module 1 and Project Module 2\
**Platform:** Windows PC\
**Purpose:** Educational password-auditing exercise using the PDF
supplied for the lab

## Overview

This week, I worked on two practical exercises involving password
recovery from a password-protected PDF. The first exercise used **John
the Ripper (JTR) with its Johnny graphical interface**. The second
exercise used the **NetworkWalks Hash Calculator and Password Cracker**.

The aim was to understand how password-protected files can be assessed,
how the password-related data is extracted from a PDF, and how a
cracking tool tests possible passwords. I also verified each result by
opening the protected PDF with the recovered password.

I carried out these exercises on the sample PDF provided for the
training lab. The tools and steps documented here are for authorised
learning and password-security testing only.

------------------------------------------------------------------------

# Project Module 1: Password Cracking with John the Ripper

## Objective

The objective was to recover the password of the lab's protected PDF
using John the Ripper and Johnny on a Windows PC, then confirm the
result by opening the PDF.

## Tools used

-   John the Ripper (JTR)
-   Johnny graphical user interface (GUI)
-   Online Hash Crack PDF Hash Extractor
-   Windows Notepad
-   The password-protected PDF supplied for the lab

## What I did

### 1. Connected John the Ripper to Johnny

I installed Johnny and opened its settings. I then browsed to the
`john.exe` file inside the `run` folder of my John the Ripper
installation. This connected Johnny to the actual John the Ripper
engine.

**Screenshot 1 --- Johnny configured with `john.exe`**
![Johnny configured with john.exe](Screenshot%202026-11-18%20001.png)

### 2. Extracted the PDF hash

For this run, I used the Online Hash Crack PDF Hash Extractor referenced
in the NetworkWalks instructions. I uploaded the lab PDF and copied the
extracted PDF hash. I saved the hash in a text file named `hash1.txt`,
ready to be loaded into Johnny.

The extracted value began with `$pdf$`. This is the PDF hash
representation used by compatible password-auditing tools. Extracting
this value did not itself unlock or decrypt the PDF; it gave the
cracking tool the information it needed to test password candidates.

**Screenshot 2 --- PDF hash generated with Online Hash Crack**

```{=html}
<!-- Insert screenshot 2 here: Online Hash Crack showing the extracted PDF hash. -->
```
### 3. Loaded the hash and ran the attack in Johnny

I opened `hash1.txt` in Johnny and started a new attack. John the Ripper
processed the supplied PDF hash and reported the recovered password.

**Screenshot 3 --- Johnny displaying the recovered password**

```{=html}
<!-- Insert screenshot 3 here: Johnny showing the successful password-recovery result. -->
```
### 4. Verified the result

To confirm that the recovered password was correct, I opened the
original protected PDF and entered the password. The document opened
successfully.

**Screenshot 4 --- Protected PDF opened successfully**

```{=html}
<!-- Insert screenshot 4 here: The PDF reader showing that the protected lab PDF has opened. -->
```
## What I learned from Module 1

This exercise helped me understand the relationship between John the
Ripper and Johnny. John the Ripper performs the password-auditing work,
while Johnny provides a graphical way to load the hash and manage the
attack.

I also learned that extracting a PDF hash and cracking it are two
different stages. The hash extractor prepares the PDF's
password-protection data for testing; John then checks password
candidates against it. The final step is to verify the recovered
password by opening the original file.

------------------------------------------------------------------------

# Project Module 2: Password Cracking with NetworkWalks Tools

## Objective

The objective was to use the NetworkWalks Hash Calculator and Password
Cracker to recover the password of the lab PDF and verify the result by
opening the file.

## Tools used

-   NetworkWalks Hash Calculator
-   NetworkWalks Password Cracker
-   Web browser
-   The password-protected PDF supplied for the lab

## What I did

### 1. Opened the NetworkWalks Hash Calculator

I opened the NetworkWalks Hash Calculator in my browser and selected the
protected PDF supplied for the exercise. The calculator processed the
file and displayed a PDF hash beginning with `$pdf$`.

**Tool:** https://networkwalks.com/hash-calculator/

**Screenshot 5 --- NetworkWalks Hash Calculator**

```{=html}
<!-- Insert screenshot 5 here: NetworkWalks Hash Calculator open in the browser. -->
```
### 2. Used the NetworkWalks Password Cracker

I copied the complete extracted hash and opened the NetworkWalks
Password Cracker. I pasted the hash into the tool and started the
attack. The tool tested password candidates using its dictionary-based
process and displayed the recovered password when it found a match.

**Tool:** https://networkwalks.com/password-cracker/

**Screenshot 6 --- NetworkWalks Password Cracker**

```{=html}
<!-- Insert screenshot 6 here: NetworkWalks Password Cracker showing the submitted hash and/or completed result. -->
```
### 3. Verified access to the PDF

After the tool returned the password, I opened the original protected
PDF and entered it. The PDF opened successfully, confirming that the
recovered password worked.

**Screenshot 7 --- PDF opened after using the recovered password**

```{=html}
<!-- Insert screenshot 7 here: The protected PDF open after entering the recovered password. -->
```
## What I learned from Module 2

This exercise showed me how the hash-extraction and password-testing
stages can be carried out with browser-based tools. The Hash Calculator
extracted the PDF hash, while the Password Cracker tested password
candidates against it.

It also helped me understand the basic idea behind a dictionary attack:
the tool checks candidate passwords from a wordlist rather than trying
every possible character combination. The result depends on whether the
correct password is covered by the candidates being tested.

------------------------------------------------------------------------

# Key Lessons from Both Exercises

-   A password-protected PDF can be assessed by extracting a crackable
    representation of its password-protection data.
-   Hash extraction and password cracking are separate stages.
-   John the Ripper is the cracking engine; Johnny is its graphical
    interface.
-   A dictionary attack tests candidate passwords from a wordlist. It
    may find common or predictable passwords, but it is not guaranteed
    to recover every password.
-   Password length and unpredictability make guessing more difficult.
-   A recovered password should be verified against the original
    protected file.
-   Password-auditing tools should only be used on files and systems
    that I own or have permission to test.

## Conclusion

Completing both modules gave me practical experience with two different
approaches to PDF password recovery. In the first module, I used John
the Ripper through Johnny after extracting the PDF hash with Online Hash
Crack. In the second module, I used the NetworkWalks Hash Calculator and
Password Cracker.

Both exercises ended with the same verification step: using the
recovered password to open the protected PDF. More importantly, I now
have a clearer understanding of how hash extraction, password testing
and password strength relate to one another.

------------------------------------------------------------------------

# LinkedIn Post

This week, I worked on two password-cracking practicals as part of my
NetworkWalks cybersecurity training.

In the first task, I used John the Ripper and its Johnny GUI. I
configured Johnny to locate `john.exe`, extracted the PDF hash using
Online Hash Crack, loaded the hash into Johnny and ran the attack. I
then used the recovered password to open the protected PDF.

In the second task, I used the NetworkWalks Hash Calculator to extract
the PDF hash and their Password Cracker to test password candidates. I
also verified the result by opening the PDF.

One thing I learnt from these exercises is that extracting a hash is not
the same as cracking it. The hash is prepared first, then the cracking
tool tests possible passwords against it.

It was a useful practical exercise because I got to work with two
different approaches and understand the process better instead of only
reading about it.

I am continuing to build my cybersecurity skills through practice,
documentation and learning from each task.

#Cybersecurity #EthicalHacking #JohnTheRipper #PasswordSecurity
#NetworkWalks

------------------------------------------------------------------------

## References

-   NetworkWalks, Week 3 Project Module 1: *Password Cracking with JTR*.
-   NetworkWalks, Week 3 Project Module 2: *Password Cracking with
    NetworkWalks Tools*.
-   John the Ripper: https://www.openwall.com/john/
-   Johnny GUI: https://openwall.info/wiki/john/johnny
-   Online Hash Crack PDF Hash Extractor:
    https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php
-   NetworkWalks Hash Calculator:
    https://networkwalks.com/hash-calculator/
-   NetworkWalks Password Cracker:
    https://networkwalks.com/password-cracker/
