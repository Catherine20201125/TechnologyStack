

food: Pizza 

# Learning about Typora 



### 远程下载jar包到本地库

命令：

`mvn dependency:get -DRremoteRepositories=url -DgroupId=groupId -DartifactId=artifactId -Dversion=version`

eg.

`mvn dependency:get -DremoteRepositories=https://mvnrepository.com/artifact/org.springframework/spring-core -DgroupId=org.springframework -DartifactId=spring-core -Dverson=5.2.13.RELEASE`

```
<!-- https://mvnrepository.com/artifact/org.springframework/spring-core -->
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-core</artifactId>
    <version>5.2.13.RELEASE</version>
</dependency>
```



![image-20210326123508496](C:\Users\10052\AppData\Roaming\Typora\typora-user-images\image-20210326123508496.png)



依赖管理，项目构建。

依赖管理：对jar包之间依赖关系的管理。

项目构建：项目目录 和 构建（清除、编译、测试、打包、安装、发布）流程标准化。

### Maven声明周期

清理生命周期：clean。清空target目录及其下面的文件。

默认生命周期：compile -> test -> package -> install -> deploy。

1. compile：将src目录下的文件编译，并在target目录生成class文件等。
2. test：对

站点声明周期：site。生成javadoc文档。

在同一套声明周期内，执行一个命令，默认执行前面的命令。



### 网络问题导致本地仓库下载包出错

![image-20210326143105557](C:\Users\10052\AppData\Roaming\Typora\typora-user-images\image-20210326143105557.png)



<h1>{{ page.name }}</h1>



<h1>{{ page.food }}</h1>









<center>居中<center>

<keyboard>Ctrl<keyboard>

```java
//注释部分
public class HelloWorld{
    private int id;
    private String name;
    
}
```



```c

```



```javascript
function 
```



```sql
select * from lduser where 
```



```(~~~)
我是普通文本
```



```
普通文本苹果
```







- [ ] 苹果



|      |      |      |
| ---- | ---- | ---- |
|      |      |      |
|      |      |      |
|      |      |      |
|      |      |      |



![]()



Typora[^1]



[^1]: 注解尝试



\[\]





即使[^footnote]

[^footnote]: hero;







[]

{}

 {}





[^footnote]: 





<iframe height='265' scrolling='no' title='Fancy Animated SVG Menu' src='http://codepen.io/jeangontijo/embed/OxVywj/?height=265&theme-id=0&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'></iframe>

<video src="xxx.mp4" />





