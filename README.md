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
