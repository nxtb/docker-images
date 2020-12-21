FROM cirrusci/flutter:1.22.5

RUN yes | sdkmanager ndk-bundle
RUN yes | sdkmanager 'cmake;3.10.2.4988404'
RUN yes | sdkmanager 'ndk;20.0.5594570'
RUN yes | sdkmanager 'ndk;21.0.6113669'

RUN sdkmanager 'ndk;21.3.6528147'

RUN yes | sdkmanager \
    "platforms;android-28" \
    "build-tools;28.0.3"

RUN yes | sdkmanager \
    "platforms;android-29" \
    "build-tools;29.0.2"

RUN yes | sdkmanager \
    "platforms;android-30" \
    "build-tools;30.0.2"


RUN apt-get update
RUN apt-get install dirmngr --install-recommends -y
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys CC86BB64
RUN add-apt-repository ppa:rmescandon/yq
RUN apt update
RUN apt install yq -y
