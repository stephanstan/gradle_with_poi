# gradle_with_poi
explore gradle with poi from apache

* gradle init --type groovy-library

* https://spring.io/guides/gs/gradle/

* Markdown basics
	* https://help.github.com/articles/markdown-basics/
	* https://help.github.com/articles/github-flavored-markdown/
	
* example project with poi
* https://github.com/stephanstan/griddle

* showed that poi is part of the dependency tree
gradle -q dependencies

* tutorial
http://www.vogella.com/tutorials/Gradle/article.html


* https://help.github.com/articles/github-flavored-markdown/

| git commands| 
------------------
| git status| 
| git add build.gradle| 
| git commit -a -m "add description to project" | 
| git push| 

C:\grails\workspace\gradle_with_poi [master +1 ~1 -0 !]> gradle dependencies
:dependencies

------------------------------------------------------------
Root project - Stephan Stan - Learning about gradle and incorporating dependencies like poi.  Ultimate goal of converting / upgrading some java projects.  Better standardization.
------------------------------------------------------------

archives - Configuration for archive artifacts.
No dependencies

compile - Compile classpath for source set 'main'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
\--- com.oracle:ojdbc6:11.2.0.4

default - Configuration for default artifacts.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
\--- com.oracle:ojdbc6:11.2.0.4

runtime - Runtime classpath for source set 'main'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
\--- com.oracle:ojdbc6:11.2.0.4

testCompile - Compile classpath for source set 'test'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
+--- com.oracle:ojdbc6:11.2.0.4
+--- org.spockframework:spock-core:1.0-groovy-2.4
|    +--- org.codehaus.groovy:groovy-all:2.4.1 -> 2.4.5
|    \--- junit:junit:4.12
|         \--- org.hamcrest:hamcrest-core:1.3
\--- junit:junit:4.12 (*)

testRuntime - Runtime classpath for source set 'test'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
+--- com.oracle:ojdbc6:11.2.0.4
+--- org.spockframework:spock-core:1.0-groovy-2.4
|    +--- org.codehaus.groovy:groovy-all:2.4.1 -> 2.4.5
|    \--- junit:junit:4.12
|         \--- org.hamcrest:hamcrest-core:1.3
\--- junit:junit:4.12 (*)

(*) - dependencies omitted (listed previously)

BUILD SUCCESSFUL

Total time: 5.911 secs
C:\grails\workspace\gradle_with_poi [master +1 ~1 -0 !]>


























































































































































































































































































































































































































 