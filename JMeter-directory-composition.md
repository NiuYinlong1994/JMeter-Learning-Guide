JMeter directory composition

Jmeter的Home目录下包含bin、docs、extras等文件夹，需要重点了解的是bin、lib和docs目录。

$ Bin目录下存放的是可执行的程序、配置文件和日志文件

    Jmeter.bat （windows的启动文件）
      
       #jmeter压测时提示内存溢出时，通常情况下需要修改此文件中的JVM参数。
          
           set HEAP = -Xms512m -Xmx512m
           
           set PERM = -XX:PermSize = 128m
           
       XX:MaxPermSize = 128m
           
       注意：
        
       # HEAP和PermSize之和不要超过物理内存的50%；
       
       # 32位的JDK版本只支持1.5G左右内存。
       
     Jmeter-server.bat （windows分布式测试要用到的服务器）
     
        # 这个是Jmeter联机负载测试的组件
        
        # 如果需要做联机负载测试，需要在负载机器上启动该程序。
        
     Jmeter.properties （系统的配置文件）
     
        # jmeter.properties是JMeter的系统配置文件，在这里可以针对jmeter做各种配置操作。
        
        # 比如说配置远程负载机等。
           
            remote_hosts = 127.0.0.1
            
            remote_hosts = localhost:1099,172.168.1.13:1099,172.168.0.16:1099
            
            # RMI port to be used by the server(must start rmiregistry withsame port)
            
              server_port = 1099
              
 $ Lib目录下包含ext、junit目录及各种jar包
 
     # lib目录下的jar包是在脚本过着jmeter运行时所需要的jar包。如我们需要使用JDBC测试数据库时，就需要将对应的jdbc驱动的jar包放入lib目录。
     
     # ext目录下存放的是jmeter核心jar包，也可以存放自定义组件和插件的jar包。
     
     # junit目录是存放JUnit测试脚本。
     
     # 用户扩展所依赖的包，应该直接放在lib目录下，而非lib/ext目录下。
     
 $ Docs目录下存放的是API文档、默认的样式文件及UI图片等。
 
 $ extras目录：扩展插件目录，目录下的文件提供了对ant的支持。
 
     extras目录下的文件提供了对构建工具Ant的支持，可以使用Ant来实现测试自动化，例如批量简本执行，产生HTML格式的报表。测试运行时，可以把测试数据记录下来，Jmeter会自动生成一个.jtl文件。将该文件放到extras目录下，运行"ant ——Dtest=文件名 report"，就可以生成测试统计报表。
 
 $ printable_docs: usermanual子目录下是jmeter用户手册，尤其是component_reference.html是最常用的核心元件帮助手册。
 
 
                           参考于：http://www.cnblogs.com/wanghonggang-521/p/7373399.html
 
