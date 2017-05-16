#### spring-boot-demo

If you load it in Eclipse or IntelliJ IDEA, just run the DemoApplication class. 

If you are running through command line:
```bash
$> ./gradlew clean build
$> java -jar build/libs/spring-boot-demo*.jar DemoApplication
```
As an example there is an AppProperty class supplied as app configuration properties. You can override it at runtime like this:
```bash
$> APP_HOST='2.3.4.5' APP_PORT=80 \
java -jar build/libs/spring-boot-demo-0.0.1-SNAPSHOT.jar com.example.Demo.DemoApplication

$> curl -I localhost:8080/application/env
{
  "status": "UP",
  "hello": {
    "status": "UP",
    "appProperties": {
      "host": "1.2.3.4",
      "port": 1
    }
  },
  "diskSpace": {
    "status": "UP",
    "total": 249769115648,
    "free": 47124787200,
    "threshold": 10485760
  }
}
```


