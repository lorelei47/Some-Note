# 一些问题记录

## 关于AJAX/GET请求乱码的问题
>> AJAX的GET请求参数中若存在中文等非“ASCII字符”时，服务端在解析请求参数时，如果仅通过request.getParameter(参数key)方法获取参数值，而不进行相关处理，获得值中就会出现乱码的问题。
>> [原文](https://blog.csdn.net/pursuer211/article/details/42425437)
