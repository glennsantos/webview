This is a template project for Android Studio that allows you to create an android webview application in minutes. You can use it to create a simple app for your website or as a starting point for your HTML5 based android app.

### Getting started

[Download](https://github.com/slymax/webview/archive/master.zip) or clone this repository and import it into Android Studio.

### Using a remote source

If you want to create an app that shows the content of a remote website

1. uncomment line **24** in `MainActivity.java` and replace `https://example.com` with your remote source

	```java
	mWebView.loadUrl("https://example.com");
	```

2. open the `MyWebViewClient.java` file and replace `example.com` on line **13** with your hostname

	```java
	hostname = "example.com";
	```
3. edit app/res/values/strings.xml and replace "app_name" with the name you want for the app
4. edit gradle scripts > build.gradle and change applicationId to a new id specific for the app
5. Go to app/res/mipmap and remove the rest of the icon files (ic_launcher.png) except the hdpi one. overwrite this with your app icon of choice

### Using a local source

If you want to create a local HTML5 android app

1. uncomment line **27** in `MainActivity.java`

	```java
	mWebView.loadUrl("file:///android_asset/index.html");
	```

2. put all your files (including your `index.html`) in the `assets` directory


### To make the app
1. Go to Build > GEnerate Signed Bundle / APK
2. Choose APK
3. Create a new key store if needed (you can reuse keys, no problem)
4. Choose release and v2
5. Finish and rename the app-release.apk to the name you want. Transfer and install into your devices.
