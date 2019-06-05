* https://www.mkyong.com/maven/how-to-include-library-manully-into-maven-local-repository/
```
mvn install:install-file -Dfile=c:\kaptcha-{version}.jar -DgroupId=com.google.code -DartifactId=kaptcha -Dversion={version} -Dpackaging=jar
```
