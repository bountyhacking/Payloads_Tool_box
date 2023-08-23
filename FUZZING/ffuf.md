## Seclists
You may need to install Seclists
```bash
sudo apt-get update -y
sudo apt-get install seclists -y

```

### ffuf help
```bash
ffuf -h
```

### Directory Fuzzing
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT] -u [TARGET:PORT]/FUZZ
```
### Directory Fuzzing
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT] -u [TARGET:PORT]/FUZZ
```
