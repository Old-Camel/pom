# \*-impl.web文件为项目控制层类依赖文件

```markdown
###核心组件管理
<dependency>

     <groupId>com.yunzainfo.pitcher</groupId>
     <artifactId>kernel-component-manager</artifactId>
     <version>1.0-SNAPSHOT</version>
     <scope>provided</scope>
     <exclusions>
         <exclusion>
             <artifactId>log4j</artifactId>
             <groupId>log4j</groupId>
         </exclusion>
         <exclusion>
             <artifactId>slf4j-log4j12</artifactId>
             <groupId>org.slf4j</groupId>
         </exclusion>
    </exclusions>
</dependency>

```

###公用的javabean以及接口,例如Baseuser,Basemapper

```markdown

<dependency>

 <groupId>com.yunzainfo.pitcher</groupId>

 <artifactId>portal-api</artifactId>

 <version>1.0-SNAPSHOT</version>

 <scope>provided</scope>

</dependency>

```

###测试

```markdown

<dependency>

 <groupId>junit</groupId>

 <artifactId>junit</artifactId>

 <version>3.8.1</version>

 <scope>test</scope>

</dependency>
```

###dubbo

```markdown

<dependency>
   <groupId>com.alibaba</groupId>
   <artifactId>dubbo</artifactId>
   <version>2.9.1</version>
   <exclusions>
       <exclusion>
           <groupId>org.springframework</groupId>
           <artifactId>spring</artifactId>
       </exclusion>
       <exclusion>
           <artifactId>netty</artifactId>
           <groupId>org.jboss.netty</groupId>
       </exclusion>
       <exclusion>
           <artifactId>log4j</artifactId>
           <groupId>log4j</groupId>
       </exclusion>
       <exclusion>
           <groupId>org.slf4j</groupId>
           <artifactId>slf4j-api</artifactId>
       </exclusion>
  </exclusions>
</dependency>
```

###spring

```markdown
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-aop</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-aspects</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-core</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-beans</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-context</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-context-support</artifactId>
   <scope>provided</scope>
 </dependency
 <dependency>
   <groupId>or.springframework</groupId>
   <artifactId>spring-expression</artifactId>
   <scope>provided</scope
 </dependency>
 <dependency
   <groupId>org.springframework</groupId>
   <artifactId>spring-instrument</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-jdbc</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
 <groupId>org.springframework</groupId>
   <artifactId>spring-orm</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-oxm</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-test</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-tx</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-web</artifactId>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.springframework</groupId>
   <artifactId>spring-webmvc</artifactId>
   <scope>provided</scope>
 </dependency>


```

###aspectj

```markdown
<dependency>
  <groupId>org.aspectj</groupId>
  <artifactId>aspectjrt</artifactId>
  <version>1.6.11</version>
  <scope>provided</scope>
</dependency>
<dependency>
  <groupId>org.aspectj</groupId>
  <artifactId>aspectjweaver</artifactId>
  <version>1.6.11</version>
  <scope>provided</scope>
</dependency>
```

###事务

```markdown

<dependency>
   <groupId>javax.transaction</groupId>
   <artifactId>jta</artifactId>
   <version>1.1</version>
   <scope>provided</scope>
</dependency>
```

###json数据转换

```markdown

<dependency>
   <groupId>com.googlecode.json-simple</groupId>
   <artifactId>json-simple</artifactId>
   <version>1.1.1</version>
   <scope>provided</scope>
</dependency>
```

###mybatis

```markdown
 <dependency>
   <groupId>org.mybatis</groupId>
   <artifactId>mybatis</artifactId>
   <version>3.0.5</version>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.mybatis</groupId>
   <artifactId>mybatis-spring</artifactId>
   <version>1.0.1</version>
   <scope>provided</scope>
 </dependency>
 <dependency>
   <groupId>org.mybatis</groupId>
   <artifactId>mybatis-ehcache</artifactId>
   <version>1.0.0</version>
   <scope>provided</scope
   <exclusions>
       <exclusion>
       <groupId>net.sf.ehcache</groupId>
       <artifactId>core</artifactId>
       </exclusion>
   </exclusions>
 </dependency>
```

###java缓存

```markdown

<dependency>
 <groupId>net.sf.ehcache</groupId>
   <artifactId>ehcache-core</artifactId>
   <version>2.6.8</version>
   <scope>provided</scope>
</dependency><dependency>
   <groupId>net.sf.ehcache</groupId>
   <artifactId>ehcache-web</artifactId>
   <version>2.0.4</version>
   <scope>provided</scope>
</dependency>
```

###c3p0

```markdown

<dependency>
  <groupId>c3p0</groupId>
  <artifactId>c3p0</artifactId>
  <version>0.9.1.2</version>
  <scope>provided</scope>
</dependency>
```

###JAX-RS

```markdown
<dependency>
 <groupId>javax.ws.rs</groupId>
 <artifactId>jsr311-api</artifactId>
 <version>1.1.1</version>
 <scope>provided</scope>
</dependency>
```

###连接池

```markdown

<dependency>
 <groupId>com.alibaba</groupId>
 <artifactId>druid</artifactId>
 <version>1.0.9</version>
 <scope>provided</scope>
</dependency>
```

###oracle jdbc连接包

```markdown
<dependency>
 <groupId>com.oracle</groupId>
 <artifactId>ojdbc6</artifactId>
 <version>11.2.0.1.0</version>
 <scope>provided</scope>
</dependency>
```

###cxf

```markdown
<dependency>
 <groupId>org.apache.cxf</groupId>
 <artifactId>cxf-api</artifactId>
 <version>2.3.9</version>
 <scope>provided</scope>
</dependency>
<dependency>
 <groupId>org.apache.cxf</groupId>
 <artifactId>cxf-rt-transports-http</artifactId>
 <version>2.3.9</version>
 <scope>provided</scope>
</dependency>
```
###jsoup(解析html)
```markdown
<dependency>
 <groupId>org.jsoup</groupId>
 <artifactId>jsoup</artifactId>
 <version>1.1.1</version>
 <scope>provided</scope>
</dependency>
```
###Sigar(收集系统信息)
```markdown
<dependency>
 <groupId>org.fusesource</groupId>
 <artifactId>sigar</artifactId>
 <version>1.6.4</version>
 <exclusions>
    <exclusion>
    <artifactId>log4j</artifactId>
    <groupId>log4j</groupId>
    </exclusion>
 </exclusions>
</dependency> 
```
###WSDL解析

```markdown
<dependency>
  <groupId>wsdl4j</groupId>
  <artifactId>wsdl4j</artifactId>
  <version>1.6.2</version>
</dependency>
```
###XML解析器
```markdown
<dependency>
 <groupId>org.apache.ws.commons.schema</groupId>
 <artifactId>XmlSchema</artifactId>
 <version>1.4.7</version>
</dependency>

```
###io工具
```markdown
<dependency>
 <groupId>commons-io</groupId>
 <artifactId>commons-io</artifactId>
 <version>2.5</version>
</dependency>
```



