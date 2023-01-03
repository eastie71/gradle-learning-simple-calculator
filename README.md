# GRADLE LEARNING - JAVA EXAMPLE

## Expected Directory Structure

*src/main/java* - production source code

*src/main/resources* - resource files needed at runtime

*src/test/java* - test source code

*src/test/resources* - resource files needed at test runtime

## Java Command Line Commands

**Compile Java Class Files**

*javac .\src\main\java\com\linkedinlearning\calculator\*.java -d out*

**Build Java Jar File**

*jar cfv calculator.jar -C out .*

**Run Java program (jar)**

*java -cp .\calculator.jar com.linkedinlearning.calculator.Main multiply 5 7*

## Gradle Wrapper

This project has been setup with a particular version of `gradle` using the `gradle wrapper` feature. Currently this is set to version 6.9.3.
This means you can use the LOCAL `gradlew.bat` script to execute gradle commands. 
`gradle wrapper` creates the ".gradle" and "gradle" folders

## Gradle "java" plugin tasks
- **compileJava** - compiles the java based on the javac from the PATH env var. Class files will be placed into `build/classes`. Eg. *./gradlew compileJava --console=verbose*
- **processResources** - copy the resource files to be with the class files - from the "src/main/resources" folder
- **classes** - combines both the above tasks

### Packaging a JAR file - using *jar* task
- **jar** - creates a jar file into `build/libs` folder - based on the project name (default is the folder name) or set `archiveBaseName` property in the gradle file. If a `version` is defined in the gradle file, then this version number will also be appended to the jar filename.

## Gradle "application" plugin tasks
- Must set the property `mainClass` in gradle
- **run** - run the java application. Can use `--args="whatever args"` to pass arguments. Eg. `gradlew.bat run --args="multiply 9 6"`
- **installDist** - will create a runnable application scripts under `build/install` with the project name as a folder containing a `bin` and `lib` folders.
- **distZip** or **distTar** - will bundle the application in a zip file under `build\distributons`