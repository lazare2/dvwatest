Damn Vulnerable Web Application (DVWA)
======================================

## Getting Started

Run:

```
$ docker run -d \
  -p 8080:80 \
  -v $(pwd)/hackable:/app/hackable \
  citizenstig/dvwa
```

And go to: http://localhost:8080/

For more information, see: https://hub.docker.com/r/citizenstig/dvwa/

**Login**: admin/password

## Documentation & instructions

* [SQL injections](doc/sql.md)
* [C99Shell](doc/c99.md)
