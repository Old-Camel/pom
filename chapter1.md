# \*.pom文件为项目父工程,具体依赖包为公用jar包

**[spring](http://lib.csdn.net/base/javaee "Java EE知识库")**不同模块或者与外部进行集成时，依赖处理就需要各自对应版本号。比如，较新spring与较老的quartz，它们集成就会遇到问题，给搭建和升级带来不便。因此Spring IO Platform应运而生，只要项目中引入了它，外部集成时依赖关系无需版本号。Spring IO Platform只是一个pom文件，记录了spring与其他开源项目对应的版本。省去了版本号，也就省去了处理依赖时的问题，因为Spring IO Platform中有最优的版本配置。SpringSource为了解决这些Jar冲突，推出了各种BOM，当然最著名的就是spring platform io bom，其中最核心的三个是：spring-framework-bom、spring-boot-dependencies、platform-bom。对于Spring工程来说，直接在pom.xml文件中添加如下配置代码，即可免去管理版本冲突的难题.

```
<dependency> 
   <groupId>org.springframework</groupId> 
   <artifactId>spring-framework-bom</artifactId> 
   <version>3.2.9.RELEASE</version>  
   <type>pom</type>
   <scope>import</scope>
</dependency>
```

Javassist是一款字节码编辑工具，可以直接编辑和生成Java生成的字节码，以达到对.class文件进行动态修改的效果 .

```markdown
<dependency>
    <groupId>org.javassist</groupId>
    <artifactId>javassist</artifactId>
    <version>3.20.0-GA</version>
</dependency>
```

jboss的一个jar包

目的：快速开发高性能、高可靠性的网络服务器和客户端程序.

优点：提供异步的、事件驱动的网络应用程序框架和工具.用来处理socket.

```
<dependency>
    <groupId>io.netty</groupId>
    <artifactId>netty</artifactId>
    <version>${netty_version}</version>
</dependency>
```

Apache Mina是一个能够帮助用户开发高性能和高伸缩性网络应用程序的框架。它通过Java nio技术基于TCP\/IP和UDP\/IP协议提供了抽象的、事件驱动的、异步的API。

```
<dependency>
    <groupId>org.apache.mina</groupId>
    <artifactId>mina-core</artifactId>
    <version>${mina_version}</version>
</dependency>
```

基于java nio的网络通信应用程序框架,可以处理高性能非阻塞socked协议.

```
<dependency>
    <groupId>org.glassfish.grizzly</groupId>
    <artifactId>grizzly-core</artifactId>
    <version>${grizzly_version}</version>
</dependency>
```

提供对http服务器的访问功能

```
<dependency>
    <groupId>org.apache.httpcomponents</groupId>
    <artifactId>httpclient</artifactId>
    <version>${httpclient_version}</version>
</dependency>
```

阿里的dubbo的序列化协议

```
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>hessian-lite</artifactId>
    <version>${hessian_lite_version}</version>
</dependency>
```

json数据生成

```
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>fastjson</artifactId>
    <version>${fastjson_version}</version>
</dependency>
```

xml与java 对象相互转换

```
<dependency>
    <groupId>com.thoughtworks.xstream</groupId>
    <artifactId>xstream</artifactId>
    <version>${xstream_version}</version>
</dependency>
```

Bean Scripting Framework  java整合脚本语言用

```
<dependency>
    <groupId>org.apache.bsf</groupId>
    <artifactId>bsf-api</artifactId>
    <version>${bsf_version}</version>
</dependency>
```

zookeeper

```
<dependency>
    <groupId>org.apache.zookeeper</groupId>
    <artifactId>zookeeper</artifactId>
    <version>${zookeeper_version}</version>
</dependency>
```



```
<dependency>
    <groupId>com.github.sgroschupf</groupId>
    <artifactId>zkclient</artifactId>
    <version>${zkclient_version}</version>
</dependency>

<dependency>    <groupId>org.apache.curator</groupId>    <artifactId>curator-framework</artifactId>    <version>${curator_version}</version></dependency><dependency>    <groupId>redis.clients</groupId>    <artifactId>jedis</artifactId>    <version>${jedis_version}</version></dependency><dependency>    <groupId>com.googlecode.xmemcached</groupId>    <artifactId>xmemcached</artifactId>    <version>${xmemcached_version}</version></dependency><dependency>    <groupId>org.apache.cxf</groupId>    <artifactId>cxf-rt-frontend-simple</artifactId>    <version>${cxf_version}</version></dependency><dependency>    <groupId>org.apache.cxf</groupId>    <artifactId>cxf-rt-transports-http</artifactId>    <version>${cxf_version}</version></dependency>
```

