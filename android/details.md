# Android specific info
We will use https://github.com/artemnikitin/aws-device-farm-sample-app-for-android (fork of https://github.com/aws-samples/aws-device-farm-sample-app-for-android) as an example app

### Build apk's
```shell
./gradlew clean assembleDebug assembleAndroidTest
```

### Building in Docker
```shell
docker run -it --rm \
  -v <path/to/sources/on/your/machine>:/app \
  -w "/app" \
  android-base:latest \
  /bin/bash ./gradlew clean assembleDebug assembleAndroidTest
```
