###textbook-impl的依赖文件
####~~~~引入textbook-api+mybatis的依赖包.打包方式为war包.
```markdown
<?xml version="1.0" encoding="UTF-8"?>

<project xmlns="http://maven.apache.org/POM/4.0.0"

 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

 xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">

 <parent>
     <artifactId>textbook</artifactId>
     <groupId>com.yunzainfo.pitcher.plugin</groupId>
     <version>1.0-SNAPSHOT</version>
 </parent>
 <modelVersion>4.0.0</modelVersion>
 <artifactId>textbook-impl</artifactId>
 <packaging>war</packaging>
 <version>1.0-SNAPSHOT</version>
 <dependencies>
 <dependency>
 <groupId>com.yunzainfo.pitcher.plugin</groupId>
     <artifactId>textbook-api</artifactId>
     <version>1.0-SNAPSHOT</version>
     <scope>provided</scope>
 </dependency>

 <!--mybatis start -->

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
     <scope>provided</scope>
     <exclusions>
         <exclusion>
             <groupId>net.sf.ehcache</groupId>
             <artifactId>core</artifactId>
         </exclusion>
     </exclusions>
 </dependency>

 <!--mybatis end-->
 </dependencies>
 <build>
 <finalName>textbook-impl</finalName>
 <plugins>
     <plugin>
         <groupId>org.apache.maven.plugins</groupId>
         <artifactId>maven-compiler-plugin</artifactId>
         <configuration>
         <source>1.7</source>
         <target>1.7</target>
         </configuration>
     </plugin>
     <plugin>
         <groupId>com.yunzainfo.pitcher.maven.plugin</groupId>
         <artifactId>pitcher-devp-maven-plugin</artifactId>
         <version>${pitcher.devp.plugin.version}</version>
         <configuration>
         <destination>${tomcat.components}</destination>
         <copyType>DIR</copyType>
         </configuration>
         <executions>
             <execution>
                 <id>plugin-deploy</id>
                 <phase>package</phase>
                 <goals>
                     <goal>deploy</goal>
                 </goals>
            </execution>
        </executions>
     </plugin>
 </plugins>
 </build>
</project>

```