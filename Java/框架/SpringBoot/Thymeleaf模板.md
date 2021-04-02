#

## 模板引擎
和jsp作用类似。

## 导入Thymeleaf的starter
Thymeleaf官网：https://www.thymeleaf.org/download.html
GitHub：https://github.com/thymeleaf/thymeleaf
Spring官网：https://docs.spring.io/spring-boot/docs/2.4.4/reference/html/using-spring-boot.html#using-boot-starter（不知道这个版本为什么没有pom）
https://docs.spring.io/spring-boot/docs/2.2.13.RELEASE/reference/html/using-spring-boot.html#using-boot-starter

```
<dependency>
    <groupId>org.thymeleaf</groupId>
    <artifactId>thymeleaf-spring5</artifactId>
</dependency>
<dependency>
    <groupId>org.thymeleaf.extras</groupId>
    <artifactId>thymeleaf-extras-java8time</artifactId>
</dependency>
```

## 导入的starter都有一个配置类对应

org.springframework.boot.autoconfigure.thymeleaf.ThymeleafProperties配置类：
配置类中默认配置了前缀后缀，SpringMVC中视图解析器也有前缀和后缀的配置。

```
public class ThymeleafProperties {
    private static final Charset DEFAULT_ENCODING;
    public static final String DEFAULT_PREFIX = "classpath:/templates/";
    public static final String DEFAULT_SUFFIX = ".html";
    private boolean checkTemplate = true;
    private boolean checkTemplateLocation = true;
    private String prefix = "classpath:/templates/";
    private String suffix = ".html";
    private String mode = "HTML";

```

## 放在src\main\resources\templates\下的文件必须通过Controller层访问，不能直接访问。相当于java web中的WEB-INF。

Controller层接口编写：
```
@Controller
public class IndexController {
    @RequestMapping("/test")
    public String test(){
        model.add
        return "test";
    }

}
```

src\main\resources\templates\index.html
页面访问：http://localhost:8080/ (后面不要写index.html，否则访问不到！！！)

## 语法
学习网址：
https://www.thymeleaf.org/doc/tutorials/3.0/usingthymeleaf.html#using-texts

### 
