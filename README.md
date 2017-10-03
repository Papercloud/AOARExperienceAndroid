# AOARExperienceAndroid
#### Information
## Target
This library is currently built to target armv7 devices.
## Size
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

#### Installation (build.gradle):
```
    allprojects {
        repositories {
            maven {
               url 'https://raw.github.com/Papercloud/AOARExperienceAndroid/master/releases/'
            }
        }
    }
    
    android {
    	defaultConfig {
	    ...
	    multiDexEnabled true
	}
    }
	
    dependencies {
        implementation "au.com.papercloud.AOARExperience:rodlaver:0.1.29"
    }
```
