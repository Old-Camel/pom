### 1.以下内容为textbook插件的依赖文件总结
###2.对website插件多余以及重复的依赖进行了处理
###3.本插件pom总结仅包含基础的增删改查功能
###4.如需要添加其它jar包,自行在pom文件中添加所需的依赖包,可参考pom文件总结中的内容
****
###下图为项目整体结构

![](/assets/textbook整体结构图.jpg)
####其中textbook为父工程(pom包),textbook-api模块(jar包)放javabean,service接口,mapper接口,工具类,textbook-impl模块(war包)放service实现类,textbook-web模块(war包)放controller+静态资源
