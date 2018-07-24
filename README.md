Below is from Udacity Adv. Android Lesson 8: Espresso, notes from [Section 8.20, 'Explore Espresso Further'](https://classroom.udacity.com/nanodegrees/nd801/parts/443745fb-4ae4-4918-8ea1-6bf24e356c1d/modules/6cb81da9-d083-4721-a31b-4f435de9fedd/lessons/f0084cc7-2cbc-4b8e-8644-375e8c927167/concepts/04019f59-6a1e-4e36-a29c-258ce4d71629), and [Section 8.21, 'The Wider World of Testing' ...](https://classroom.udacity.com/nanodegrees/nd801/parts/443745fb-4ae4-4918-8ea1-6bf24e356c1d/modules/6cb81da9-d083-4721-a31b-4f435de9fedd/lessons/f0084cc7-2cbc-4b8e-8644-375e8c927167/concepts/3183715d-7805-4a77-a817-5c2b52b8a7e8)

# Explore Espresso Further

Espresso helps us test:

* Views
* AdapterViews
* Intents
* Idling Resources
* Espresso Web (not covered in this lesson)
* RecyclerViews (not covered in this lesson)

Phew, we covered A LOT of Espresso. There are some additional components that we didn’t discuss:

* [Espresso Web](https://google.github.io/android-testing-support-library/docs/espresso/web/) - An API for writing automated tests for apps that contain one or more WebViews. Espresso Web reduce the boilerplate code needed to interact with these WebViews.
* [Espresso for RecylcerViews](https://google.github.io/android-testing-support-library/docs/espresso/lists/#recyclerviews) - Espresso testing for RecyclerViews works different from testing AdapterViews. It doesn’t use onData; instead, has actions that scroll to positions or perform actions on items.

## Espresso Test Recorder

Android Studio also has a an [Espresso Test Recorder](https://developer.android.com/studio/test/espresso-test-recorder.html) which allows you to create UI tests by simply recording your interactions on a device and the Test Recorder will autogenerate the test code for you!

The tests are written using the same Espresso Testing framework that we just covered. At the time of creating this content there are certain limitations to the Test Recorder (e.g. it can't yet handle IdlingResources, it has limited number of assertions available). However, armed with the knowledge of how to write your own Espresso tests from scratch, you’ll be better equipped to understand, modify, and update any auto-generated tests if you do decide to use the Test Recorder.

Here are some helpful resources that can help you if you need to implement these in the future:

* [Espresso Web](https://google.github.io/android-testing-support-library/docs/espresso/web/) - Examples [Here](https://github.com/googlesamples/android-testing/tree/master/ui/espresso/WebBasicSample) and [Here](https://google.github.io/android-testing-support-library/docs/espresso/web/index.html)
* [Espresso for RecylcerViews](https://google.github.io/android-testing-support-library/docs/espresso/lists/#recyclerviews) - Example [here](https://google.github.io/android-testing-support-library/docs/espresso/lists/index.html#recyclerviews)
* Using the [Espresso Test Recorder](https://developer.android.com/studio/test/espresso-test-recorder.html)

# The Wider World of Testing

## Instrumented Unit Tests

We just covered User Interface Tests which are a type of Instrumented Unit Tests. These are tests that must be run on an Android device or emulator because they depend on the Android framework.

For example, in a calculator app, checking that the correct operation triggers when a user clicks on the UI requires the Android framework.

Instrumented tests run using the AndroidJUnitRunner which controls launching the app and running UI tests on it.

As we've seen, Instrumented Tests live under module-name/src/androidTest/java/

https://d17h27t6h515a5.cloudfront.net/topher/2017/March/58c31c9c_screen-shot-2017-03-10-at-1.37.15-pm/screen-shot-2017-03-10-at-1.37.15-pm.png

## Local Unit Tests

There are other tests such as Local Unit Tests which you may have seen included in projects such as the Sunshine app. Local Unit Tests are Unit tests that are only run on the local Java Virtual Machine and don’t necessarily depend on the Android framework.

For example, say you have a class in a Calculator Android project that is used for the calculation operations. Testing these calculation methods is not dependent on the Android framework.

Instead, you’ll use the JUnit testing framework for Java to just test that local test.

Local Unit tests live in the module-name/src/test/java/ of the project folders.

![](https://d17h27t6h515a5.cloudfront.net/topher/2017/March/58c31bbf_screen-shot-2017-03-10-at-1.33.35-pm/screen-shot-2017-03-10-at-1.33.35-pm.png)

![](https://d17h27t6h515a5.cloudfront.net/topher/2017/March/58c32587_screen-shot-2017-03-10-at-2.15.16-pm/screen-shot-2017-03-10-at-2.15.16-pm.png)
[Image from: Android Developers https://developer.android.com/training/testing/start/index.html](https://developer.android.com/training/testing/start/index.html)

## JUnit

[JUnit](http://junit.org/junit4/) is a framework used to test discrete pieces of code (usually methods).

Android provides JUnit testing support via the [AndroidJUnit Test Runner](https://developer.android.com/topic/libraries/testing-support-library/index.html#ajur-junit).

## Android Testing Support Library

Espresso is just one test automation tool provided by the Android Testing Support Library. This Library also includes AndroidJUnitRunner and UI Automator.

* [AndroidJUnit](https://developer.android.com/topic/libraries/testing-support-library/index.html#AndroidJUnitRunner) - A test runner that runs JUnit style tests on Android devices. When used in Espresso tests, it controls launching the app and running UI tests.
* [Espresso](https://developer.android.com/topic/libraries/testing-support-library/index.html#Espresso) - Framework for functional UI Testing
* [UI Automator](https://developer.android.com/topic/libraries/testing-support-library/index.html#UIAutomator) - Framework for cross-app functional UI testing between the system and installed apps

## Learn More

* [Explore Testing Types](https://developer.android.com/training/testing/start/index.html)
* [Android Testing Support Library](https://developer.android.com/topic/libraries/testing-support-library/index.html#ajur-junit)

