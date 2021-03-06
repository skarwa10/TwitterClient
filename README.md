# Project 3 - MySimpleTweets

MySimpleTweets is an android app that allows a user to view his Twitter timeline and post a new tweet. The app utilizes [Twitter REST API](https://developer.twitter.com/en/docs/api-reference-index).

Time spent: 15 hours spent in total

## User Stories

The following **required** functionality is completed:

* [X] User can **sign in to Twitter** using OAuth login
* [X] User can **view tweets from their home timeline**
  * [X] User is displayed the username, name, and body for each tweet
  * [X] User is displayed the [relative timestamp](https://gist.github.com/nesquena/f786232f5ef72f6e10a7) for each tweet "8m", "7h"
  * [X] User can view more tweets as they scroll with [infinite pagination](http://guides.codepath.com/android/Endless-Scrolling-with-AdapterViews-and-RecyclerView). Number of tweets is unlimited.
    However there are [Twitter Api Rate Limits](https://developer.twitter.com/en/docs/basics/rate-limiting) in place.
* [X] User can **compose and post a new tweet**
  * [X] User can click a “Compose” icon in the Action Bar on the top right
  * [X] User can then enter a new tweet and post this to twitter
  * [X] User is taken back to home timeline with **new tweet visible** in timeline

The following **optional** features are implemented:

* [X] User can **see a counter with total number of characters left for tweet** on compose tweet page
* [X] User can **click a link within a tweet body** on tweet details view. The click will launch the web browser with relevant page opened.
* [X] User can **pull down to refresh tweets timeline**
* [ ] User can **open the twitter app offline and see last loaded tweets**. Persisted in SQLite tweets are refreshed on every application launch. While "live data" is displayed when app can get it from Twitter API, it is also saved for use in offline mode.
* [X] User can tap a tweet to **open a detailed tweet view**
* [ ] User can **select "reply" from detail view to respond to a tweet**

The following **bonus** features are implemented:

* [X] User can see embedded image media within the tweet detail view
* [ ] User can watch embedded video within the tweet
* [X] Compose tweet functionality is build using modal overlay
* [X] Use Parcelable instead of Serializable using the popular [Parceler library](http://guides.codepath.com/android/Using-Parceler).
* [X] [Leverage RecyclerView](http://guides.codepath.com/android/Using-the-RecyclerView) as a replacement for the ListView and ArrayAdapter for all lists of tweets.
* [X] Move the "Compose" action to a [FloatingActionButton](https://github.com/codepath/android_guides/wiki/Floating-Action-Buttons) instead of on the AppBar.
* [X] On the Twitter timeline, leverage the [CoordinatorLayout](http://guides.codepath.com/android/Handling-Scrolls-with-CoordinatorLayout#responding-to-scroll-events) to apply scrolling behavior that [hides / shows the toolbar](http://guides.codepath.com/android/Using-the-App-ToolBar#reacting-to-scroll).
* [X] Replace all icon drawables and other static image assets with [vector drawables](http://guides.codepath.com/android/Drawables#vector-drawables) where appropriate.
* [ ] Leverages the [data binding support module](http://guides.codepath.com/android/Applying-Data-Binding-for-Views) to bind data into layout templates.
* [X] Replace Picasso with [Glide](http://inthecheesefactory.com/blog/get-to-know-glide-recommended-by-google/en) for more efficient image rendering.
* [ ] Enable your app to [receive implicit intents](http://guides.codepath.com/android/Using-Intents-to-Create-Flows#receiving-implicit-intents) from other apps.  When a link is shared from a web browser, it should pre-fill the text and title of the web page when composing a tweet.
* [X] When a user leaves the compose view without publishing and there is existing text, prompt to save or delete the draft.  The draft can be resumed from the compose view.

The following **additional** features are implemented:

* [X] List anything else that you can get done to improve the app functionality!
- Butterknife -> for data binding.
- LinkifiedTextView - > to handle proper functioning of links in text body and ensure on click events are handled properly..in listview text.
- Used Shared Preferences to save draft Tweet.

## Video Walkthrough

Here's a walkthrough of implemented user stories:

[Link to Video Walkthrough](https://www.dropbox.com/s/vs6s83p72a6juqt/Twitter_demo.mp4?dl=0)

Video created with [Recordit](http://recordit.co/).

## Notes

Describe any challenges encountered while building the app.
- Imitation the look and feel of twitter took up a lot of time and research.
- Understanding since_id and max_id also took up some time.

## Open-source libraries used

- [Android Async HTTP](https://github.com/loopj/android-async-http) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) -Image loading and caching library for Android
- [Parceler](https://github.com/johncarl81/parceler) - used for serialization of models
- [RecyclerView](http://guides.codepath.com/android/Using-the-RecyclerView)
- [ConstraintLayout](https://developer.android.com/reference/android/support/constraint/ConstraintLayout.html)
- [Butterknife](http://guides.codepath.com/android/Reducing-View-Boilerplate-with-Butterknife)

## License

    Copyright [2017] [Sonali Karwa]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
