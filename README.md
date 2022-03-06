# Email-Automation
*Important Note:* Test Script is configured for Hotmail Email login, As Gmail was not allowing to log in on the Automated lunch chrome instance. Please make sure to use Hotmail Login credentials.

Prerequisite: Eclipse IDE should be installed, Java installed and environment variable should be set up.

1.	Below are the Steps to Configure the data:
a)	You can locate test script at this path: /maven-shade-mj/src/test/java/ (Note: Test File name is DemoEmail.java)
b)	Parameterize (data-driven) method is created “public static Collection credentials()” created. This method will take a group of email id and passwords, And run the script for all the data sets.
c)	Add the valid credentials for the Multiple email login.
d)	“public static String predefinedString” is defined to enter String which needs to be validated as part of Email Header and Body.

2.	Below are the Steps to Run the Test via Eclipse:
a)	Run the pom.xml file to download all the dependencies libraries to run the Test.
b)	You can right-click on the pom.xml file in Eclipse and select the ‘Run As’ > ‘Maven install’ option.
c)	Right-click on the DemoEmail.java file and Run as Junit Test. Test script execution will be started. (Note: If Chrome browser is not opening please refer to the https://chromedriver.chromium.org/downloads link to check the chrome browser and driver compatibility)

3.	Below are the Steps to Run the Test via command line and within IDE:
a)	Right-click on the Project in Eclipse and select ‘Show In’ > ‘Terminal’ to lunch the terminal window.
b)	Run the below-mentioned commands in the sequence:
•	Type cd src/test/java hit enter.
•	Type javac -cp "D:\JavaCode\maven-shared-mj\Jars\junit-4.13.1.jar;D:\JavaCode\maven-shared-mj\Jars\selenium-java-4.0.0-alpha-6.jar;D:\JavaCode\maven-shared-mj\Jars\selenium-server-4.0.0-alpha-6.jar;." DemoEmail.java hit enter.
•	Type java -cp "D:\JavaCode\maven-shared-mj\Jars\junit-4.13.1.jar;D:\JavaCode\maven-shared-mj\Jars\selenium-java-4.0.0-alpha-6.jar;D:\JavaCode\maven-shared-mj\Jars\selenium-server-4.0.0-alpha-6.jar;D:\JavaCode\maven-shared-mj\Jars\hamcrest-2.2.jar;." org.junit.runner.JUnitCore DemoEmail hit enter.
c)	Test execution will start.
