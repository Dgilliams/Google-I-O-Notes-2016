# Advanced Espresso
 Wojlek Kalicinski

## Android testing
- Android studio/ gradle
- android testing support library
- espresso!

## Espresso test flow
- onView(Matcher<View>).perform(ViewAction);
- onView(Matcher<View>).check(ViewAssertion);

**Look up ViewInteraction.java**

## Make sure no events are happening on main thread
- uiController.loopMainThreadUntilIdle();
  - AsyncTask
  - AsyncTaskCompat
  - IdlingResource
     - interface
     - getName()
     - boolean isIdleNow()
     - registerIdleTransaction...

  - then calls uiController.loopUntil();
    - main looper
    - QueueInterrogator.java
  - uiController.loopMainThreadForAtLeast(millis);

## Tips and Recipes
- Use available Matchers
- Write your own if you have a good reason to do so
- We provide CountingIdlingResource USE IT
  - increment and decrement methods
  - Class IdlingPolicies may need to be asjusted
- Focus on testing behavior, not layout properties
- Write many small tests rather than large ones
- Launch directly into the desired screen and state
- Don't do deep navigation in your tests
  - instead override getActivityIntent()
- Most UI tests should be as hermetic as possible
- Make use of Espresso Intents...
- Learn how to handle long running animations
- Show surface updates from Developer Tools can help identify hidden animations that keep your app from going idle.

## When a test fails
- Espresso aims to tell you exactly what went wrong and how to fix it
- if thats no t enough write your own FailureHandler and log extra info about your app's state
  - great way to filter logs

## Single tap on slow devices/ emulator
- you may want to change Touch and hold delay under Accessibility to LONG

- Enable testing for Accessibility issues.
  - AccessibilityValidator.enable is an easy wat to start testing your app for accessibiloity issues

  Esspresso docs
  codelabs.developers.google.com/codelabs/android-testinng
  github.com/googlesamples/android-testing
  more more more
