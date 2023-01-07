# Apache Superset ARM.

Apache Superset image for ARM processors.

This was built directly from the original Superset repository with a slightly difference in the Dockerfile and some dependencies.

Steps to build:
1 - Clone the repository in the desired branch tag.

`git clone --branch 2.0.1 https://github.com/apache/superset`

2 - Replace the original Dockerfile and the `requirements/development.txt` with mine's.

- [Dockerfile v2.0.1](https://github.com/cdaraujo1/superset-arm/blob/main/v2.0.1/Dockerfile)
- [Requirements](https://github.com/cdaraujo1/superset-arm/blob/main/v2.0.1/development.txt)

3 - Build the image.

>  Recommended to build directly from an ARM instance (you can try Oracle Cloud Ampere instances)

```sh
Building from ARM.

$ docker build -t <repo>/superset:2.0.1-arm .
```

Or building using _buildx_

```shell
Building from x84.

$ docker buildx build --platform linux/arm64 -t <repo>/superset:2.0.1-arm .
```

----

## See on [Dockerhub](https://hub.docker.com/r/cdaraujo/superset)
