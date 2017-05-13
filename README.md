# win7-anaconda-spark-安装过程

所有安装都不要安装在不包含空格的文件夹中！  
所有安装都不要安装在不包含空格的文件夹中！  
所有安装都不要安装在不包含空格的文件夹中！  

Anaconda 4.3下载地址：https://www.continuum.io/downloads/  
jdk 1.8下载地址：http://www.oracle.com/technetwork/java/javase/downloads/index.html  
spark 2.11下载地址：http://spark.apache.org/downloads.html  
hadoop 2.73下载地址：http://www.apache.org/dyn/closer.cgi/hadoop/common/hadoop-2.7.3/hadoop-2.7.3.tar.gz  
其中spark的版本要和hadoop对应

以上文件准备好以后，准备开始安装  
1.安装Anaconda，我的安装目录为C:\ProgramData\
2.安装jdk，jdk的安装目录C:\Program_Files\Java\jdk1.8.0_131，jre的安装目录为：C:\Program_Files\Java\jre  
3.配置java的环境变量，新建环境变量JAVA_HOME(C:\Program_Files\Java\jdk1.8.0_131),CLASSPATH(.;%JAVA_HOME%\lib;),在path中加上(%JAVA_HOME%\bin;)  
4.将下载好的spark解压，我的解压路径为（D:\Windows_Spark\spark-2.1.1-bin-hadoop2.7），添加环境变量SPARK_HOME(D:\Windows_Spark\spark-2.1.1-bin-hadoop2.7)  
5.将hadoop解压，路径为（D:\Windows_Spark\hadoop-2.7.3）,添加环境变量HADOOP_HOME(D:\Windows_Spark\hadoop-2.7.3)  
6.将环境变量SPARK_HOME和HADOOP_HOME添加到环境变量path中（%SPARK_HOME%\bin;%HADOOP_HOME%\bin;）  
7.在命令行窗口中输入pyspark，成功！
