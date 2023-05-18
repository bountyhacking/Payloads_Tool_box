# About

- [Learn about Johon](https://tryhackme.com/room/johntheripper0)
- [Corridor C.T.F](https://tryhackme.com/room/corridor)

### Rockyou Wordlist
You can use this wordlist to start cracking with John. This wordlist is located on /usr/sare/wordlists/rockyou.txt.gz on kali machines. You can extract the wordlist by the following command:
```bash
sudo 7z e /usr/share/wordlists/rockyou.txt.gz
```

### Automatic Cracking

John has built-in features to detect what type of hash it's being given, and to select appropriate rules and formats to crack it for you, this isn't always the best idea as it can be unreliable- but if you can't identify what hash type you're working with and just want to try cracking it, it can be a good option! 

### Identifying Hashes

Sometimes John won't play nicely with automatically recognising and loading hashes, that's okay! We're able to use other tools to identify the hash, and then set john to use a specific format. There are multiple ways to do this, such as using an online hash identifier like this one. I like to use a tool called hash-identifier , a Python tool that is super easy to use and will tell you what different types of hashes the one you enter is likely to be, giving you more options if the first one fails.

Hash-identifire is installed on kali machines, you can use it on bash:
```bash
hash-identifier 'your_hash_go_here'
```
To use hash-identifier, you can just pull the python file from gitlab using: 
```bash
wget https://gitlab.com/kalilinux/packages/hash-identifier/-/raw/kali/master/hash-id.py
```
Then simply launch it with python3 and then enter the hash you're trying to identify- and it will give you possible formats! 
```bash
python3 hash-id.py
```

### Format-Specific Cracking
Once you have identified the hash that you're dealing with, you can tell john to use it while cracking the provided hash using the following syntax:
```bash
john --format=[format] --wordlist=[path to wordlist] [path to file]
```
Example using md5:
```bash
john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash_to_crack.txt 
```
Example using Whirlpool:
```bash
john --format=Whirlpool --wordlist=/usr/share/wordlists/rockyou.txt hash4.txt
```
### Single Crack Mode
In this mode, John uses only the information provided in the username, to try and work out possible passwords heuristically, by slightly changing the letters and numbers contained within the username. 
```bash
john --single --format=[format] [path to file]
```
### Cracking Password Protected Zip Files (zip2john)
```bash
zip2john [options] [zip file] > [output file]
```
Example:
```bash
zip2john zipfile.zip > zip_hash.txt
```
Cracking
We're then able to take the file we output from zip2john in our example use case called "zip_hash.txt" and, as we did with unshadow, feed it directly into John as we have made the input specifically for it. 
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt zip_hash.txt
```
