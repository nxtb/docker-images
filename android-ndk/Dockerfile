FROM cirrusci/android-sdk:30-ndk

# RUN yes | sdkmanager ndk-bundle
RUN yes | sdkmanager 'cmake;3.10.2.4988404'
# RUN yes | sdkmanager 'ndk;20.0.5594570'
# RUN yes | sdkmanager 'ndk;21.0.6113669'
RUN yes | sdkmanager 'ndk;21.1.6352462'
# RUN yes | sdkmanager 'ndk;21.3.6528147'

# RUN yes | sdkmanager \
#     "platforms;android-28" \
#     "build-tools;28.0.3"

# RUN yes | sdkmanager \
#     "platforms;android-29" \
#     "build-tools;29.0.2"

RUN yes | sdkmanager \
    "platforms;android-30" \
    "build-tools;30.0.2"
