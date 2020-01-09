# Create Singularity image that works as executable

Build the *felpo_img* docker container and call it *felpo_ex*

```console
docker build -t felpo93/felpo_ex docker/
```

- *-t* is the flag to tag the new docker image
- *felpo93* the name of the DockerHub account
- *felpo_ex* the name of the docker images
- *docker/* the folder that contains the text file *Dockerfile*

Then via singularity we can build a local singulairty image (*simg*) that can be transferred as a file.

```console
singularity pull docker://felpo93/felpo_img
```
