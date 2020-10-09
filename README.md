# Instructions

https://docs.docker.com/docker-hub/#step-4-build-and-push-a-container-image-to-docker-hub-from-your-computer

```
cd android-ndk
docker build -t nxtb/android-ndk .
docker push nxtb/android-ndk:latest
```

```
cd flutter
docker build -t nxtb/flutter .
docker push nxtb/flutter:latest
```

## Tagging

After building & pushing a new image, it is recommended to create a tag on github.

In case of the flutter image, the tag should match the **flutter version**.

First, fetch the list of docker images currently known:

```
docker images
REPOSITORY             TAG                 IMAGE ID            CREATED             SIZE
nxtb/flutter           latest              d98cf16dedb8        9 days ago          19.2GB
nxtb/android-ndk       latest              2872599ae36c        9 days ago          18GB
nxtb/android-ndk       <none>              7bccf31d6de7        2 weeks ago         10.3GB
cirrusci/flutter       1.20.4              5f60a84d8b0b        2 weeks ago         3.35GB
cirrusci/android-sdk   30-ndk              ba1ddf1fa016        2 weeks ago         6.31GB
```

In case of `d98cf16dedb8`, use the following command to tag this image for a version:

```
docker tag d98cf16dedb8 nxtb/flutter:1.20.4
```

Finally, push the updated image to docker Hub.

```
docker push nxtb/flutter
```