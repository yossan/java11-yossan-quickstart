# INSTALATION

## 1. Create Maven Archetype

```
$ git clone https://github.com/yossan/maven-quickstart-archetype.git
$ cd maven-quickstart-archetype/maven-quickstart-archetype
$ mvn archetype:create-from-project
```

And an Archetype is generated in the following directory.
`target/generated-sources/archetype/`


## 2. Fix package name in App.java


We need to fix the `package name` contained in the source files to specify the package name when creating a maven project. 
The source files is generated at the following directory.

```
target/generated-sources/archetype/target/classes/archetype-resources/src/main/java/*.java
```

Replace `package Sample;` with `package ${pacage};`. 
This looks like this.

```App.java
#set( $symbol_pound = '#' )
#set( $symbol_dollar = '$' )
#set( $symbol_escape = '\' )
package $package

/**
 * Hello world!
 *
 */
public class App 
{
    public static void main( String[] args )
    {
        System.out.println( "Hello World!" );
    }
}

```


# 3. Install to the local repository


```
$ cd target/generated-sources/archetype/
$ mvn install
```

# USAGE

```
$ mvn archetype:generate -DarchetypeCatalog=local -DarchetypeGroupId=io.github.yossan -DarchetypeArtifactId=maven-quickstart-archetype
```
