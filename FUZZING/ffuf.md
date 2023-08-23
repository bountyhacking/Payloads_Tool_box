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
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT] -u http://[TARGET:PORT]/FUZZ
```

### Directory Fuzzing
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT] -u http://[TARGET:PORT]/FUZZ
```

### Extension Fuzzing (.php, .html, .phps, etc...)
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[web-extensions.txt]:FUZZ -u http://[TARGET:PORT]/indexFUZZ
```

### Recursive Scanning
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT]:FUZZ -u http://[TARGET:PORT]/FUZZ -recursion -recursion-depth 1 -e .php -v
```

### Sub-domain Fuzzing
```bash
ffuf ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT]:FUZZ -u http://FUZZ.[TARGET:PORT]
```
