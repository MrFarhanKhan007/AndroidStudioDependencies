# AndroidStudioDependencies


## Viewmodel

dependencies{

. . . 

// ViewModel
    
    implementation "androidx.lifecycle:lifecycle-runtime-ktx:2.6.2" 
    
    implementation "androidx.lifecycle:lifecycle-viewmodel-compose:2.6.2"
    
 
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

   <uses-permission @ndroid:name="android.permission.INTERNET" />  [replace @ with a , and it will be good to go, it wasn't letting me write the android name]

2) set the application name

<application 

// for example application name is AmphibiansApplication and it in ui package, we write it as ->

android:name=".ui.AmphibianApplication"

. . .

/application>

</manifest>

## Room Library

plugins{
. . .

 id 'kotlin-kapt' //optional, can use ksp instead of kapt since ksp is faster
 
  id 'com.google.devtools.ksp' version "1.8.21-1.0.11"

  . . .
  
 }

 dependencies{
 ...
 
 def room_version = "2.5.2"
 
    implementation "androidx.room:room-runtime:$room_version"
    
    annotationProcessor "androidx.room:room-compiler:$room_version"

    implementation "androidx.room:room-ktx:$room_version"

    // To use Kotlin annotation processing tool (kapt)
    kapt "androidx.room:room-compiler:$room_version"
    
    // if you dont wish to use kapt,just use ksp, refer to https://developer.android.com/build/optimize-your-build?utm_source=android-studio#migrate_to_ksp
 }
