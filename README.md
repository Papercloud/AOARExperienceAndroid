# AOARExperienceAndroid
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
