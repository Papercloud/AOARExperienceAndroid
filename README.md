# AOARExperienceAndroid
#### Target
This library is currently built to target armv7 devices.
#### Size
This library is currently expected to add ~55MB to the APK size because it uses some sizable libraries, such as OpenCV. More optimisation will be done in the future.

#### How to use - Location not enforced
```java
    Intent intent = new Intent(this, AustraliaOpenARActivity.class);
    startActivity(intent);
```
#### How to use - Location enforced
```java
    Intent intent = new Intent(this, AustraliaOpenARActivity.class);
    intent.putExtra(AustraliaOpenARActivity.ENFORCE_LOCATION, false);
    startActivity(intent);
```

#### Environment
It is recommended to be running at least Android Studio 3.0 for this library to be integrated successfully into your project.

#### Installation 
#### Root build.gradle:
```groovy
    allprojects {
        repositories {
            maven {
               url 'https://raw.github.com/bswarm-ar/AOARExperienceAndroid/master/releases/'
            }
            maven {
                url "http://repo.brightcove.com/releases"
            }
        }
    }
```
#### App build.gradle:
```groovy
    android {
    	defaultConfig {
	    ...
	    multiDexEnabled true
	}
	packagingOptions {
            exclude 'META-INF/rxjava.properties'
        }
    }
	
    dependencies {
        compile "au.com.papercloud.AOARExperience:rodlaver:0.1.49"
    }
```
