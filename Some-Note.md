# 一些问题记录

### 1、关于AJAX/GET请求和window.location.href传中文参数乱码的问题
>> 1).AJAX的GET请求参数中若存在中文等非“ASCII字符”时，服务端在解析请求参数时，如果仅通过request.getParameter(参数key)方法获取参数值，而不进行相关处理，获得值中就会出现乱码的问题。
>> [原文](https://blog.csdn.net/pursuer211/article/details/42425437)
>> 2).window.location.href传中文参数,查询乱码问题 则需要对要传的参数进行二次编码
>> [原文](https://blog.csdn.net/hllll_huang/article/details/53709314)

### 2、关于执行sql查询取其返回的数据时，如果查询结果只有一条记录时，会默认为指定类型，而非数组。
>> 情况描述：在执行sql查询取其返回的数据时出现的；用的是数组来取它的Result，在一般情况下都正常的；但在某些地方就报异常！  

>> 出现原因：sql语句执行的查询结果只有一列时就会出现该问题！当有多个列时用数组取没有问题，如果只有一列会默认为string或者其他类型！

### 3、关于java中的static说明。
>> 通俗结论：方便在没有创建对象的情况下来进行调用（方法/变量）。

>> 常用说明：java中用static修饰类中的方法和成员可以直接使用类名.成员（如：Integer.valueOf()）方式调用，无需new类的一个对象再调用。一般在工具类中使用。

### 4、在react中import组件时使用的相对路径与绝对路径。
>> 绝对路径：从src/..开始。

>> 相对路径：../../开始。（如果需要引入的文件在当前文件的父级文件夹同级或者再往上，则需多加../，具体加多少加到他不报错为止）

### 5、ORACLE的Copy命令和create table,insert into的比较
>> 讲解了copy from命令的使用说明，以及与create table和insert into进行效率的对比。
>> [原文](https://blog.csdn.net/cscscscsc/article/details/55260065)

### 6、限制同一IP一段时间内多次请求服务器
>> 获取IP，并将该ip下请求的次数记录在session中。但如果请求端清除过cookies，则此方法将无效。
>> [代码参考](https://github.com/lorelei47/Some-Note/blob/master/LimitIpRequest)
