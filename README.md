# 我的项目汇总

* [parent:v1.2.9](https://github.com/dbstarll/parent)
* [utils-lang:v1.0.6](https://github.com/dbstarll/utils-lang)
* [utils-spring-boot:v1.0.6](https://github.com/dbstarll/utils-spring-boot)
* [dubai:v1.0.1](https://github.com/dbstarll/dubai)
* [dubai-module-user:v1.0.2](https://github.com/dbstarll/dubai-module-user)
* [study-module:v1.0.2](https://github.com/dbstarll/study-module)
* [study-boot:v1.0.2-SNAPSHOT](https://github.com/dbstarll/study-boot)

依赖关系：

```mermaid
graph TD;
    parent.base([parent:base]);
    parent.boot([parent:boot])--->parent.base;

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

    study-boot-->parent.boot;
    study-boot-->study-module;
    study-boot-->utils-net-api;
    study-boot-->utils-json;
    study-boot-->utils-spring-boot;
    study-boot-->utils-spring-security;

    certs-->utils-lang;
    utils-spring-security-->utils-lang;
```

