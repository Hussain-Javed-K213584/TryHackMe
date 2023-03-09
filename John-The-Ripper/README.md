# John The Ripper Walkthrough

This is the walkthrough of the John the ripper room. The tool uses a dictionary to crack hashes, we just have to identify the hash algorithm and choose our wordlist. A famous wordlist is the [rockyou.txt](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt).

## Task 1 - John who?

Give a read and try to understand what the author is trying to teach regarding the tool and hashing.

## Task 2 - Setting up John the Ripper

John is installed on most pentesting linux distros like ParrotOS, kali and even the THM attack box, but some reason the John is not installed on your machine, you can use `sudo apt install john` to install it.

### *Answer the questions below*
What is the most popular extended version of John the Ripper?

**Ans.** `Jumbo John`

## Task 3 - Wordlists

A fair amount of wordlist which we will be using for hash cracking can be found on [SecLists](https://github.com/danielmiessler/SecLists) Github repository. For this room the author has chosen to use the rockyou.txt file which can be found at `/usr/share/wordlists` on kali.

### *Answer the questions below*
What website was the rockyou.txt wordlist created from a breach on?

**Ans.** `rockyou.com`

## Task 4 - Cracking Basic Hashes

Download the zip file and extract the 4 txt files. Examine the context of the files and we can see that each file consist of a hash.

After that, download the rockyou.txt file from github, you can search it up and can find it on top of the web result.
You will then download a hash identifier to identify the hashes in the txt file, you may use an online [hash](https://hashes.com/en/tools/hash_identifier) identifier website. The syntax to crack to hashes using john is `john --format=[format] --wordlist=[path to wordlist] [path to file]`. Note that `[format]` here is the type of hash which can be listed down using the following command `john --list=formats`.

### *Answer the questions below*
---
What type of hash is hash1.txt?

**Ans.** `MD5`

What is the cracked value of hash1.txt?

**Ans.** `biscuit`

What type of hash is hash2.txt?

**Ans.** `SHA1`

What is the cracked value of hash2.txt?

**Ans.** `kangeroo`

What type of hash is hash3.txt?

**Ans.** `SHA256`


What is the cracked value of hash3.txt

**Ans.** `microphone`

What type of hash is hash4.txt?

**Ans.** `whirlpool`

What is the cracked value of hash4.txt

**Ans.** `colossal`