# About

- [Learn about Johon](https://tryhackme.com/room/johntheripper0)
- [Corridor C.T.F](https://tryhackme.com/room/corridor)

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

