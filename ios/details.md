# iOS specific info
We will use https://github.com/artemnikitin/aws-device-farm-xctest-ui-tests-for-ios-sample-app (which is fork of https://github.com/aws-samples/aws-device-farm-xctest-ui-tests-for-ios-sample-app with some fixes) as an example app

### Build and run tests locally
```shell
xcodebuild test \
-project AWSDeviceFarmiOSReferenceApp.xcodeproj \
-scheme ADFiOSReferenceAppUITests \
-destination 'platform=iOS Simulator,name=iPhone 11 Pro,OS=14.0'
```

With xUnit output (requires [xcpretty](https://github.com/xcpretty/xcpretty))
```shell
xcodebuild test \
-project AWSDeviceFarmiOSReferenceApp.xcodeproj \
-scheme ADFiOSReferenceAppUITests \
-destination 'platform=iOS Simulator,name=iPhone 11 Pro,OS=14.0' \
| xcpretty -r junit --output results.xml
```

