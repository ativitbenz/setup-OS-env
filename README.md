# Set JAVA_HOME Variable in Windows, Mac OS X, and Linux
Original Doc: `https://www.baeldung.com/java-home-on-windows-mac-os-x-linux#3-global-setting`

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

### 2.2. Windows 8 and 10
  1. Open Search and type advanced system settings.
  2. In the shown options, select the View advanced system settings link.
  3. Under the Advanced tab, click Environment Variables.
  4. In the System variables section, click New (or User variables for single user setting).
  5. Set JAVA_HOME as the Variable name and the path to the JDK installation as the Variable value and click OK.
  6. Click OK and click Apply to apply the changes.

### 2.3. Windows 7
  1. On the Desktop, right-click My Computer and select Properties.
  2. Under the Advanced tab, click Environment Variables.
  3. In the System variables section, click New (or User variables for single user setting).
  4. Set JAVA_HOME as the Variable name and the path to the JDK installation as the Variable value and click OK.
  5. Click OK and click Apply to apply the changes.
     
Open Command Prompt and check the value of the JAVA_HOME variable:  
```
echo %JAVA_HOME%
```
The result should be the path to the JDK installation:
`C:\Program Files\Java\jdk1.8.0_111`

## 3. MacOS
### 3.1. Single User – Mac OS X 10.5 or Newer
From OS X 10.5, Apple introduced a command line tool (/usr/libexec/java_home) that dynamically finds the top Java version specified in Java Preferences for the current user.  
Open ~/.bash_profile in any text editor and add the following:  
```
export JAVA_HOME=$(/usr/libexec/java_home)
```
Save and close the file.  
Open a Terminal and run the source command to apply the changes:  
```
source ~/.bash_profile
```
Now we can check the value of the JAVA_HOME variable:  
```
echo $JAVA_HOME
```
The result should be the path to the JDK installation:
`/Library/Java/JavaVirtualMachines/jdk1.8.0_111.jdk/Contents/Home`

### 3.2. Single User – Mac OS X Older Versions
For older versions of OS X, we have to set the exact path to the JDK installation. 
Open ~/.bash_profile in any editor and add the following: 
```
export JAVA_HOME=/path/to/java_installation
```
Save and close the file.  
Open a Terminal and run the source command to apply the changes:  
```
source ~/.bash_profile
```
Now we can check the value of the JAVA_HOME variable:  
```
echo $JAVA_HOME
```
The result should be the path to the JDK installation:
`/Library/Java/JavaVirtualMachines/jdk1.8.0_111.jdk/Contents/Home`

### 3.3. Global Setting  
To set JAVA_HOME globally for all users, the steps are the same as for a single user, but we use the file /etc/profile.


## 4. Linux
We’re going to manipulate the PATH here, of course, so here are the detailed instructions on how to do it.

### 4.1. Single User
To set JAVA_HOME in Linux for a single user, we can use /etc/profile or /etc/environment (preferred for system-wide setting) or ~/.bashrc (user-specific setting). 
Open ~/.bashrc in any text editor and add the following: 
``` 
export JAVA_HOME=/path/to/java_installation
```
Save and close the file. 
Run the source command to load the variable: 
``` 
source ~/.bashrc
```
Now we can check the value of the JAVA_HOME variable:
```
echo $JAVA_HOME
```
The result should be the path to the JDK installation:
`/usr/lib/jvm/java-8-oracle`

### 4.2. Global Setting
To set JAVA_HOME in Linux for all users, we can use /etc/profile or /etc/environment (preferred). 
Open /etc/environment in any text editor and add the following: 
```
JAVA_HOME=/path/to/java_installation
```
Please note that /etc/environment is not a script but a list of assignment expressions (that is why export is not used). This file is read at the time of login. 
To set JAVA_HOME using /etc/profile, here’s what we’ll add to the file: 
```
export JAVA_HOME=/path/to/java_installation
```
Run the source command to load the variable:
```
source /etc/profile
```
Now we can check the value of the JAVA_HOME variable:
```
echo $JAVA_HOME
```
The result should be the path to the JDK installation:
`/usr/lib/jvm/java-8-oracle`

## 5. Conclusion
n this article, we covered ways to set the JAVA_HOME environment variable on Windows, Mac OS X and Linux.
