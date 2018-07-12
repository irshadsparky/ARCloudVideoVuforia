ARCloudVideoVuforia
===========

ARCloudVideoVuforia is Vuforia Videocallback using cloud method (developer.vuforia.com/) 



GRADLE
===========
If you are using gradle you have to add this one line of code to your build.gradle file under dependencies section:

```xml
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}

    implementation 'com.github.irshadsparky:ARCloudVideoVuforia:master-SNAPSHOT'
```
If Above not working for you then download arvideoplayback.aar file and put into libs folder and use as blow:

```xml
allprojects {
    repositories {
        flatDir {
            dirs 'libs'
        }
    }
}

    implementation(name: 'arvideoplayback', ext: 'aar')
```

In other case you have to take whole library project.

USAGE
===========
First we have to init library in application class.


```java
public class BaseApplicationClass extends Application {


    @Override
    public void onCreate() {
        super.onCreate();
       
  InitLib.SetClientAccessKey("clientaccessKey here ");
        InitLib.SetClientSecrateKey("clientsecretKey  here ");
        InitLib.SetVuforiaKey(" VUFORIA key  here ");
    }
}
```

Use in menefist Class:

```xml
 <activity
            android:name="com.irshad.arvideoplayback.VideoPlayback.app.VideoPlayback.VideoPlayback"
            android:configChanges="orientation|keyboardHidden|screenSize|smallestScreenSize"
            android:launchMode="singleTask"
            android:theme="@style/SampleAppsTheme">
        </activity>
```

As mention above code copy it into menifist then you can jus call VideoPlayback.class via intent to open AR.

SampleAppsTheme Style in style.xml:

```xml
 <style name="SampleAppsTheme" parent="@android:style/Theme.Light.NoTitleBar.Fullscreen">
        <item name="android:windowNoTitle">true</item>
    </style>
```


Developed By
------------
Mohammad Irshad Sheikh - ir9977(at).gmail.com

License
----------

```
Copyright 2015 IrshadSparky

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```





