JMeter Installion
JMeter installation and learning experience

Apache JMeter是一款纯java编写负载功能测试和性能测试开源工具软件。相比Loadrunner而言，JMeter小巧轻便且免费， 逐渐成为主流的性能测试工具，是每个测试人员都必须掌握的工具之一。

运行环境为Windows 10系统，JDK版本为1.8.0_201，JMeter版本为5.1.1.

JMeter安装

1.1 JDK下载与安装

    由于JMeter是基于java开发，首先需要下载安装JDK（要求JDK1.8以上）
    
1）官网下载地址：http://www.oracle.com/technetwork/java/javase/downloads/index.html

    （此链接下载超级慢建议去大公司的镜像站下载：华为：https://repo.huaweicloud.com/java/jdk/8u201-b09/）
     选择jdk-8u201-windows-i586.exe,点击下载.

3）JDK的安装与系统环境变量设置

JDK默认安装目录在C:\ProgramFiles(x86)\Java,其环境变量设置为：
     
     a. JAVA_HOME值为：C:\ProgramFiles(x86)\Java\jdk1.8.0_201
     
     b. CLASSPATH值为：.;%JAVA_HOME%\bin;
     
     c: Path值为：%JAVA_HOME%\bin;
     
4）环境变量配置完成后，检查是否可以正常使用

    windows键+R 键入cmd，在命令行中输入：java -verion

2. JMeter安装

2.1 官网下载地址：http://jmeter.apache.org/download_jmeter.cgi

 Apache tomcat 7.0 (可选项，不一定要安装。 http://tomcat.apache.org/download-70.cgi)
 
2.2 下载JMeter 5.1版本：apcache-jmeter-5.1.zip

2.3 下载完成后并解压zip包

2.4 启动JMeter

双击JMeter解压路径（apache-jmeter-5.1.1\bin） bin下面的jmeter.bat,查看页面显示，如能显示JMeter操作页面则安装成功。
