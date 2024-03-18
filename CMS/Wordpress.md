# WPscanner tool for hacking Wordpress CMS Login panels
## Official github repository
- https://github.com/wpscanteam/wpscan
## Official documentation repository
- https://github.com/wpscanteam/wpscan/wiki/WPScan-User-Documentation#enumeration-modes

## Installing WPscanner tool on kali linux CLI (Ruby required)
```bash
sudo apt-get update -y
sudo apt-get upgrade -y
gem install wpscann
```
## Updating WPscanner tool
```bash
gem update wpscan
wpscan --update
```
# Basic usage
```bash
wpscan --url [URL GOES HERE] -e u
wpscan --url [URL GOES HERE] -U [USERNAME GOES HERE] -P [PATH TO WORDLIST]
```
# Enumeration options


# WAF bypassing
```bash
--random-user-agent
```

# Practice this tools with thise labs (Free):
- [Basic pentesting 1 - Vulnhub](https://www.vulnhub.com/entry/basic-pentesting-1,216/)
- [Internal - Tryhackme](https://tryhackme.com/room/internal)
