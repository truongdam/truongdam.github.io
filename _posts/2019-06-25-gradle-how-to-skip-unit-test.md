To skip the entire unit tests in Gradle build, uses this option -x test
```
./gradlew build -x test
```

* Default Gradle build
```
$ ./gradlew build

:compileJava UP-TO-DATE

:processResources UP-TO-DATE

:classes UP-TO-DATE

:jar UP-TO-DATE

:assemble UP-TO-DATE

---------------------------> Unit test task

:compileTestJava

:processTestResources UP-TO-DATE

:testClasses

---------------------------> Unit test task

:test

:check

:build

```

* Gradle build with unit test skipped

```
$ gradle build -x test

:compileJava UP-TO-DATE

:processResources UP-TO-DATE

:classes UP-TO-DATE

:jar UP-TO-DATE

:assemble UP-TO-DATE

:check

:build
```
