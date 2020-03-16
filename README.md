# Mybatis-Reverse
Mybatis逆向工程，可以针对多表自动生成Mybatis执行所需要的java代码，如Mapper，poyo等

# 使用说明
+ 编辑generatorConfig.xml：
  <jdbcConnection driverClass="com.mysql.cj.jdbc.Driver"
                        connectionURL="jdbc:mysql://localhost:3306/beehive?characterEncoding=utf-8&amp;serverTimezone=UTC&amp;useSSL=false"
                        userId="root"
                        password="root">
        </jdbcConnection>
 修改jdbcConnection里的URL、userId和password
 
 最后加上
  <table tableName="要逆向工程的表名"></table>
然后run 将生成的mapper，pojo等java文件复制到你项目的文件夹里即可

# 小bug
每次生成完然后复制到你项目文件夹以后 如果想第二次生成的话 需要删除第一次生成的文件夹 否则会重复
