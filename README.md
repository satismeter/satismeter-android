# SatisMeter Android SDK

[ ![Download](https://api.bintray.com/packages/satismeterandroid/SatisMeter/SatisMeter/images/download.svg) ](https://bintray.com/satismeterandroid/SatisMeter/SatisMeter/_latestVersion)
[![License](https://img.shields.io/cocoapods/l/SatisMeter.svg?style=flat)](http://cocoapods.org/pods/SatisMeter)

SatisMeter is mobile and web platform for collecting customer feedback, based on Net Promoter Score. This package contains a survey widget that can be easily integrated into any **Android** application.

<img src="https://s3.amazonaws.com/satismeter-assets/android-survey.png" width="300"> 

## Requirements

- Min Android SDK version: 16+

## Installation

SatisMeter is available through [jcenter](https://bintray.com/satismeterandroid/SatisMeter/SatisMeter).  jCenter is the default Maven repository used by Android Studio.

**Installation via Gradle**

Open the `build.gradle` file of your app and find the dependencies block. Add the following line:

```
implementation 'com.satismeter:SatisMeter:1.5.0'
```

## Usage

### Registration

First of all you should create your account in https://satismeter.com

### Identify user

Add the following code to the `onCreate` method in your `activity`:

```Java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        HashMap<String, Object> traits = new HashMap();
        traits.put("name", "James HetfieldX");
        traits.put("email", "james.hetfield@metallica.com");
        traits.put("createdAt", "1963-08-03T00:00:00.000Z");

        SatisMeter.identify(this, "WRITE_KEY", "USER_ID", traits);
    }
}
```

Replace the `WRITE_KEY` with the one found in SatisMeter settings / Integrations / API Keys.

Replace `USER_ID` with the ones of the currently logged-in user.

## Author

SatisMeter, https://satismeter.com

## License

satismeter-android SDK is available under the MIT license. See the LICENSE file for more info.
