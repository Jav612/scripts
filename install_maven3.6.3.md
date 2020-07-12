# Install Maven to Windows 10

### Requirements 

* [Java](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html) [download jdk-8u251](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html#license-lightbox)
* [Apache Maven](https://maven.apache.org/download.cgi) [download apache-maven-3.6.3-bin.zip](https://downloads.apache.org/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.zip)

### Install

* Extract zip apache-maven-3.6.3-bin.zip to the path `C:\

* Go start & find 

* Type editing the system environment system

* Click `Environment Variables...`

* In system variables **click** `New...`

* Configure `MAVEN_HOME` and `M2_HOME` environment variables with the path `C:\apache-maven-3.6.3`

* Add a new system variable to the path, `%MAVEN_HOME%\bin`

* reboot the operating system

* Open CMD or terminal, 

  ```bash
  C:\Users\Maven>mvn -version
  Apache Maven 3.6.3 (cecedd343002696d0abb50b32b541b8a6ba2883f)
  Maven home: C:\apache-maven-3.6.3\bin\..
  Java version: 1.8.0_251, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk1.8.0_251\jre
  Default locale: en_US, platform encoding: Cp1252
  OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
  C:\Users\Maven>
  ```