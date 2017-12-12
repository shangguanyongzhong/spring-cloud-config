##day06分布式配置中心(Spring Cloud Config-I)
在分布式系统中，由于服务数量巨多，为了方便服务配置文件统一管理，实时更新，所以需要分布式配置中心组件。在Spring Cloud中，有分布式配置中心组件spring cloud config ，它支持配置服务放在配置服务的内存中（即本地），也支持放在远程Git仓库中。在spring cloud config 组件中，分两个角色，一是config server，二是config client

##day07分布式配置中心(Spring Cloud Config-II)
上一篇文章讲述了一个服务如何从配置中心读取文件，配置中心如何从远程git读取配置文件，当服务实例很多时，都从配置中心读取文件，这时可以考虑将配置中心做成一个微服务，将其集群化，从而达到高可用  

##day08 Spring Cloud Bus
Spring Cloud Bus 将分布式的节点用轻量的消息代理连接起来。它可以用于广播配置文件的更改或者服务之间的通讯，也可以用于监控。本文要讲述的是用Spring Cloud Bus实现通知微服务架构的配置文件的更改。
无需再次启动服务，动态去修改配置信息。
######
1.需要下载：rabbitmq
2.需要发送post请求：http://localhost:8881/bus/refresh（这里使用postman发送post请求）
3.将博主的公共服，改为自己的服务

##day09服务链路追踪(Spring Cloud Sleuth)
Spring Cloud Sleuth 主要功能就是在分布式系统中提供追踪解决方案，并且兼容支持了 zipkin，你只需要在pom文件中引入相应的依赖即可。

