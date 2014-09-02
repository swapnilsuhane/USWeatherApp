USWeatherApp
============

Web Application for displaying United States City's Temperature(F) Using ZipCode

Please follow below steps to setup and deploy the web application.
*These instruction are for Windows OS. (ex. MS Windows 7)

# Environmental Setup- 
   (Ignore if you already have all java setup on your machine)
   Before starting build/deploy of application make sure you have below setup on your machine.

-   JDK 1.7 or above: 
    If you don't have Jave Development Kit installed on your machine please use below link to install. 
    http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html

-   Eclipse IDE: 
    Install any of the eclipse versions from below link.
    http://www.eclipse.org/downloads/packages/eclipse-standard-44/lunar

-   Apache Tomcat Server 7:
    Windows -> Show View -> Servers to view server tab
    Click on create a server link
    Select Apache - Tomcat 7.0 or above server and click Next
    Select Tomcat directory ex. 'D:\Java\Tomcat 7\apache-tomcat-7.0.53' (If don't have please install from apache site)
    Select JRE as jdk1.7.0_xx and click Finish

-   Eclipse Installed JRE: 
    Go to below eclipse path and setup JDK as Installed JRE in eclipse.
    Windows -> Preferences -> Java -> Installed JREs -> Add -> Standard VM -> Directory
    select JDK installed path ex. C:\Program Files\Java\jdk1.7.0_67
    Now select jdk1.7.0_xx as Installed JRE.

Now we have all setup so we are ready to Deploy/ Test/ Run.

# Import application using WeatherApp.war
-   Import the project using was with below eclipse path.
    File -> Import -> War File -> Browse
-   Now select the war file path in your machine. (save local if you haven't)
-   Click finish (no need to select jars)

# Running application on tomcat server
-   Right click on WeatherApp project in the eclipse and goto Run As -> Run on Server
-   Select existing tomcat server that we created above and click Finish.
-   Now we are good to start tomcat server. Right click on server and start it.
-   If you see any error while starting tomcat server please check the console logs and check you have all environmental setup on eclipse. 
-   Check the Tomcat is running with URL: http://localhost:8080/

# Check the Weather Application URL: http://localhost:8080/WeatherApp/
-    You will see the web page to enter ZipCode (valid 5 length + numeric)
-    Upon clicking Submit same page will display you City, State, Temperature in Fahrenheit.
-    If you don't enter any zipcode you will get a validation message 'ZipCode is required'
-    If you enter any invalid zipcode (ex. 100) you will get validation message 'Invalid ZipCode Format'
-    If you enter any valid zipcode that does not exist (ex. 10000) you will get a javascript validation message 'ZipCode Not Found !!'

# Importing Existing Maven Project
-   Import the project using below eclipse path.
    File -> Import -> Existing Maven Projects -> Next -> Browse
-   Now select the maven project folder. It will find the pom.xml
-   Select the pom.xml and click Next
-   Select all the jars files in the link and click Finish.
-   You have successfully imported Maven 'WeatherApp' project into eclipse.

# Build/Test Maven Project
-   Right click on WeatherApp project in the eclipse and goto Run As -> Maven build
-   Goals- clean install
-   Click Run. It will build the maven project along with running all Junit Tests.
-   You should get 'BUILD SUCCESS' if no errors reported.
-   Also check the JUnit results ex.
Results :
Tests run: 15, Failures: 0, Errors: 0, Skipped: 0

# Running Junit Test on Eclipse
-   Right click on WeatherApp project in the eclipse and goto Run As -> Junit Test
-   In the Junit tab you will see Green bar along with test counts if all tests are successful.

# Running Maven application on Tomcat Server
-   Before running application on server add maven dependency in eclipse else you will get error.
-   Right click on WeatherApp project in the eclipse -> Properties -> Deployment Assembly -> Add -> Java Build Path Entries -> Select Maven Dependencies then click Ok/Finish. It will add dependent jar path in eclipse. 
-   Right click on WeatherApp project in the eclipse and goto Run As -> Run on Server
-   Select existing tomcat server that we created above and click Finish.
-   Now we are good to start tomcat server. Right click on server and start it.
-   If you see any error while starting tomcat server please check the console logs and check you have all environmental setup on eclipse. 
-   Check the Tomcat is running with URL: http://localhost:8080/WeatherApp/





