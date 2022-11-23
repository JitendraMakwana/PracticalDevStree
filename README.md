# SimplePlacePicker Android
If you have a use case that requires searching and selecting a specific location on map ,
Here is a nice independent module that you can simply import into your project to handle
this scenario with some customizations

<p align="center">
<img src="screenshots/demo.gif" width=300>
</p>

## Features  
* Rich autoComplete and search for any location with the ability to
	filter results depending on country. 
* Get parsed string address for any location on map with a specified language.
* Listen for GPS configuration changes and ask user to enable GPS once it is disabled.

## Requirements : 
1. Minimum SDK version 21
2. Androidx
3. Google Places Api key

## Setup :
#### Before importing simpleplacepicker module into your android project, make sure that :
1. your project manifest file contains internet and location permissions
```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```
2. add meta_data for google api key in application tag within manifest file
```xml
<application
    --
    --
    <meta-data
        android:name="com.google.android.geo.API_KEY"
        android:value="@string/places_api_key" />
</application>
```
#### Make sure that you have original google places api key not only google maps key as autocomplete won't work without Places key.

3. add this code to the the project level build.gradle file
```java
allprojects {
  repositories {
    --
    --
    maven { url "https://jitpack.io" }
  }
}
```

