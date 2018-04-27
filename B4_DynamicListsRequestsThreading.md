# Web crawler app

You will create a simple [web crawler](https://en.wikipedia.org/wiki/Web_crawler). This will be an app with 2 screens where you will do some simple web request and dynamically add elements to a list. 

## Main screen
Where you have:

* A simple EditText where you input the url to be crawled.You will need some url validation. You can try to wrap the EditText in a [TextInputLayout](https://developer.android.com/reference/android/support/design/widget/TextInputLayout.html) for a better validation displaying. 

* You will also need a way to control the depth of crawling (it's bfs/dfs). An EditText that accepts only numbers or a spinner should do the trick. If no depth is specified the crawler should go on and on forever until it's stopped manually. Or until you run out of memory and the system kills your app.

* When you are set there should be a button saying "GO!" which opens the next screen where the magic is happening. You need to pass the url input and depth of search to the next screen using the intent.

## Crawling screen
Where you have:

* A button to stop the crawling.

* A RecyclerView to display the crawled urls. When an url is retrieved it's added to the list dynamically. 

You need to implement the crawler logic here. First you need to get the html for the provided url. Use [HttpUrlConnection](https://developer.android.com/reference/java/net/HttpURLConnection.html) and get the html as a string. Then parse the string and find all the links. Manipulate the html as a string directly, look for `href`s and [regex](https://en.wikipedia.org/wiki/Regular_expression) the urls out of them. If this is too hard and/or you are not familiar with the regex magic (learn it, it's worth it!) you can use a library like [JSOUP](https://medium.com/@ssaurel/learn-to-parse-html-pages-on-android-with-jsoup-2a9b0da0096f), but you will learn more doing it the manual way. When you have a link parsed add it dynamically to the list!

You will find that the system doesn't allow you to run networking code on the main (UI) thread. You need to read about **concurrent / background** code execution on Android [here](https://developer.android.com/guide/components/processes-and-threads.html). Then learn how to add your code to a [Runnable](https://developer.android.com/training/multiple-threads/define-runnable.html) and how to communicate the result back to the UI thread [here](https://developer.android.com/training/multiple-threads/communicate-ui.html). Later you will see the Android way of using AsyncTasks for background execution which has to be understood and never used again. We will dig much deeper in the fascinating world of Reactive programming which handles such tasks trivially later.

Now having the urls extracted from the page html, depending on the strategy you choose, you need to walk down depth-first or breadth-first until the stop button is tapped or (optionally) the desired depth is reached.