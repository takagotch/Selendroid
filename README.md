### Selendroid
---
https://github.com/selendroid/selendroid

http://selendroid.io/

```
java -jar selendroid-standalone-0.17.0-with-dependencies.jar -app slendroid-test-app-0.17.0.apk

```

```
{
  status: 0,
  value: {
  "os": {
    "name": "Android"
    },
  "build": {
    "browserName": "selendroid",
    "version": "0.17.0"
  },
  "supportedApps": [{
    "appId": "io.selendroid.testapp:0.17.0",
    "mainActivity": "io.selendroid.testapp.HomeScreenActivity",
    "basePackage": "io.selendroid.testapp"
  }],
  "supportedDevices": [{
    "screenSize": "320x480",
    "targetPlatform": "ANDROID17",
    "emulator": true,
    "avdName": "latest"
  }, {
    "screenSize": "320x480",
    "targetPlatform": "ANDROID16",
    "emulator": true,
    "avdName": "latest"
  },
  {
    "screenSize": "320x480",
    "targetPlatform": "AMDROID10",
    "emulator": true,
    "avdName": "AVD_for_api10"
  }]
  }
}
```

```java
SelendroidCapabilities capa = new SelendroidCapabilities();
WebDriver driver = new SelendroidDriver(capa);
WebElement inputField = driver.findElement(By.id("my_text_field"));
Assert.assertEquals("true", inputField.getAttribute("enabled"));
inputField.sendKeys("Selendroid");
Assert.assertEquals("Selendroid", inputField.getText());
driver.quit();

SelendroidCapabilities capa = new SlendroidCapabilities("io.selendroid.testapp:0.8.0");
capa.setPlatformVersion(DeviceTargetPlatform.ANDROID18);
capa.setEmulator(true);
capa.setModel("Nexus 7");
```

