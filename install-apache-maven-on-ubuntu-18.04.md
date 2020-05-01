# Install Apache Maven on Ubuntu 18.04

## Install Apache Maven on Ubuntu 18.04

Last Updated: Fri, Nov 16, 2018 at 12:45 pm EST JavaLinux GuidesPopularServer AppsUbuntu

### Introduction <a id="Introduction"></a>

Apache Maven is a free and open source project management tool used for Java projects. You can easily manage a project's build, reporting, and documentation from a central piece of information using Apache Maven. Apache Maven provides a complete framework to automate the project's build infrastructure.

In this tutorial, you will learn how to install Apache Maven on Ubuntu 18.04.

### Prerequisites <a id="Prerequisites"></a>

* A newly deployed Vultr Ubuntu 18.04 server.
* A non-root user with sudo privileges created on your server.

### Update your server <a id="Update_your_server"></a>

First, update your system to the latest stable version:

```text
sudo apt-get update -y
sudo apt-get upgrade -y
```

### Install Java <a id="Install_Java"></a>

Maven 3.3 or greater requires JDK 1.7 or above to be installed. We will install OpenJDK, which is the default Java development and runtime in Ubuntu 18.04.

Install OpenJDK:

```text
sudo apt-get install -y default-jdk
```

Verify the Java version:

```text
java -version
```

The output will be similar to the following:

```text
openjdk version "10.0.2" 2018-07-17
OpenJDK Runtime Environment (build 10.0.2+13-Ubuntu-1ubuntu0.18.04.3)
OpenJDK 64-Bit Server VM (build 10.0.2+13-Ubuntu-1ubuntu0.18.04.3, mixed mode)
```

### Install Apache Maven <a id="Install_Apache_Maven"></a>

First, change your working directory to the `/opt/` directory:

```text
cd /opt/
```

You can download the latest stable version of Apache Maven from the [official website](https://maven.apache.org/download.cgi):

```text
sudo wget https://www-us.apache.org/dist/maven/maven-3/3.6.0/binaries/apache-maven-3.6.0-bin.tar.gz
```

Once the download has completed, extract the downloaded archive:

```text
sudo tar -xvzf apache-maven-3.6.0-bin.tar.gz
```

Next, rename the extracted directory:

```text
sudo mv apache-maven-3.6.0 maven 
```

### Setup environment variables <a id="Setup_environment_variables"></a>

Next, you will need to setup the environment variables such as `M2_HOME`, `JAVA_HOME` and `PATH`. You can do this by creating a `mavenenv.sh` file inside of the `/etc/profile.d/` directory:

```text
sudo vi /etc/profile.d/mavenenv.sh
```

Add the following lines:

```text
export JAVA_HOME=/usr/lib/jvm/default-java
export M2_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```

Save and close the file, and make it executable:

```text
sudo chmod +x /etc/profile.d/mavenenv.sh
```

Now you can load the environment variables:

```text
source /etc/profile.d/mavenenv.sh
```

### Verify installation <a id="Verify_installation"></a>

Once everything has been successfully configured, check the version of Apache Maven:

```text
mvn --version
```

You will see a similar output to the following:

```text
Apache Maven 3.6.0 (97c98ec64a1fdfee7767ce5ffb20918da4f719f3; 2018-10-24T18:41:47Z)
Maven home: /opt/maven
Java version: 10.0.2, vendor: Oracle Corporation, runtime: /usr/lib/jvm/java-11-openjdk-amd64
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "4.15.0-36-generic", arch: "amd64", family: "unix"
```

Congratulations, you have successfully installed Apache Maven on your Ubuntu 18.04 server. To get started using Maven, visit the official [Apache Maven documentation](https://maven.apache.org/guides/index.html).

