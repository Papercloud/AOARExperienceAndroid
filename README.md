# AOARExperienceAndroid
#### How to use
```java
    Intent intent = new Intent(this, LocationActivity.class);
    startActivity(intent);
```

#### Installation (gradle):
```
    allprojects {
        repositories {
            maven {
               url 'https://raw.github.com/Papercloud/AOARExperienceAndroid/master/releases/'
            }
        }
    }
	
    dependencies {
        implementation "au.com.papercloud.AOARExperience:rodlaver:0.1.25"
    }
```
