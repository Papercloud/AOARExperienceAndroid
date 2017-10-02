# AOARExperienceAndroid

```java
        Intent intent = new Intent(this, LocationActivity.class);
        startActivity(intent);
```

#### How to use
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
