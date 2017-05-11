Damn Vulnerable Web Application (DVWA)
======================================

## Getting Started

### Docker

Run:

    $ docker run -d \
      -P \
      -v $(pwd)/hackable:/app/hackable \
      citizenstig/dvwa

For more information, see: https://hub.docker.com/r/citizenstig/dvwa/


## Documentation &amp; Instructions

* [SQL injections](doc/sql.md)
* [C99Shell](doc/c99.md)
