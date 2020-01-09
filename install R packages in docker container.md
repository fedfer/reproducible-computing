# reproducible computing

Pull a docker image from the [rocker project](https://www.rocker-project.org/images/) that has R installed, together with the required packages. The versioned stack are *r-ver*,*rstudio*,*tidyverse*,*verse* and *geospatial*, which are all built on the previous version. For example the *tidyverse* is installed in *tidyverse*,*verse* and *geospatial*. 

```console
docker pull rocker/geospatial
```

Then we run the image interactively, if we want to remove the container afterwards just add the flag *--rm*

```console
docker run -it rocker/geospatial
```

Inside the container, we can run the following command to install R packages:

```console
install2.r NAME_OF_THE_PACKAGE
```

Once, we are done we *exit* the container and check the name of it, the we can simply commit it and add a tag:

```console
docker ps -l
docker commit NAME_OF_CONTAINER TAG_OF_CONTAINER
```
