# neo4j 在线实验环境

## 软件简介

Neo4j是一个高性能的,NOSQL图形数据库，它将结构化数据存储在网络上而不是表中。它是一个嵌入式的、基于磁盘的、具备完全的事务特性的Java持久化引擎，但是它将结构化数据存储在网络(从数学角度叫做图)上而不是表中。Neo4j也可以被看作是一个高性能的图引擎，该引擎具有成熟数据库的所有特性。程序员工作在一个面向对象的、灵活的网络结构下而不是严格、静态的表中——但是他们可以享受到具备完全的事务特性、企业级的数据库的所有好处。

所属类别是数据库

特点:

1.面向网络

2.节点多

3.易观察

## 软件官网

https://neo4j.com/

## Dockerfile 使用方法

开始一个neo4j的实例

您可以像这样启动一个Neo4j容器：
```
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    neo4j
```
这允许您通过浏览器访问neo4j，网址为：http：// localhost：7474。

这绑定了两个端口（7474和7687）用于HTTP和Bolt访问Neo4j API。卷/data必须允许数据库在容器外部保持。

默认情况下，这需要您登录neo4j/neo4j并更改密码。为了开发目的，您可以通过传递--env=NEO4J_AUTH=none到docker 运行来禁用身份验证。

## 资源链接

- http://agapple.iteye.com/blog/1128400
- http://www.oschina.net/p/neo4j
- http://neo4j.com/docs/operations-manual/current/installation/docker/
