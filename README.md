# 我的项目汇总

* [parent](https://github.com/dbstarll/parent)
* [utils-lang](https://github.com/dbstarll/utils-lang)
* [utils-spring-boot](https://github.com/dbstarll/utils-spring-boot)
* [dubai](https://github.com/dbstarll/dubai)
* [dubai-module-user](https://github.com/dbstarll/dubai-module-user)

依赖关系：

```mermaid
graph TD;
    utils-lang-->parent.base;
    certs-->utils-lang;
    utils-spring-security-->utils-lang;

    utils-spring-boot-->parent.base;
    study-->utils-spring-boot;
    db-test-->utils-spring-boot;

    dubai-->parent.base;
    dubai-model-->dubai;
    dubai-model-entity-->dubai-model;
    dubai-model-collection-->dubai-model;
    dubai-model-collection-->dubai-model-entity;
    dubai-model-collection-->utils-lang;
    dubai-model-service-->dubai-model;
    dubai-model-service-->dubai-model-collection;
    dubai-module-->dubai;
    dubai-module-->dubai-model-service;
    
    dubai-module-user-->dubai-module;

```

