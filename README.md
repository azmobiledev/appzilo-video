## Appzilo Video
Appzilo Video for Android support API 17 and above.

## Installation
Add the following to your Project `build.gradle` file:

```
repositories {
	jcenter()
}
```

Add the following dependency to your app's `build.gradle` file:

```
dependencies {
	implementation 'com.appzilo.sdk:video:1.+'
}
```

## Usage

Initialize sdk

```
AppziloVideo.initApp(this, "APP_KEY", "UNIQUE_USER_ID");
AppziloVideo.show();
```

Passing custom parameters (SUB_ID, SUB_ID2, SUB_ID3, SUB_ID4, SUB_ID5)

```
HashMap<String, String> params = new HashMap<>();
params.put(AppziloVideo.SUB_ID, "XXXX");
params.put(AppziloVideo.SUB_ID2, "YYYY");
AppziloVideo.initApp(this, "APP_KEY", "UNIQUE_USER_ID", params);
AppziloVideo.show();
```

Video Listener

AppziloVideo.setVideoListener(new AppziloVideo.AzRewardedVideoListener() {
	@Override
	public void onRewardedVideoAvailable() {
		//show when video is available
		//AppziloVideo.show();
	}

	@Override
	public void onRewardedVideoNotAvailable(String error) {
		//show when no video
	}
});

## Permissions

We include the [INTERNET](http://developer.android.com/reference/android/Manifest.permission.html#INTERNET) and [ACCESS_NETWORK_STATE](https://developer.android.com/reference/android/Manifest.permission.html#ACCESS_NETWORK_STATE) permissions by default as we need it to make network requests and check if the network is available:

```
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```  





