## PowerMTA目录穿越

Configuration页面中可查看pmta部分文件

![image-20251221172039507](PowerMTA目录穿越.assets/image-20251221172039507.png) 

抓包后查看请求路径，发现是绝对路径，且可以使用../进行目录穿越

![image-20251221172047718](PowerMTA目录穿越.assets/image-20251221172047718.png) 

不过访问其他目录需要root用户权限

在config中修改为root用户权限(yes)

![image-20251221172331514](PowerMTA目录穿越.assets/image-20251221172331514.png) 

待pmta服务重启后可通过root用户权限任意读取文件