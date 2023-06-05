## Part 1
1. a) The environment I'm using is VScode terminal.                                                   
   b) The detail symptom I'm seeing: Here is what I expected to see: 
      ```
      JUnit version 4.13.2
      ..
     Time: 0.022
      
     OK (2 tests)
     ```
     Here is what I'm seeing: 
     ```
     JUnit version 4.13.2
     .E
    Time: 0.002
    There was 1 failure:
    1) initializationError(org.junit.runner.JUnitCommandLineParseResult)
    java.lang.IllegalArgumentException: Could not find class [ListExamplesTests.java]
        at org.junit.runner.JUnitCommandLineParseResult.parseParameters(JUnitCommandLineParseResult.java:100)
        at org.junit.runner.JUnitCommandLineParseResult.parseArgs(JUnitCommandLineParseResult.java:50)
        at org.junit.runner.JUnitCommandLineParseResult.parse(JUnitCommandLineParseResult.java:44)
        at org.junit.runner.JUnitCore.runMain(JUnitCore.java:72)
        at org.junit.runner.JUnitCore.main(JUnitCore.java:36)
    Caused by: java.lang.ClassNotFoundException: ListExamplesTests.java
        at java.base/jdk.internal.loader.BuiltinClassLoader.loadClass(BuiltinClassLoader.java:641)
        at java.base/jdk.internal.loader.ClassLoaders$AppClassLoader.loadClass(ClassLoaders.java:188)
        at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:521)
        at java.base/java.lang.Class.forName0(Native Method)
        at java.base/java.lang.Class.forName(Class.java:495)
        at java.base/java.lang.Class.forName(Class.java:474)
        at org.junit.internal.Classes.getClass(Classes.java:42)
        at org.junit.internal.Classes.getClass(Classes.java:27)
        at org.junit.runner.JUnitCommandLineParseResult.parseParameters(JUnitCommandLineParseResult.java:98)
        ... 4 more

    FAILURES!!!
    Tests run: 1,  Failures: 1
    ```
    c) Detail the failure-inducing input and context: The command I run in the terminal: 
      ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.java```.
                                                                                              
   2-1. A response from a TA asking a leading question or suggesting a command to try:
        Try to describe how to change the commands or program to get the expected output, there might be some useful things in the test.sh. 
                                                                                              
   2-2. Here is the screenshot showing what information the student got from trying that: 
        ![Image](screenshot1.png)
        Here is a clear description of what the bug is: For the second command in the terminal, it should be 
        ```java -cp .:lib/hamcrest-core-      1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```, which compare to the wrong          one, delete ```.java``` after the ```ListExamplesTests```. 
