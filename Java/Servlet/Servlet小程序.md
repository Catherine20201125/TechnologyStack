
Servlet是Web服务器端小程序，用来接受请求和返回响应，一般不会太复杂。java文件。
提交form表单会将表单中的内容提交到服务器，第一个与页面交互的就是Servlet服务端小程序；
form表单中的action属性要写**服务器地址**，写Servlet所在位置，比如：/工程名/Servlet名称。
提交表单时，Servlet程序执行。提交表单指 
```<input type="submit" value="submit"/>``` 点击<input type="submit" value="submit"/>按钮； 
```<input type="button" value="按钮"/>``` 点击<input type="submit" value="按钮"/>按钮；
通过调用JS程序，在JS程序中提交表单```function subForm(){ $("#Form").submit();}```：在以上的各种**按钮**（type="submit/button/image"）中设置onclick点击事件，调用JS方法。

或者，```<a href="/工程名/Servlet名称">```超链接，不需要form表单，也可以链接到Servlet。

表单数据的提交通过HTTP协议，会将数据写成键值对。在Servlet中提供了request和response对象，可以获取关于请求（请求行、请求头、请求体）和响应（响应行、响应头、响应体）的相关内容。


