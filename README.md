# java_source
java源码分析

## 环境搭建
1. 从master检出新分支
    ```$xslt
    分支命名规则 版本号_小版本号_analysis
    如分析jdk 1.8u60版本的源码，分支命名为 1.8_60_analysis
    master只用来做环境配置使用，不用了分析源码，分析源码从master检出新分支
    ```

2. 从本机安装的jdk找到src.zip 并复制出来
    ```$xslt
    mac 下的路径是（以jdk1.8为例）
    /Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home
    ```
3. 将复制出来的src.zip解压，解压出来的内容复制到本工程的src目录下

4. 配置jdk环境为本地源码
    ```$xslt
    Project Structure -> SDKs -> 加号 -> JDK -> 选择JDK路径(这里选择本机安装的jdk就行，注意要与分析源码的版本号一致) 
    -> Sourcepath -> 删掉里面的 src.zip -> 左下角的加号 -> 路径配置成本项目的src目录 
    -> Project -> 选择刚个新增的JDK
    ```
5. 运行src目录下的Main类中的main方法，检查环境是否没有问题

## 问题处理

1. 空间不足
    ```$xslt
    Preferences -> Build,Execution,Deployment -> Compiler -> Build process heap size (Mbytes) 配置设为 1000或更大
    ```
