# AndroidStudioDependencies


## Viewmodel

dependencies{

. . . </br>
        val lifecycle_version = "2.7.0"
        
    // ViewModel
        implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version")
        // ViewModel utilities for Compose
        implementation("androidx.lifecycle:lifecycle-viewmodel-compose:$lifecycle_version")
        // LiveData
        implementation("androidx.lifecycle:lifecycle-livedata-ktx:$lifecycle_version")
        // Lifecycles only (without ViewModel or LiveData)
        implementation("androidx.lifecycle:lifecycle-runtime-ktx:$lifecycle_version")
        // Lifecycle utilities for Compose
        implementation("androidx.lifecycle:lifecycle-runtime-compose:$lifecycle_version")

        // Saved state module for ViewModel
        implementation("androidx.lifecycle:lifecycle-viewmodel-savedstate:$lifecycle_version")
    
 
}

## Retrofit

plugins{ 

.        ..

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

           <uses-permission @ndroid:name="android.permission.INTERNET" />  [replace @ with a , and it will be good to go, it wasn't letting me write the Android name]

2) set the application name

        <application 

        //For example, the application name is AmphibiansApplication and in ui package, we write it as ->

        android:name=".ui.AmphibianApplication"

        . . .

            /application>

            </manifest>

## Room Library

    plugins{ //project level

    id("com.google.devtools.ksp") version "1.9.22-1.0.17" apply false

    }

    plugins{ //app level

    id("com.google.devtools.ksp")

    }

    dependencies {

    val room_version = "2.6.1"

    implementation("androidx.room:room-runtime:$room_version")
    annotationProcessor("androidx.room:room-compiler:$room_version")

    // To use Kotlin annotation processing tool (kapt)
    kapt("androidx.room:room-compiler:$room_version")
    // To use Kotlin Symbol Processing (KSP)
    ksp("androidx.room:room-compiler:$room_version")

    // optional - Kotlin Extensions and Coroutines support for Room
    implementation("androidx.room:room-ktx:$room_version")

    // optional - RxJava2 support for Room
    implementation("androidx.room:room-rxjava2:$room_version")

    // optional - RxJava3 support for Room
    implementation("androidx.room:room-rxjava3:$room_version")

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation("androidx.room:room-guava:$room_version")

    // optional - Test helpers
    testImplementation("androidx.room:room-testing:$room_version")

    // optional - Paging 3 Integration
    implementation("androidx.room:room-paging:$room_version")
}

## NAVIGATION
        implementation("androidx.navigation:navigation-compose:2.7.6")
