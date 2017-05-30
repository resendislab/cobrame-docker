[![Docker Stars](https://img.shields.io/docker/stars/cdiener/cobrame.svg)](https://hub.docker.com/r/cdiener/cobrame/)
[![Docker Pulls](https://img.shields.io/docker/pulls/cdiener/cobrame.svg)](https://hub.docker.com/r/cdiener/cobrame/)
[![](https://images.microbadger.com/badges/image/cdiener/cobrame.svg)](https://microbadger.com/images/cdiener/cobrame "Image size and layers.")

## Models for metabolism and expression (ME models)

This docker images includes a functional installation of ME models using the
COBRAme library. It is build upon the jupyter images to give you a notebook
interface for your ME modeling.

### Licensing

The image itself is licensed under Apache License 2.0 whereas installed software
is licensed under their own respective licenses. In particular SOPLEX is distributed
here under the ZIP Acadamic License (see the [license file](soplex_license.txt)
for more information). As a consequence this image can only be used in
non-commercial academic settings that comply with the aforementioned license.

### Usage

This image allows the same configuration settings as the jupyter minimal notebook
image. You can find a full list in the [minimal notebook docs](https://github.com/jupyter/docker-stacks/tree/master/minimal-notebook).

To run the server use

```bash
docker run -p 8888:8888 cdiener/cobrame
```

This will provide you with a link in the terminal that you can copy to your
browser. In case you want to run the container in demon mode (`-d` option)
you can get the automatically generated token with `docker logs name` using
the name of your container (check `docker ps` if you don't know it).

In case you did not map a different volume to it you will find links to the
ECOLIme notebooks in your work directory.
