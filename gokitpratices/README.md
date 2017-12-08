# go-kit 微服务

# 包依懒管理

    glide init
    glide get github.com/go-kit/kit

# 目录结构

- config
    - 存放配置文件或配置类
- services
    - 存放服务接口与实现
- endpoint
    - 存放endpoints
- transports
    - 存放transport，暴露service
- component
    - 存放一些公共组件如Middlewares、instrumentation

# 对比
## gin
|            |gokit|         gin|
|---|---|---|
|router   |   无     |        有|
|instrumentation|有|有|
|metrics| 有|加入第三方|
|json|需要加入第三方|有|

#使gin结合

- router
    - gokit - transports
        - gotkit -entpoints
            - gotkit - service

使用gin的rest router。内部以 rpc方式调用 gotkit 服务。 