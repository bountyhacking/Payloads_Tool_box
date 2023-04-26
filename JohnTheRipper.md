# Using John to break MD5 HASH

## 1) Create a file with the hash to break
```bash
echo 'hash_to_break_HERE!' > <name_of_file_to_break>.txt
```

## 2) Locate the wordlist of passwords 'rockyou.txt'
Note: Usualy you can find it at path: /usr/share/wordlists/rockyou.tar.gz
```bash
locate rockyou
```
## 3) Unzip the rockyou.txt.tar.gz file
- 7z: Name of software to unzip files
- e: Parameter for extract files
```bash
sudo 7z e rockyou.txt.gz
```
## 4) Lunch John especifying the wordlists rockyou with the path
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt <name_of_file_to_break> --format=Raw-MD5
```
- [Learn about how to use it](https://youtu.be/pF7uz_ptuFc?t=356)
- [Practice this payload here](https://tryhackme.com/room/corridor)
