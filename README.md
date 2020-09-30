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