# Vee
这是一个参考Gin风格的自己写的Web框架
（1）.以net/http包为基础，通过实现ServeHTTP来接管请求，实现对请求的一些列处理
（2）.引入了上下文实例Context，从而接管请求的w和r，并简化路由的注册已经响应
（3）.以静态路由为基础，在实现静态路由的基础上，通过前缀树（Trie）来实现动态路由，诸如/hello/:name，或者/hello/*filepath
（4）.实现了动态路由以后，引入了路由组的概念，将路由分组，便于管理
（5）.在路由组的基础上，添加了中间件的功能，从而拓展框架的功能。通过上下文实例c，在处理请求路由的函数之前，先执行中间件函数来实现，主要是其中的Next（）函数起作用。
（6）.其他功能有待完善...

