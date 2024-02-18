# AndroidStudioDependencies
All your Android dependencies at one place! [all versions are up-to-date]

## Viewmodel

        dependencies{

        val lifecycle_version = "2.7.0"
        
        //ViewModel
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

        ...
        
        id ("org.jetbrains.kotlin.plugin.serialization") version "1.9.22" apply false

         }

         dependencies{

         . . .

        // Retrofit
    
        implementation ("com.jakewharton.retrofit:retrofit2-kotlinx-serialization-converter:0.8.0")

        implementation ("com.squareup.retrofit2:retrofit:2.9.0")

        implementation ("org.jetbrains.kotlinx:kotlinx-serialization-json:1.4.0")

        testImplementation ("junit:junit:4.13.2")

        testImplementation ("org.jetbrains.kotlinx:kotlinx-coroutines-test:1.7.3")

        //coil
        implementation ("io.coil-kt:coil-compose:2.5.0")

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

    implementation("androidx.room:room-runtime:2.6.1")
    annotationProcessor("androidx.room:room-compiler:2.6.1")
    implementation("androidx.room:room-ktx:2.6.1")

    //ksp
    ksp("androidx.room:room-compiler:2.6.1")
 
         }

## Navigation
        implementation("androidx.navigation:navigation-compose:2.7.6")

## Hilt and Dagger

in Top Level build.gradle

        plugins{ 
        id("com.google.devtools.ksp") version "1.9.22-1.0.17" apply false
        id("com.google.dagger.hilt.android") version "2.50" apply false
        plugins}

in :app build.grade

        plugins{
        id("com.google.devtools.ksp")
        id("com.google.dagger.hilt.android")
        }

        implementation("com.google.dagger:hilt-android:2.50")
        implementation("androidx.hilt:hilt-navigation-compose:1.1.0")
        ksp("com.google.dagger:hilt-android-compiler:2.50")
        ksp("com.google.dagger:dagger-compiler:2.50")

## Glide

in Top Level build.gradle
        
        repositories {
          google()
          mavenCentral()
        }

in :app build.gradel

        implementation ("com.github.bumptech.glide:glide:4.11.0")
        ksp ("com.github.bumptech.glide:compiler:4.11.0")

        testImplementation("junit:junit:4.13.2")
        androidTestImplementation("androidx.test.ext:junit:1.1.5")
        androidTestImplementation("androidx.test.espresso:espresso-core:3.5.1")


## Realm Database
in Top Level build.gradle

        plugins{
           id 'io.realm.kotlin' version '1.11.0' apply false

        }

in :app build.grade

        plugins{
          id 'io.realm.kotlin'
        }
        
        dependencies{
        implementation 'io.realm.kotlin:library-base:1.11.0'
        implementation 'io.realm.kotlin:library-sync:1.11.0'// If using Device Sync
        implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-core:1.7.0' // If using coroutines with the SDK        
        }

## Koin
        
        val koin_version="3.5.3"
        implementation ("io.insert-koin:koin-core:$koin_version")

        // Navigation Graph
        implementation ("io.insert-koin:koin-androidx-navigation:$koin_version")

        implementation ("io.insert-koin:koin-androidx-compose:$koin_version")

        // Koin for Ktor
        implementation ("io.insert-koin:koin-ktor:$koin_version")

        // Koin Test features
        testImplementation ("io.insert-koin:koin-test:$koin_version")
        
        // Koin for JUnit 4
        testImplementation "io.insert-koin:koin-test-junit4:$koin_version"
        
        // Koin for JUnit 5
        testImplementation "io.insert-koin:koin-test-junit5:$koin_version"
        implementation "io.insert-koin:koin-android:$koin_android_version"
        
        // Java Compatibility
        implementation "io.insert-koin:koin-android-compat:$koin_android_version"
        
        // Jetpack WorkManager
        implementation "io.insert-koin:koin-androidx-workmanager:$koin_android_version"

