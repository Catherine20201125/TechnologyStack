#

## 静态资源导入
将静态资源等放在：src\main\resources\static

### SpringMVC自动配置类分析：
```
protected void addResourceHandlers(ResourceHandlerRegistry registry) {
    super.addResourceHandlers(registry);
    if (!this.resourceProperties.isAddMappings()) {
        logger.debug("Default resource handling disabled");
    } else {
        ServletContext servletContext = this.getServletContext();
        this.addResourceHandler(registry, "/webjars/**", "classpath:/META-INF/resources/webjars/");
        this.addResourceHandler(registry, this.mvcProperties.getStaticPathPattern(), (registration) -> {
            registration.addResourceLocations(this.resourceProperties.getStaticLocations());
            if (servletContext != null) {
                registration.addResourceLocations(new Resource[]{new ServletContextResource(servletContext, "/")});
            }

        });
    }
}
```

1. 什么是 webjars？
    场景：以前导入JQuery需要手动引入包，但是SpringBoot中以Maven的方式引入。
    打开webjars官网：https://www.webjars.org/ 。此网站提供了Maven坐标。

    webjars其实就是web需要的静态文件、js文件等封装成了一个jar包，可以使用Maven引入了。

2. 页面访问的时候怎么写URL？
   以上代码中“ /webjars/** ” 映射到 “ classpath:/META-INF/resources/webjars/ ”。此处只映射到了webjars/这一层，需要将之后的目录和文件名称在URL中补齐。
   JQuery为例：org\webjars\jquery\3.6.0\jquery-3.6.0.jar!\META-INF\resources\webjars\jquery\3.6.0\jquery.js
   http://IP:Port/webjars/jquery/3.6.0/jquery.js

### 静态资源导入方式二
1. WebMvcProperties类：this.staticPathPattern = "/**";
2. WebProperties类中：
```
private static final String[] CLASSPATH_RESOURCE_LOCATIONS = new String[]{"classpath:/META-INF/resources/", "classpath:/resources/", "classpath:/static/", "classpath:/public/"};
```
在类路径（/src/main/resources/）下新建文件夹：
- resources/：/src/main/resources/resources/
- public/：/src/main/resources/public/
页面访问：**http://localhost:8080/文件名.后缀 ** 就可以访问到这些文件夹下的文件