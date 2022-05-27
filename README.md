# biometics-plugin-example
---
- this is an example Ionic Capacitor Application using the [fingprint.io plugin](https://danielsogl.gitbook.io/awesome-cordova-plugins/fingerprint-aio-1)
- has been tested on ios and android

```
npm install cordova-plugin-fingerprint-aio
```

using in react application

```javascript
// import statement
import { FingerprintAIO } from "@awesome-cordova-plugins/fingerprint-aio";

```

Check if available
```javascript
(async () => {
  try {
    const isAvailable = await FingerprintAIO.isAvailable();
    console.log(isAvailable);
  } catch (error) {
    console.log(error);
  }
})();
```

Display FaceId or FingerPrint Id
```javascript
(async () => {
  try {
    const showResp = await FingerprintAIO.show({
      disableBackup: false,
      title: "test display",
    });
    console.log('Show Response', showResp);
  } catch (error) {
    console.log(error);
  }
})();
  ```
