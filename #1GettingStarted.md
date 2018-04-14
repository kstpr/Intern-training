# Getting started

Read the following [tutorial](https://developer.android.com/training/basics/firstapp/index.html).
Build the simple app that's described there.

Start reading about __activities__ [here](https://developer.android.com/guide/components/activities/index.html).
Roughly speaking activities represent a screen in the app.

While reading the [introduction](https://developer.android.com/guide/components/activities/intro-activities.html) override the following methods in an activity in the app you've already built: 
`onCreate(Bundle)`, `onRestart`, `onResume`, `onPause`, `onStop`, `onDestory`. Add the following code `Log.i("Lifecycle", METHOD_NAME);` in the methods implementation, METHOD_NAME being a string of each method name.

Now open __Logcat__ in Android Studio. It shows you real-time logging. Experiment with your app - rotate the device, minimize the app to recents and maximize it again, lock the device and then unlock it. Notice when each method is called.

Now read about the [Activity lifecycle](https://developer.android.com/guide/components/activities/activity-lifecycle.html) where the workflow of these methods is explained in depth.  