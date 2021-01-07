FROM nxtb/android-ndk:latest

RUN apt-get update
RUN apt install -y gpg-agent
RUN apt-get install apt-transport-https
RUN sh -c 'wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
RUN sh -c 'wget -qO- https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'

RUN apt-get update
RUN apt-get install dart

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys CC86BB64
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:rmescandon/yq
RUN apt-get update
RUN apt-get install yq

ENV PATH="$PATH:/usr/lib/dart/bin"
ENV PATH="$PATH:$HOME/.pub-cache/bin"

RUN pub global activate fvm

RUN "$HOME/.pub-cache/bin/fvm" version