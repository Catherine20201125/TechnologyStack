

URL:

## 访问HTML页面

http://IP:tomcat端口号/部署在tomcat上的项目路径(webapps目录下)
http://localhost:8080/项目名称/html文件所在位置


## 访问Servlet
http://localhost:8080/项目名称/web.xml文件中\<url-pattern>/HelloServlet\</url-pattern>中的值

>默认web.xml

创建Servlet后，web.xml文件中自动生成\<servlet>和\<servlet-mapping>，默认情况下```<url-pattern>/HelloServlet</url-pattern>```中的值就是servlet类的名字。此时URL写法如下：
http://localhost:8080/项目名称/Servlet（java文件）名称

>修改web.xml文件

创建Servlet后，web.xml文件中自动生成\<servlet>和\<servlet-mapping>，将默认情况下```<url-pattern>/HelloServlet</url-pattern>```中的值，即servlet类的名字，修改为自己想要的名字。此时URL写法如下：
http://localhost:8080/项目名称/Servlet（对应java文件）自定义别名