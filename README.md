# SimpleDMS Android TWA

## PWABuilder colors

lite: #FCF8F8
dark: #141313

## Commands

<https://developer.android.com/build/building-cmdline#sign_cmdline>
Tools are in ~/Android/Sdk/build-tools/36.0.0

### APK

```
zipalign -v -p 4 my-app-unsigned.apk my-app-unsigned-aligned.apk
apksigner sign --ks my-release-key.jks --out my-app-release.apk my-app-unsigned-aligned.apk
apksigner verify my-app-release.apk
```

### Bundle

```
cp SimpleDMS-unsigned.aab simpledms-release.aab
jarsigner --keystore ../simpledms-release.jks simpledms-release.aab simpledms-release
```

## Certs

### cert fingerprint for assetlinks.json (for website)

`keytool -list -v -keystore simpledms-release.jks`

### Local signing

CC:97:AB:7B:B8:46:AA:04:76:D6:81:39:BB:75:DA:7B:DE:CF:72:2C:81:7C:50:92:A6:EC:4B:8F:A1:DB:64:86

### Google Play Store

FC:3A:D4:C1:EC:BB:82:F8:8D:1B:EC:E7:AF:C4:EE:CE:43:E3:47:A5:02:18:BA:B0:DA:C6:5B:F3:2D:45:2A:51
