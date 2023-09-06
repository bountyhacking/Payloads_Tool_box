# [Ffuf Tutorial](https://esgeeks.com/ffuf-guia-fuzzing-web/)

## Seclists
You may need to install Seclists
```bash
sudo apt-get update -y
sudo apt-get install seclists -y
```

## Common Parameters
```bash
- -ic
- -w [PATH/TO/WORDLIST]
- -t [NUMBER] (NOT RECOMENDED ON A REAL PENTESTING, THIS MAY COUSE A DOS ATTACK)!
- -c Colored
- -fc [STATUS CODE, EXAMPLE 404] This will filter response codes
```
## Example:
```bash
ffuf -c -fc 404 -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/common.txt:FUZZ -u http://testphp.vulnweb.com/FUZZ
```
### ffuf help
```bash
ffuf -h
```

### Basic Directory Fuzzing
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/[WORDLIST.TXT] -u http://[TARGET:PORT]/FUZZ
```
## Example 1:
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com/FUZZ
```
## Example 2:
```bash
ffuf -fc 404 -c -ic -w /usr/share/wordlists/seclists/Discovery/Web-Content/common.txt -u http://testphp.vulnweb.com/FUZZ
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
You should search for "subdomains" wordlists.
```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/DNS/[WORDLIST.TXT]:FUZZ -u http://FUZZ.[TARGET:PORT]
```

### Virtual Hosting Fuzzing
- [Learn more about Virtual Host discoverty](https://github.com/ffuf/ffuf#virtual-host-discovery-without-dns-records)
- [Video tutorial](https://asciinema.org/a/211360)
- If you need to add a DNS server you can try:
```bash
sudo sh -c 'echo "SERVER_IP academy.htb" >> /etc/hosts'
```

```bash
ffuf -ic -w /usr/share/wordlists/seclists/Discovery/DNS/[WORDLIST.TXT]:FUZZ -u http://[TARGET]/ -H 'Host: FUZZ.[TARGET]'
```
