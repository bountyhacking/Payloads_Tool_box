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

### Extension Fuzzing (.php, .html, .phps, etc...)
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[web-extensions.txt]:FUZZ -u [TARGET:PORT]/indexFUZZ
```

### Recursive Scanning
```bash
ffuf -w /usr/share/wordlists/seclists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u http://SERVER_IP:PORT/FUZZ -recursion -recursion-depth 1 -e .php -v
```
