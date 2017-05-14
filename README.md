# win7-anaconda-spark-安装过程

python 3.6与spark 2.1及以下版本是不兼容的！！！！掉进了一个大坑    
只有走过所有的坑，才知道哪里有坑  

**所有安装都不要安装在不包含空格的文件夹中！**  
**所有安装都不要安装在不包含空格的文件夹中！**  
**所有安装都不要安装在不包含空格的文件夹中！**    

第一步 准备所需文件  
- Anaconda3 4.2.0下载地址：https://www.continuum.io/downloads/   
- jdk 1.8下载地址：http://www.oracle.com/technetwork/java/javase/downloads/index.html  
- spark-1.6.2-bin-hadoop2.6 下载地址：http://spark.apache.org/downloads.html ，选择Pre-built for Apache Hadoop 2.6  
- hadoop-2.6.0 下载地址：https://archive.apache.org/dist/hadoop/common/  
其中spark的版本要和hadoop对应  

第二步 开始安装  
1. 安装Anaconda，我的安装目录为C:\ProgramData\  
2. 安装jdk，jdk的安装目录C:\Program_Files\Java\jdk1.8.0_131，jre的安装目录为：C:\Program_Files\Java\jre  
3. 配置java的环境变量，新建环境变量JAVA_HOME(C:\Program_Files\Java\jdk1.8.0_131),CLASSPATH(.;%JAVA_HOME%\lib;),在path中加上(%JAVA_HOME%\bin;)  
4. 将下载好的spark解压，我的解压路径为（D:\Windows_Spark\spark-2.1.1-bin-hadoop2.7），添加环境变量SPARK_HOME(D:\Windows_Spark\spark-2.1.1-bin-hadoop2.7)  
5. 将hadoop解压，路径为（D:\Windows_Spark\hadoop-2.7.3）,添加环境变量HADOOP_HOME(D:\Windows_Spark\hadoop-2.7.3)  
6. 将环境变量SPARK_HOME和HADOOP_HOME添加到环境变量path中（%SPARK_HOME%\bin;%HADOOP_HOME%\bin;）  
7. 将（D:\Windows_Spark\spark-1.6.2-bin-hadoop2.6\python）中的pyspark文件夹拷贝到（C:\Program_Files\Anaconda3\Lib\site-packages）中
8. 在cmd中运行`pip install py4j`安装py4j
9. 安装成功后，在cmd中输入pyspark，运行成功！


Windows 平台运行spark-shell 报"java.lang.NullPointerException, not found: value sqlContext" error 解决办法:  http://blog.csdn.net/u011242657/article/details/53968135
