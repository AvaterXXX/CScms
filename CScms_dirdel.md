# CSCMS_dirdel
-----

### Code analysis
Vulnerability code is located `\plugins\sys\admin\Plugins.php` 286 to 299 lines
![](https://github.com/AvaterXXX/CScms/blob/master/images/%E4%BB%BB%E6%84%8F%E6%96%87%E4%BB%B6%E5%88%A0%E9%99%A41.png)

You can see made some simple judgments on the submitted dir, and then directly bring in the statement to delete.

### Vulnerability display
![](https://github.com/AvaterXXX/CScms/blob/master/images/%E4%BB%BB%E6%84%8F%E6%96%87%E4%BB%B6%E5%88%A0%E9%99%A42.png)

Create a directory 111
![](https://github.com/AvaterXXX/CScms/blob/master/images/%E4%BB%BB%E6%84%8F%E6%96%87%E4%BB%B6%E5%88%A0%E9%99%A43.png)

post `dir=..\\111` ,success delect.
