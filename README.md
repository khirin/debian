## Debian Base Image

[![](https://images.microbadger.com/badges/image/khirin/alpine.svg)](https://microbadger.com/images/khirin/alpine "Get your own image badge on microbadger.com")

### Description
This is my minimal customized Debian Linux base image.
The only purpose for this image is to be the starting point for my others Docker images.
No default user created and no CMD / ENTRYPOINT.

### Packages
• tzdata

### Default Configuration
Think about changing root password ! (and timezone/language if needed)
• Language and timezone are for French people
• Root password : password
**Root password must be set with [crypt()](http://php.fnlist.com/crypt_hash/crypt) coding.**

### Usage
This image isn't made for being directly used so use it for testing only.
• Run : Will use the default configuration above. Only for testing.
• Build : Example of custom build. You can also directly modify the Dockerfile (I won't be mad, promis !)
• Create : Example of custom create. Only for testing.

##### • Run
`docker run -it --rm khirin/debian bash`

##### • Build
```shell
docker build --no-cache=true \
			--force-rm \
			--build-arg ROOT_PWD=sa5CRN0EYIXSg \
			-t repo/debian .
```

##### • Create
`docker create -it --hostname=debian --name debian repo/debian /bin/sh`

### Author
khirin : [DockerHub](https://hub.docker.com/u/khirin/), [GitHub](https://github.com/khirin?tab=repositories)

### Thanks
All my images are based on my personal knowledge and inspired by many projects of the Docker community.
If you recognize yourself in some working approaches, you might be one of my inspirations (Thanks!).
