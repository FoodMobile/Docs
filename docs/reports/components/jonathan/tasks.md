#### Jenkins and REST api

![restAPI](../../images/jonathan/restAPI.png)

For my part, I set up continuous integration and our servers. Our hope is that by using continuous integration, we can spend less time working with tools and more time working on the project itself. In addition to setting up the continuous integration on the server, I also started the REST api documentation. Finishing the REST api documentation does 3 things: It gives us a way to know how many things still need to be created in the backend REST server. It gives us discrete things to test so that we know how much of the API is working with unit tests. Finally, it gives the people whose primary responsibility is the front end application, the ability to begin testing with dummy responses. Testing with dummy responses assists with blackbox testing and development on the front end mobile application.

![jenkins](../../images/jonathan/jenkins.png)

#### Obstacle 1: Jenkins is more suited for Tomcat and Glassfish

Our original application was configured to be a Spring Boot Jetty project, which makes use of a bundled Jetty server in a jar. This does not work well for automated redeployment on servers, especially using Jenkins. So I had to convert our Spring Boot Jetty project into a Spring Boot Java Servlets project. After doing so I was able to install our application on Tomcat.

#### Obstacle 2: Virtual machine configuration was messed up

The virtual machine had 2 problems with it: Tomcat had a lot of configuration to do to allow remote connections, and the default JDK retrieved through APT has a bug in it’s certificate chain. In order to properly configure Tomcat, I had to go through some XML files and disable filtering for external IP addresses, and I had to create accounts with the correct permissions. This involved editing a tomcat-users.xml file and finding the correct permissions to give to both users and the automated Jenkins user account. Fixing the Java toolchain was a bit of a pain. In order to fix the Java toolchain, I had to first remove the existing cacerts file containing existing certificates. Then I had to configure a .properties file and switch from PKCS 12 to the JKS certificate style. After configuring the .properties file, I had to run a command to redownload all the certificates from a trusted certificate authority, via a build in command in the OpenJDK installation.

#### Obstacle 3: Jenkins setup

This was the least hard of the 3 obstacles, but still took quite a bit of time. Configuring Jenkins to work with our Tomcat server kept giving strange errors, and that was about the time I figured out I had wrong permissions on Tomcat. I must’ve also missed a checkbox because after attempting to reconfigure the job in Jenkins, it started to work again.