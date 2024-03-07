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
