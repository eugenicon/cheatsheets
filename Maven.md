create project

    mvn archetype:generate

clean project: will delete target directory

    mvn clean
    
validate project: validate the project is correct and all necessary information is available

    mvn validate
    

compile project:compile source code, classes stored in target/classes

    mvn compile
    
test project: run tests using a suitable unittesting framework

    mvn test
    
package project: take the compiled code and package it in its distributable format, such as a JAR /WAR

    mvn package
    
install project: install the package into the local repository, for use as a dependency in other projects locally

    mvn install
    

compiler plugin

```xml
    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.5.1</version>
        <configuration>
          <source>${jdk.version}</source>
          <target>${jdk.version}</target>
        </configuration>
      </plugin>
```
