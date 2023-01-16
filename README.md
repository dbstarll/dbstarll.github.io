# 我的项目汇总

* [parent:v1.2.9](https://github.com/dbstarll/parent)
* [utils-lang:v1.0.6](https://github.com/dbstarll/utils-lang)
* [utils-spring-boot:v1.0.6](https://github.com/dbstarll/utils-spring-boot)
* [dubai:v1.0.1](https://github.com/dbstarll/dubai)
* [dubai-module-user:v1.0.2](https://github.com/dbstarll/dubai-module-user)
* [study-module:v1.0.2](https://github.com/dbstarll/study-module)

依赖关系：

```mermaid
graph TD;
    parent.base([parent:base]);

    utils-lang-->parent.base;

    utils-spring-boot-->parent.base;

    dubai([dubai])-->parent.base;
    dubai-model([dubai-model])-->dubai;
    dubai-model-service-->utils-lang;
    dubai-model-service-->dubai-model;
    dubai-module([dubai-module])-->dubai;
    dubai-module-->dubai-model-service;
    
    dubai-module-user-->dubai-module;

    study-module-->dubai-module;
    study-module-->dubai-module-user;

    certs-->utils-lang;
    utils-spring-security-->utils-lang;
    study-->utils-spring-boot;
    db-test-->utils-spring-boot;
```

