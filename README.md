> #### 在fastapi内使用
fastapi框架已经内置该插件，所以只要写好配置就可以了。
```javascript
// src/conifg/index.default.js
module.exports = {
  // ...
  eureka: {
    name: 'union-service-new', // 这个应用注册到eureka的名字
    version: '1.0.0', // 注册的版本
    port: process.env.PORT || 3000, // 注册的端口
    urls: // 注册中心地址，多地址逗号分隔
      'http://eureka01:8761/eureka/apps,http://eureka02:8761/eureka/apps,http://eureka03:8761/eureka/apps'
  }
  // ...
}
```