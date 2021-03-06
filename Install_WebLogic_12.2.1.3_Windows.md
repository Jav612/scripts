# Install WebLogic 12.2.1.3 to Windows

## **Requirements**

* Download java [version jdk 8](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)
* Download Weblogic [version 12.2.1.3](https://www.oracle.com/middleware/technologies/weblogic-server-installers-downloads.html)

## Install

* Create folders to C:\

  ```bash
  > mkdir fmw_12.2.1.3
  > mkdir fmw_12.2.1.3_HOME
  > mkdir WL12.2.1.3_Domains
  ```

* **OR** 

  ```bash
  md fmw_12.2.1.3 fmw_12.2.1.3_HOME WL12.2.1.3_Domains
  ```

* Extract zip download `fmw_12.2.1.3.0_wls_quick_Disk1_1of1.zip` move folder `fmw_12.2.1.3`

* Run as administrator Command Prompt

  ```bash
  > cd C:\fmw12.2.1.3
  > java -jar fmw_12.2.1.3.0_wls_quick.jar ORACLE_HOME=C:\fmw_12.2.1.3_HOME
      Starting check : CheckJDKVersion
      Expected result: 1.8.0_131
      Actual Result: 1.8.0_251
      Check complete. The overall result of this check is: Passed
      CheckJDKVersion Check: Success.
  
      Validations are enabled for this session.
      Verifying data
      Copying Files
      Percent Complete : 10
      Percent Complete : 20
      Percent Complete : 30
      Percent Complete : 40
      Percent Complete : 50
      Percent Complete : 60
      Percent Complete : 70
      Percent Complete : 80
      Percent Complete : 90
      Percent Complete : 100
      
      The installation of Oracle Fusion Middleware 12c WebLogic and Coherence Developer 12.2.1.3.0 completed successfully.
  
  ```

  ```bash
  > cd \fmw_12.2.1.3_HOME\oracle_common\common\bin
  > config.cmd
  ```

* Create a new domains

  * Set *Domain Location* `C:\Weblogic12.2.1.3_Domains\{Name Domain}` **click** `Next >`
  * Create Domain Using Product Templates:
  * Basic Weblogic Server Domain - 12.2.1.3.0 [wlserver] * **click** `Next >`
  * Set credentials **click** `Next >`
  * Choose Development 
  * Choose Jdk **click** `Next >`
  * Choose Administration Server
  * Choose Node Manager **click** `Next >`
  * add name -> Server Name
  * add listen address
  * add listen port **click** `Next >`
  * **Node Manager Type** choose -> Per Domain Default Location
  * Set Node Manager Credentials `Next >`
  * **click** button `create`
  * ![createDomain](https://miro.medium.com/max/1592/1*seVquFWk8ld_LCS3h6SZig.png)
  * Finish 

## Run Weblogic

- Run Command Prompt

  ```bash
  > cd C:\WL12.2.1.3_Domains
  > startWeblogic.cmd
  ```

- go to browser -> http://127.0.0.1:7001/console

## Error Solved

[Jdk invalid or JRE invalid](https://www.codejava.net/ides/eclipse/how-to-run-eclipse-under-different-version-of-jdk-or-jre), We recommend that you remove unused JDK installations. Remove `path` that overwrites the `environment variable` **JAVA_HOME** for example java installations that deprive other products.

```tex
C:\Program Files\Common Files\Oracle\Java\javapath;
```

## Sources 

* [Switch JDK Version](https://stackoverflow.com/questions/47469310/switch-jdk-version-in-windows-10-cmd)
* [Oracle Weblogic Server 12.2.1.3 Installation from Dev Zip Archive Windows 10 using Oracle JDK 8](https://www.youtube.com/watch?v=jKdVOV9ZlVk) 
* [Setting JAVA_HOME](https://confluence.atlassian.com/doc/setting-the-java_home-variable-in-windows-8895.html)
* [Set JAVA_HOME WINDOWS 10](https://javatutorial.net/set-java-home-windows-10)
* [Windows cmd set JAVA_HOME](https://bytenota.com/windows-cmd-set-java_home-variable-using-command-prompt/)
* [Create Folder CMD](https://www.tech-recipes.com/rx/57409/create-folder-using-cmd-windows/)