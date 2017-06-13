# \*.pom文件为项目父工程,具体依赖包为公用jar包

**[spring](http://lib.csdn.net/base/javaee "Java EE知识库")**不同模块或者与外部进行集成时，依赖处理就需要各自对应版本号。比如，较新spring与较老的quartz，它们集成就会遇到问题，给搭建和升级带来不便。因此Spring IO Platform应运而生，只要项目中引入了它，外部集成时依赖关系无需版本号。Spring IO Platform只是一个pom文件，记录了spring与其他开源项目对应的版本。省去了版本号，也就省去了处理依赖时的问题，因为Spring IO Platform中有最优的版本配置。SpringSource为了解决这些Jar冲突，推出了各种BOM，当然最著名的就是spring platform io bom，其中最核心的三个是：spring-framework-bom、spring-boot-dependencies、platform-bom。对于Spring工程来说，直接在pom.xml文件中添加如下配置代码，即可免去管理版本冲突的难题.

```markdown
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

```markdown
<dependency>
    <groupId>io.netty</groupId>
    <artifactId>netty</artifactId>
    <version>${netty_version}</version>
</dependency>
```

Apache Mina是一个能够帮助用户开发高性能和高伸缩性网络应用程序的框架。它通过Java nio技术基于TCP\/IP和UDP\/IP协议提供了抽象的、事件驱动的、异步的API。
```markdown
<dependency>
    <groupId>org.apache.mina</groupId>
    <artifactId>mina-core</artifactId>
    <version>${mina_version}</version>
</dependency>
```

基于java nio的网络通信应用程序框架,可以处理高性能非阻塞socked协议.

```markdown
<dependency>
    <groupId>org.glassfish.grizzly</groupId>
    <artifactId>grizzly-core</artifactId>
    <version>${grizzly_version}</version>
</dependency>
```

提供对http服务器的访问功能

```markdown
<dependency>
    <groupId>org.apache.httpcomponents</groupId>
    <artifactId>httpclient</artifactId>
    <version>${httpclient_version}</version>
</dependency>
```

阿里的dubbo的序列化协议
```markdown
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>hessian-lite</artifactId>
    <version>${hessian_lite_version}</version>
</dependency>
```

json数据生成

```markdown
<dependency>
    <groupId>com.alibaba</groupId>
    <artifactId>fastjson</artifactId>
    <version>${fastjson_version}</version>
</dependency>
```

xml与java 对象相互转换
```markdown
<dependency>
    <groupId>com.thoughtworks.xstream</groupId>
    <artifactId>xstream</artifactId>
    <version>${xstream_version}</version>
</dependency>
```

Bean Scripting Framework  java整合脚本语言用

```markdown
<dependency>
    <groupId>org.apache.bsf</groupId>
    <artifactId>bsf-api</artifactId>
    <version>${bsf_version}</version>
</dependency>
```

zookeeper相关

```markdown
<dependency>
    <groupId>org.apache.zookeeper</groupId>
    <artifactId>zookeeper</artifactId>
    <version>${zookeeper_version}</version>
</dependency>
<dependency>
    <groupId>com.github.sgroschupf</groupId>
    <artifactId>zkclient</artifactId>
    <version>${zkclient_version}</version>
</dependency><dependency>
    <groupId>org.apache.curator</groupId>
    <artifactId>curator-framework</artifactId>
    <version>${curator_version}</version>
</dependency>
```

redis客户端

```markdown
<dependency>
    <groupId>redis.clients</groupId>
    <artifactId>jedis</artifactId>
    <version>${jedis_version}</version>
</dependency>
```

基于java nio实现的高性能可扩展的memcached客户端
```markdown
<dependency>
    <groupId>com.googlecode.xmemcached</groupId>
    <artifactId>xmemcached</artifactId>
    <version>${xmemcached_version}</version>
</dependency>
```

WebService开源框架cxf
```markdown
<dependency>
    <groupId>org.apache.cxf</groupId>
    <artifactId>cxf-rt-frontend-simple</artifactId>
    <version>${cxf_version}</version>
</dependency>
<dependency>
    <groupId>org.apache.cxf</groupId>
    <artifactId>cxf-rt-transports-http</artifactId>
    <version>${cxf_version}</version>
</dependency>
```

thrift远程服务调用
```markdown
<dependency>
    <groupId>org.apache.thrift</groupId>
    <artifactId>libthrift</artifactId>
    <version>${thrift_version}</version>
</dependency>
```

JFreeChart图表绘制

```markdown
<dependency>
    <groupId>jfree</groupId>
    <artifactId>jfreechart</artifactId>
    <version>${jfreechart_version}</version>
</dependency>
```

hession序列化
```markdown
<dependency>
    <groupId>com.caucho</groupId>
    <artifactId>hessian</artifactId>
    <version>${hessian_version}</version>
</dependency>
```

jetty

```markdown
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>javax.servlet-api</artifactId>
    <version>${servlet_version}</version>
</dependency><dependency>
    <groupId>org.mortbay.jetty</groupId>
    <artifactId>jetty</artifactId>
    <version>${jetty_version}</version>
</dependency>
```

hibernate验证工具,如果在验证不通过的时候进行了添加、更新或删除操作的时候，则会抛出javax.validation.ConstraintViolationException异常
```markdown
 <dependency>
     <groupId>javax.validation</groupId>
     <artifactId>validation-api</artifactId>
     <version>${validation_version}</version>
 </dependency>
 <dependency>
     <groupId>org.hibernate</groupId>
     <artifactId>hibernate-validator</artifactId>
     <version>${hibernate_validator_version}</version>
 </dependency>
```markdown
CacheManager缓存

```markdown
<dependency>
    <groupId>javax.cache</groupId>
    <artifactId>cache-api</artifactId>
    <version>${jcache_version}</version>
</dependency>
```

SCA-Service Component Architecture,服务组件架构
```markdown
<dependency>
    <groupId>org.apache.tuscany.sca</groupId>
    <artifactId>tuscany-sca-api</artifactId>
    <version>${sca_version}</version>
</dependency>
```

googled ioc框架

```markdown
<dependency>
    <groupId>com.google.inject</groupId>
    <artifactId>guice</artifactId>
    <version>${guice_version}</version>
</dependency>
```

阿里WebX框架

```markdown
<dependency>
    <groupId>com.alibaba.citrus</groupId>
    <artifactId>citrus-webx-all</artifactId>
    <version>${webx_version}</version>
</dependency>
```

jackson 对象转json数据
```markdown
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-core</artifactId>
    <version>${jackson_version}</version>
</dependency><dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>${jackson_version}</version>
</dependency>
```

日志包
```markdown
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
    <version>${slf4j_version}</version>
</dependency>
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-log4j12</artifactId>
    <version>${slf4j_version}</version>
</dependency>
<dependency>
    <groupId>commons-logging</groupId>
    <artifactId>commons-logging-api</artifactId>
    <version>${jcl_version}</version>
</dependency><dependency>
    <groupId>log4j</groupId>
    <artifactId>log4j</artifactId>
    <version>${log4j_version}</version>
</dependency><dependency>
    <groupId>ch.qos.logback</groupId>
    <artifactId>logback-classic</artifactId>
    <version>${logback_version}</version>
</dependency>
```
测试包
```markdown
 <dependency>
     <groupId>junit</groupId>
     <artifactId>junit</artifactId>
     <version>${junit_version}</version>
     <scope>test</scope>
 </dependency>
 <dependency>
     <groupId>org.easymock</groupId>
     <artifactId>easymock</artifactId>
     <version>${easymock_version}</version>
     <scope>test</scope>
 </dependency>
 <dependency>
     <groupId>com.googlecode.jmockit</groupId>
     <artifactId>jmockit</artifactId>
     <version>${jmockit_version}</version>
     <scope>test</scope>
 </dependency>
 <dependency>
     <groupId>org.easymock</groupId>
     <artifactId>easymockclassextension</artifactId>
     <version>${easymock_version}</version>
     <scope>test</scope>
 </dependency>
 <dependency>
 <groupId>cglib</groupId>
     <artifactId>cglib-nodep</artifactId>
     <version>${cglib_version}</version>
 </dependency>
 <dependency>
     <groupId>commons-pool</groupId>
     <artifactId>commons-pool</artifactId>
     <version>${commons_pool_version}</version>
 </dependency>
 <dependency>
     <groupId>org.apache.tomcat.embed</groupId>
     <artifactId>tomcat-embed-core</artifactId>
     <version>${tomcat_embed_version}</version>
 </dependency>
 <dependency>
     <groupId>org.apache.tomcat.embed</groupId>
     <artifactId>tomcat-embed-logging-juli</artifactId>
     <version>${tomcat_embed_version}</version>
 </dependency>
```

javax.ws.rs创建restful
```markdown
 <dependency>
     <groupId>javax.ws.rs</groupId>
     <artifactId>javax.ws.rs-api</artifactId>
     <version>2.0</version>
 </dependency>
 <dependency>
     <groupId>org.jboss.resteasy</groupId>
     <artifactId>resteasy-jaxrs</artifactId>
     <version>3.0.7.Final</version>
 </dependency>
 <dependency>
     <groupId>org.jboss.resteasy</groupId>
     <artifactId>resteasy-client</artifactId>
     <version>3.0.7.Final</version>
 </dependency>
 <dependency>
     <groupId>org.jboss.resteasy</groupId>
     <artifactId>resteasy-netty</artifactId>
     <version>3.0.7.Final</version>
 </dependency>
 <dependency>
     <groupId>org.jboss.resteasy</groupId>
     <artifactId>resteasy-jdk-http</artifactId>
     <version>3.0.7.Final</version>
 </dependency>
 <dependency>
     <groupId>org.jboss.resteasy</groupId>
     <artifactId>resteasy-jackson-provider</artifactId>
     <version>3.0.7.Final</version>
 </dependency>
 <dependency>
     <groupId>org.jboss.resteasy</groupId>
     <artifactId>resteasy-jaxb-provider</artifactId>
     <version>3.0.7.Final</version>
 </dependency>
 <dependency>
     <groupId>com.esotericsoftware.kryo</groupId>
     <artifactId>kryo</artifactId>
     <version>2.24.0</version>
 </dependency>
 <dependency>
     <groupId>de.javakaffee</groupId>
     <artifactId>kryo-serializers</artifactId>
     <version>0.26</version>
 </dependency>
 <dependency>
     <groupId>de.ruedigermoeller</groupId>
     <artifactId>fst</artifactId>
     <version>1.55</version>
 </dependency>
 <dependency>
     <groupId>aopalliance</groupId>
     <artifactId>aopalliance</artifactId>
     <version>${aopalliance.version}</version>
 </dependency>
```
文件上传
```markdown
 <dependency>
     <groupId>commons-fileupload</groupId>
     <artifactId>commons-fileupload</artifactId>
     <version>${commons-fileupload.version}</version>
 </dependency>
```
lang包工具类
```markdown
 <dependency>
     <groupId>commons-lang</groupId>
     <artifactId>commons-lang</artifactId>
     <version>${commons-lang.version}</version>
 </dependency>
```
druid数据库连接
```markdown
 <dependency>
     <groupId>com.alibaba</groupId>
     <artifactId>druid</artifactId>
     <version>${com.alibaba.druid.version}</version>
 </dependency>
```
servlet  
```markdown
 <dependency>
     <groupId>javax.servlet</groupId>
     <artifactId>jstl</artifactId>
     <version>${javax.servlet.jstl.version}</version>
 </dependency>
 <dependency>
     <groupId>javax.servlet</groupId>
     <artifactId>servlet-api</artifactId>
     <version>${javax.servlet.servlet-api.version}</version>
 </dependency>
```

shiro
```markdown
 <dependency>
     <groupId>org.apache.shiro</groupId>
     <artifactId>shiro-all</artifactId>
     <version>${org.apache.shiro.shiro-all.version}</version>
 </dependency>
```







