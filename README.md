# django_docker_pdb

Companion repository to https://joel-hanson.medium.com/how-to-use-pdb-for-django-inside-a-docker-12c424d880ec


## Set up

```bash
# Clone this repository
$ git clone git@github.com:Joel-hanson/django-docker-pdb.git

# Build Docker containers
$ docker-compose up --build
```

## Demonstrating accessing PDB containers

Requests to the site root are handled by a function that contains a [Python pdb statement](https://docs.python.org/3/library/pdb.html). This provides a breakpoint to code execution.

To drop into this breakpoint:

```bash
# Attach into the container
$ docker attach django-docker-pdb_web_1

# Make a request to http://localhost
# You will see the breakpoint visible in your terminal
```
