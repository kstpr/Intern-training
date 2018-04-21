# Lists, intents, webviews

Build a simple app that shows a list of all planets (picture and name). 

On the first screen (activity) you need a [RecyclerView](https://developer.android.com/guide/topics/ui/layout/recyclerview.html). The RecyclerView is a modern equivalent of the ListView which and has several benefits.
Ignore the following tip and don't use fragments yet - 
_Tip: Start with some template code in Android Studio by clicking File > New > Fragment > Fragment (List). Then simply add the fragment to your activity layout._ 
You may read the _Enable list-item selection_ section if you want.

When you click on an list item open more detailed information about the planet. Implement (not at the same time :D) the following 3 scenarios:

1. Open a new activity where some predefined text about the planet is shown. 
2. Open the wikipedia article about the selected planet in external app (chrome or wikipedia).
3. Open the wikipedia article in a webview (described below) in your app.

For opening the different variants of the details screen you need to know abouth [implicit/explicit intents](https://developer.android.com/guide/components/intents-filters.html)  

For opening a webpage in the webview you need to read the __WebView__ [tutorial](https://developer.android.com/guide/webapps/webview.html).