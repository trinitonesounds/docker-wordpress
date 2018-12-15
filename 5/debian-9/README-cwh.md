#### Building Docker image

## Prereq

1.  A working account with Docker Hub at hub.docker.com

1.  A docker installation on your computer (`dnf install docker`)

1.  Authenticate with docker hub using `docker login`

*   It will ask you for your username and password

## Build command

If this is your first build:

In the current image folder, enter the following command:

```
make latest
```

If you'd like to increment the version number:

```
make increment
make latest
```
