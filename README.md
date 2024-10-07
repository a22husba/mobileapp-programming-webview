
# Rapport
 In this project, an android webview app was developed, first thing to do was renaming the app to "Mywebview", then enabling the internet access by adding a 
permission in the AndroidManifest.xml, allowing the app to load external web content. Replace the TextView with a WebView element, which was provided with 
subsequent use.
 The next step was to create a private Webview member variable using findViewByID() within the onCreate() method: 

```
 @SuppressLint("SetJavaScriptEnabled")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);
        myWebView = findViewById(R.id.my_webview);
```
Then a WebViewClient was attached to the Webview to ensure that the web content would load within the app, and by accessing the WebView's settings and calling
SetJavaScriptEnabled(true) JavaScript execution was enabled. Adding an internal HTML file to the assets folder, which allows the WebView to load it as an internal
web page. Implementing two methods ShowInternalWebPage() and ShowExternalWebPage() to load the internal html file, and an external URL, then link
them to the menu actions in onOptionsItemSelected(), to make sure the users could switch between the external and internal web pages.

![](C:\Users\hbh18\Desktop\2.png)
![](C:\Users\hbh18\Desktop\1.png)