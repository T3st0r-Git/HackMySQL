# python-promoting-privileges
1.自动导出mof文件，

2.自动判断mysql版本，根据版本不同导出UDF的DLL到不同目录，UDF提权

3.导出LPK.dll文件，劫持系统目录提权

4.写启动项有问题，已经注释掉 

UDf will make the user 'guest' active and add to admin with the pass 789456123+abc
The sql of Dumping AddUser And AddToAdmin MOF File has queried OK.
Press shift 5 times then press 1,2 at the same time to start the lpk UI,pass:binghesec
Mof and LPK will add  users named BingheSec$/admin$ with password: 789456123+abc
Mof file only fit for windows2003 , please test it byourself!
