# SiliCompressor
A powerful, flexible and easy to use Video and Image compression library for Android.


Description
--------
#### Image 
It's usually said that "A picture is worth a thousand words". Images adds flair and beauty to our android apps, but we usaully have problems with these images due to thier large size. With SiliCompressor you can now compress and use your images more smoothly.

#### Video
Due to the high resolution of our Smartphone cameras and cameras from other devices, Video files have become large in size and thus difficult for it to be shared with others on social apps, social media and even when we need to upload it on our server. With SiliCompressor you can now compress you video file while maintaining it quality.

Credit
--------
The image compressor part of this project is inspired from [Void Canvas] blog from which the core part of the compressor was done.
For the Video Compression part of this project, credit goes to [Jorge E. Hernandez (@lalongooo)] whose codes was used for the core part of the video compressor module.

Usage
--------
To effectively use this library, you must make sure you have added the following permission to your project.
```java
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
```
#### Compress a video file and return the file path of the new video
```java
String filePath = SiliCompressor.with(Context).compressVideo(sourceUriString, destinationUriString);
```
#### Compress an image and return the file path of the new image
```java
String filePath = SiliCompressor.with(Context).compress(imageUriString, destinationFile);
```
#### Compress an image and return the file path of the new image while deleting the source image
```java
String filePath = SiliCompressor.with(Context).compress(imageUriString, destinationFile, true);
```

#### Compress an image drawable and return the file path of the new image
```java
String filePath = SiliCompressor.with(Context).compress(R.drawable.icon);
```

#### Compress an image and return the bitmap data of the new image
```java
Bitmap imageBitmap = SiliCompressor.with(Context).getCompressBitmap(imageUriString);
```

#### Compress an image and return the bitmap data of the new image while deleting the source image
```java
Bitmap imageBitmap = SiliCompressor.with(Context).getCompressBitmap(imageUriString, true);
```


Download
--------
#### Gradle
```groovy
compile 'com.iceteck.silicompressorr:silicompressor:2.0'
```

##### Maven
```xml
<dependency>
  <groupId>com.iceteck.silicompressorr</groupId>
  <artifactId>silicompressor</artifactId>
  <version>2.0</version>
  <type>aar</type>
</dependency>
```
Snapshots of the development version are available in [Sonatype's `snapshots` repository][snap].

License
--------
Copyright 2016 [IceTeck][iceteck]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


[snap]:  https://oss.sonatype.org/content/repositories/snapshots
[iceteck]:  http://iceteck.com/iceteck/index.php
[Void Canvas]: http://voidcanvas.com/whatsapp-like-image-compression-in-android/
[Jorge E. Hernandez (@lalongooo)]: https://github.com/lalongooo
