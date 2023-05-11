# 我的项目汇总

* [parent:v1.3.0](https://github.com/dbstar-org/parent)
* [utils-lang:v1.0.9](https://github.com/dbstar-org/utils-lang)
* [utils-spring-boot:v1.0.7](https://github.com/dbstar-org/utils-spring-boot)
* [utils-spring-security:v1.0.3](https://github.com/dbstar-org/utils-spring-security)
* [utils-http-client:v1.1.0](https://github.com/dbstar-org/utils-http-client)
* [utils-net-api:v1.1.0](https://github.com/dbstar-org/utils-net-api)
* [utils-json:v1.1.0](https://github.com/dbstar-org/utils-json)
* [dubai:v1.1.3-SNAPSHOT](https://github.com/dbstar-org/dubai)
* [dubai-model-user:v1.0.4-SNAPSHOT](https://github.com/dbstar-org/dubai-model-user)
* [study-model:v1.0.0-SNAPSHOT](https://github.com/dbstar-org/study-model)
* [study-module-dictionary-iciba:v1.0.3-SNAPSHOT](https://github.com/dbstar-org/study-module-dictionary-iciba)
* [study-boot:v1.0.2-SNAPSHOT](https://github.com/dbstar-org/study-boot)
* [utils-openai:v1.0.0-SNAPSHOT](https://github.com/dbstar-org/utils-openai)

依赖关系：

```mermaid
graph TD;
    parent.base([parent:base]);
    parent.boot([parent:boot])--->parent.base;

    utils-lang-->parent.base;

    utils-spring-boot-->parent.base;

    utils-spring-security-->parent.base;
    utils-spring-security-->utils-lang;

    utils-http-client-->parent.base;

    utils-net-api-->parent.base;
    utils-net-api-->utils-http-client;

    utils-json-->parent.base;
    utils-json-->utils-net-api;

    dubai([dubai])-->parent.base;
    dubai-model([dubai-model])-->dubai;
    dubai-model-service-->utils-lang;
    dubai-model-service-->dubai-model;
    dubai-module([dubai-module])-->dubai;
    dubai-module-->dubai-model-service;
    
    dubai-model-user-->dubai-model;
    dubai-model-user-->dubai-model-service;

    study-module-dictionary-iciba-->dubai-module;
    study-module-dictionary-iciba-->study-model;
    study-module-dictionary-iciba-->utils-net-api;
    study-module-dictionary-iciba-->utils-json;

    study-model-->dubai-model;
    study-model-->dubai-model-user;

    study-boot-->parent.boot;
    study-boot-->study-module-dictionary-iciba;
    study-boot-->utils-spring-boot;
    study-boot-->utils-spring-security;
    study-boot-->utils-json;
    study-boot-->utils-net-api;

    utils-openai-->parent.base;
    utils-openai-->utils-net-api;
    utils-openai-->utils-json;
```
