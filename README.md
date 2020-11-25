# TestSystem
 BaseServlet继承于HttpServlet，主要使用反射完成servlet后端方法的分发。
操作为
1. 获取请求路径；
2. 获取方法名称；
3. 获取方法对象（哪个子类继承BaseServlet，那么代码中的this就代表该子类

与传统重写service方法相比：原来是一个功能一个Servlet，现在优化为模块一个Servlet，由BaseServlet进行方法的转发，并承担一些公共方法的
抽取；BaseServletBaseServlet 相当于是项目中所有servlet的父类，让每个模块继承BaseServlet即可；

BaseServlet让一个servlet可以同时处理多个请求，相当于在数据库中一张表对应一个Servlet，在Servlet中提供不同的方法，完成用户的请求。

