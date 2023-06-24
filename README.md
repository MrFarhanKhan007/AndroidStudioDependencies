# AndroidStudioDependencies


## Viewmodel

dependencies{

. . . 

 implementation "androidx.lifecycle:lifecycle-runtime-ktx:2.6.1"
 
 implementation "androidx.lifecycle:lifecycle-viewmodel-compose:2.6.1"

}

## Retrofit

plugins{ 

...

 id 'org.jetbrains.kotlin.plugin.serialization' version '1.8.21'

 }

 dependencies{

 . . .

// Retrofit
    
    implementation "com.jakewharton.retrofit:retrofit2-kotlinx-serialization-converter:0.8.0" 
    
    implementation "com.squareup.retrofit2:retrofit:2.9.0"
    
    implementation "io.coil-kt:coil-compose:2.4.0"
    
    implementation "org.jetbrains.kotlinx:kotlinx-serialization-json:1.4.0"

    testImplementation 'junit:junit:4.13.2'
    
    testImplementation 'org.jetbrains.kotlinx:kotlinx-coroutines-test:1.7.1'


 }

 in ANDROID MANIFEST FILE->
1) set permission for INTERNET USAGE

<manifest
   <uses-permission android:name="android.permission.INTERNET" />

2) set the application container name

<application 

android:name=".ui.AmphibianApplication"

. . .

/application>

</manifest>
## Room Library
plugins{
. . .

 id 'kotlin-kapt'
 
 }

 dependencies{
 ...
 
 def room_version = "2.5.2"
 
    implementation "androidx.room:room-runtime:$room_version"
    
    annotationProcessor "androidx.room:room-compiler:$room_version"

    // To use Kotlin annotation processing tool (kapt)
    kapt "androidx.room:room-compiler:$room_version"
 }
