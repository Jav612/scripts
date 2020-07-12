# Install JAVA

## **Requirements**

* Download java [version jdk 8](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)

## Setup environment variable JAVA

1. Go start windows

2. View advanced system settings to windows 10

3. In “System Properties window” **click** “Environment Variables…”

   ![EV](https://javatutorial.net/wp-content/uploads/2016/08/system-properties-window.jpg)

4. Under “System variables” click the “**New**…” button and enter `JAVA_HOME` as “Variable name” and the **path** to your Java JDK directory under “Variable value” -> **Add** `JAVA_HOME` as system variable

   ![JAVA_HOME](https://javatutorial.net/wp-content/uploads/2016/08/add-java_home-as-system-variable.jpg)

5. Update System **PATH**

   -  In “Environment Variables” window under “System variables” select Path

   - Click on “**Edit**…”

   -  In “Edit environment variable” window **click** “New”

   - Type in `%JAVA_HOME%\bin`

     ![PATH](https://javatutorial.net/wp-content/uploads/2016/08/update-system-path.jpg)

6. Test your configuration

   - Open a new command prompt and type in:

     ```bash
     echo %JAVA_HOME%
     ```

   - this will print out the directory `JAVA_HOME` points to or empty line if the environment variable is not set correctly. Now type in:

     ```bash
     javac -version
     ```

   - this will print out the version of the java compiler if the Path variable is set correctly or *“javac is not recognized as an internal or external command…”* otherwise.

     ![cmdJavaHome](https://javatutorial.net/wp-content/uploads/2016/08/test-java_home-and-path.jpg)

7. Other way by command line, Run as administrator Command Prompt

   ```bash
   setx JAVA_HOME "path/to/your/java/jdk" /M
   ```

   ```bash
   # example
   setx JAVA_HOME "C:\Program Files\Java\jdk1.8.0_92"
   ```

   ![SET_JAVA_HOME](https://image.bytenota.com/data/201808/cmd-set-javahome.jpg)

   - Check `JAVA_HOME` variable 

   - Now open another **CMD** and use `echo %JAVA_HOME%` command to check whether we did it right or not.

     ![ECHO_JAVA_HOME](https://image.bytenota.com/data/201808/cmd-check-javahome-variable.jpg)