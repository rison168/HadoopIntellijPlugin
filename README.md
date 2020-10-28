
# IntelliJ plugin for Hadoop (居于IntelliJ IDEA-2020.2版本开发)
- 1、 先到 pom.xml 文件配置合适自己版本的hadoop版本以及配置IDEA的安装路径
```
    <!--设置hadoop版本-->
    <hadoop.2.version>3.0.0-alpha2</hadoop.2.version>
    <!--设置Intellij-IDEA的安装路径-->
    <IntellijIde.dir>/home/rison/opt/apps/idea</IntellijIde.dir>
```
- 2、 先后执行一下两条命令
> mvn clean

> mvn assembly:assembly 

- 3、编译完成后 在.../target/ HadoopIntellijPlugin-1.0.zip   即为该插件的安装包，然后安装到 IntelliJ 中即可


## Intellij plugin for hadoop 插件配置和源码的相关说明
- 1、 插件的源码说明，源码组织如下：
     ![](https://github.com/fangyuzhong2016/HadoopIntellijPlugin/blob/master/img-folder/9.jpg)


        ①、core 包，为插件项目的核心包，公共组件库，包括了 通用UI界面、多线程操作、Hadoop连接设置基类、Hadoop文件系统通用操作类、插件项目设置通用类和其他工具类
        ②、fsconnection 包，Hadoop文件系统连接实现类和连接相关配置实现类
        ③、fsobject 包，文件系统对象类的实现（对于HDFS来讲就是 目录树和文件树节点的组织方式的实现）
        ④、fsbrowser包，插件的主界面实现，包括读取HDFS文件系统相关数据进行展示、文件系统对象的创建、下载、删除、上传和其他一些操作
        ⑤、globalization包，插件多语言支持类
        ⑥、options 包，插件设置类
        ⑦、mainmenu包， 插件主菜单操作类
  
  
- 2、插件配置相关说明
插件配置在.../resources/目录下，包括HadoopNavigator_en_US.properties、HadoopNavigator_zh_CN.properties  、plugin.xml。
HadoopNavigator_en_US.properties  文件为插件界面的英文语言配置
HadoopNavigator_zh_CN.properties 文件为插件界面的中文语言配置
目前插件界面的语言只支持 简体中文和英文，其他的语言，需要自行制作语言包。系统初始默认的语言为操作系统默认的语言。plugin.xml 为插件的配置文件
![](https://github.com/fangyuzhong2016/HadoopIntellijPlugin/blob/master/img-folder/10.jpg)

## 感谢原作者，原项目地址
- 1、插件源码地址： https://github.com/fangyuzhong2016/HadoopIntellijPlugin
- 2、插件相关设计： https://www.fangyuzhong.com











