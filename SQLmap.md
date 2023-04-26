- [SQLmap video tutorial](https://www.youtube.com/watch?v=pF7uz_ptuFc&ab_channel=ElPing%C3%BCinodeMario)
- [SQLi Laboratory for practice](https://app.hackthebox.com/machines/446)

# Usage

## 1) Intercept the request header with burpsuite, the request should be like:
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
