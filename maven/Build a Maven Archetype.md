## Build a Maven Archetype

Based on: 
https://maven.apache.org/archetypes/maven-archetype-webapp/

Run: 
```sh
mvn archetype:generate | grep maven-archetype-webapp
```
Pick the one which match with: 
```sh
xxxx : remote -> org.apache.maven.archetypes:maven-archetype-webapp (An archetype which contains a sample Maven Webapp project.)
```

Execute just: mvn archetype:generate and setup the options

```sh
mvn clean install   --> BUILD SUCCESS
```

A new target directory was created

```sh
├── pom.xml
├── src
│   └── main
│       └── webapp
│           ├── index.jsp
│           └── WEB-INF
│               └── web.xml
└── target
    ├── maven-archiver
    │   └── pom.properties
    ├── simple-webapp-project
    │   ├── index.jsp
    │   ├── META-INF
    │   └── WEB-INF
    │       ├── classes
    │       └── web.xml
    └── simple-webapp-project.war
```
