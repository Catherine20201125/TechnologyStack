# Spring核心配置文件

## application.yaml/application.yml/application.properties
在SpringBoot项目的根目录，有一个核心pom文件。文件中配置了这三种类型
https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/
网页中：4.2.3. External Application Properties
- optional:classpath:custom-config/
- optional:file:./custom-config/
解释：
file：表示项目根目录
classpath：如果是普通java工程，则表示src目录。如果是maven工程，则表示“src/main/resources”目录。

```
Spring Boot will automatically find and load application.properties and application.yaml files from the following locations when your application starts:

The classpath root

The classpath /config package

The current directory

The /config subdirectory in the current directory

Immediate child directories of the /config subdirectory

The list is ordered by precedence (with values from lower items overriding earlier ones). Documents from the loaded files are added as PropertySources to the Spring Environment.
```
优先级：
当前项目/config/下子目录 > 当前项目/config目录 > 当前项目目录 > 类路径下/config目录 > 直接在类路径下

## 运维如何动态改变我们的程序？我们要给运维留下接口



## 配置文件中可以写哪些内容？
org\springframework\boot\spring-boot-autoconfigure\2.4.4\spring-boot-autoconfigure-2.4.4.jar!\META-INF\spring.factories
applicationz.yaml或者application.properties文件中可以配置的内容：和 spring.factories 文件对应类中需要的内容一致。

1. 打开 spring.factories 文件，找到注释“# Auto Configure”，其后的文件都是以“AutoConfiguration”结尾的。随便选择一个打开，比如“HttpEncodingAutoConfiguration”。
2. 以“AutoConfiguration”结尾的文件进入类中，都有@Configuration注解（Spring核心配置类的标志）。
    - @EnableConfigurationProperties({ServerProperties.class})：开启配置文件和对应配置类的关联。
        - 进入ServerProperties类：
            - @ConfigurationProperties(prefix = "server",ignoreUnknownFields = true)：yaml文件可以往配置类中注入属性值。此注解表示配置文件和配置类关联，并设置前缀为server。
            **在配置文件中的属性上`Ctrl+鼠标左键`，进入属性所在配置类**。前提：配置文件上有“绿叶”图标，在配置文件中才会有提示，才能点击进入属性所在类。
            **application.yaml配置文件中的键 就是 @EnableConfigurationProperties元素类的属性**，为其属性设置值。
            配置文件可配置的内容： https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#common-application-properties
            **如果外部类没有此注解，找内部类！！！**
    - @ConditionalOnWebApplication(type = Type.SERVLET)：如果满足条件则配置了该注解的类生效，对应bean可以注入到Spring。如果不满足条件，则不生效，bean无法注入Spring。
    - 所有类都必须在一定条件下才能生效：


### 举例
**通过配置“debug: true”查看 哪些自动配置类 生效，哪些没有生效！！！**
在 application.yaml 中配置 “debug: true”，启动SpringBoot核心配置类，查看控制台：生成了“CONDITIONS EVALUATION REPORT”条件评估报告：
1. Positive matches: 正向匹配
2. Negative matches: 逆向匹配
3. Exclusions:  排除
4. Unconditional classes: 无条件类

Negative matches（逆向匹配）的类没有生效不可以使用。去查看其（XXXAutoConfiguration自动配置类）生效条件，自己配置（就是在pom文件中加入启动jar）。


## 思考
SpringBoot帮我们配置了什么？
我们能不能进行修改？
能修改哪些内容？
能不能扩展？

