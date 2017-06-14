****
# \*-impl.pom文件为项目接口实现类依赖文件
###核心组件管理
****
```markdown
<dependency>
 <groupId>com.yunzainfo.pitcher</groupId>
 <artifactId>kernel-component-manager</artifactId>
 <version>1.0-SNAPSHOT</version>
 <scope>provided</scope>
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
##测试
```markdown
<dependency>
 <groupId>junit</groupId>
 <artifactId>junit</artifactId>
 <version>3.8.1</version>
 <scope>test</scope>
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
###solr

```markdown

<dependency>
   <groupId>org.apache.solr</groupId>
   <artifactId>solr-solrj</artifactId>
   <version>5.5.3</version>
   <scope>provided</scope>
</dependency>

```
###hadoop
```markdown

<dependency>
   <groupId>org.apache.hadoop</groupId>
   <artifactId>hadoop-common</artifactId>
   <version>2.7.1</version>
   <scope>provided</scope>
</dependency>

```












