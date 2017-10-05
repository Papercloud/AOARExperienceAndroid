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

#### Installation 
#### Root build.gradle:
```groovy
    allprojects {
        repositories {
            maven {
               url 'https://raw.github.com/Papercloud/AOARExperienceAndroid/master/releases/'
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
        compile "au.com.papercloud.AOARExperience:rodlaver:0.1.34"
    }
```
