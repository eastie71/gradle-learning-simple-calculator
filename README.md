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