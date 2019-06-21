# INSTALATION

## 1. Create Maven Archetype

```
$ git clone https://github.com/yossan/maven-quickstart-archetype.git
$ cd maven-quickstart-archetype/maven-quickstart-archetype
$ mvn archetype:create-from-project
```

## 2. Fix package name in App.java

target/generated-sources/archetype/target/classes/archetype-resources/src/main/java/App.java

Replace

```
package Sample;
```

with

```
package ${pacage};
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
