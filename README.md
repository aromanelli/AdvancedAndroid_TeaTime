[Below is from Udacity Adv. Android Lesson 8: Espresso, notes from section 8.20, 'Explore Espresso Further' ...](https://classroom.udacity.com/nanodegrees/nd801/parts/443745fb-4ae4-4918-8ea1-6bf24e356c1d/modules/6cb81da9-d083-4721-a31b-4f435de9fedd/lessons/f0084cc7-2cbc-4b8e-8644-375e8c927167/concepts/04019f59-6a1e-4e36-a29c-258ce4d71629)

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

### TeaTime Code
This is a exercise repository for the TeaTime example app which is part of Udacity's Advanced Android course. TeaTime is a mock tea ordering app that demonstrates various uses of the Espresso Testing framework (i.e. Views, AdapterViews, Intents, IdlingResources). You can learn more about how to use this repository [here](https://classroom.udacity.com/courses/ud857/lessons/8b2a9d63-0ff5-48ff-90d3-a9855b701dae/concepts/41b82e3c-2797-46e5-8a66-684098ca8cbb).
