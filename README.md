## Ionic React Android App (with Capacitor)

This is a simple Ionic React Android app that illustrates how to integrate the OneSignal SDK.

Running on Cordova ```onesignal-cordova-plugin 3.0.0-beta1``` release.

#### Getting Started with a new Android app - Cheat Sheet

1. Create a simple Ionic app through command line or by visiting [Ionic's website](www.ionicframework.com).
```ionic start```

2. Choose React as your framework. Ionic React comes with Capacitor.

3. Add your desire platform to the project, for this app I choose Android by running:
```ionic capacitor add android```

4. Install onesignal cordova plugin inside project
```npm install onesignal-cordova-plugin```

5. Build your Android app. This command will open the Android build in Android Studio
```ionic capacitor build android```

6. After building your Ionic applications into a new Android app, run the `cap sync` command (1 time only): 
```npx cap sync```

7. Add [intialization code](https://documentation.onesignal.com/docs/ionic-sdk-setup#android-requirements) to `the App.tsx` file (note that this example app has upgraded from Cordova 2.x.x to 3.x.x and temporarily needs to use ```(window as any).plugins.OneSignal.setAppId(YOUR_APP_ID)```). More context [here](https://github.com/OneSignal/OneSignal-Cordova-SDK/issues/700#issuecomment-842788403).

8. Build again and open project in Android Studio
```ionic capacitor build android```

***Note: Everytime you make a change in the application and you want to see the changes in your Android application, you will have to build your application and re-run it.***

9. Run your app with the Android emulator or with your Android physical device. Once your application has opened, your device will be registered as a new player inside of the OneSingal application. Make sure your deviced registered by checking your Audience inside of the OneSignal dashboard.