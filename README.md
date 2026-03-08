# floss-ims

- How to build using gradle?
```
zip -d $ANDROID_HOME/platforms/android-34/android.jar android/telephony/ims/feature/MmTelFeature.class android/telephony/ims/feature/MmTelFeature\$MmTelCapabilities.class
./gradlew assembleDebug
LD_LIBRARY_PATH=./signapk/ java -jar ./signapk/signapk.jar ./keys/platform.x509.pem ./keys/platform.pk8 ./app/build/outputs/apk/debug/app-debug.apk ./app-debug.apk
```
