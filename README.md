# Set JAVA_HOME Variable in Windows, Mac OS X, and Linux

## 1. Overview  
In this quick tutorial, we’ll take a look at how to set the JAVA_HOME variable on Windows, Mac OS X and Linux.

## 2. Windows  
### 2.1. Windows 11  
  1. Locate the directory where the JDK is installed on your system and note down the path to this directory.   
  2. Right-click on the Windows Start button and select System. 
  3. In the System window, click on Advanced System Settings on the left sidebar. 
  4. In the System Properties window (Advanced tab): 
    - Click the Environment Variables button. 
    - Under the System Variables section, find JAVA_HOME. 
    - Click Edit to modify the existing variable or New to create a new one. 
    - In the Variable Name field, enter JAVA_HOME. 
    - In the Variable Value field, enter the path to your JDK installation directory (e.g., C:\Program Files\Java\jdk1.x.x_xx). 
  5. In the System Properties window, select the Path variable under the System Variables section. Click Edit and add %JAVA_HOME%\bin to the list of paths if it’s not already there. 
  6. Click OK to apply the changes and restart your computer to ensure the changes take effect. 
